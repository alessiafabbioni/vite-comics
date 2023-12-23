<script>
export default{
    name: "FooterMenu",
    data() {
        return {
            footerNavs: [
                {
                    section: 'DC COMICS',
                    links: ['characters', 'comics', 'movies', 'tv', 'games', 'videos', 'news']
                },
                {
                    section: 'SHOP',
                    links: ['shop dc', 'shop dc collectibles']
                },
                {
                    section: 'DC',
                    links: ['terms of use', 'privacy policy', 'ad choices', 'advertising', 'jobs', 'subscriptions', 'talent workshops', 'CPSC certificates', 'ratings', 'shop help', 'contact us']
                },
                {
                    section: 'SITES',
                    links: ['DC', 'Mad magazine', 'DC kids', 'DC Universe', 'DC power visa']
                },
            ]
        }
    }
}
</script>

<template>
    <footer class="row">
        <nav class="col" v-for="footerNav in footerNavs" :key="footerNav.section">
            <h3>{{ footerNav.section }}</h3>
            <ul>
                <li v-for="link in footerNav.links" :key="link">{{ link }}</li>
            </ul>
        </nav>


    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

footer {
    background-color: black;
    background-image: url("./img/footer-bg.jpg");

}
nav {

    h3 {
        color: white;
    }

    ul {
        list-style: none;
    }

    li {
        color: gray;
        padding: 5px 0;
    }
}

.row {
    display: flex;
    flex-direction: row;
}

.col{
    margin: 1rem;
}

</style>