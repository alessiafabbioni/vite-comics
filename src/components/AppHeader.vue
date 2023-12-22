<script>
export default{
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false, 
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: false, 
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false, 
                },
                {
                    text: "TV",
                    url: "#",
                    current: false, 
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false, 
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false, 
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false, 
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false, 
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false, 
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false, 
                },
            ]
        }

    }
}
</script>

<template>
  <header>
    <!-- logo principale -->
    <a href="/">
        <img src="/img/dc-logo.png" alt="DC Logo">
    </a>
    <!-- navigazione menu principale -->
    <ul>
        <li v-for="link in links">
            <a :href="link.url" :class="link.current ? 'active' : ''">
                {{ link.text }}
            </a>
        </li>
    </ul>


  </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

header {
    text-align: center;
    @include space-between;

    a {
        padding: 1rem;

    }

    ul {
        list-style: none;
        margin: 0 2rem; 
        @include center();

        li a{
            display: inline-block;
            padding: 2.5rem 1rem 5rem;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s;

            &.active,
            &:hover {
                color: $secondary;
                border-bottom: solid 7px $secondary; 
            }


        }
    };
}

</style>