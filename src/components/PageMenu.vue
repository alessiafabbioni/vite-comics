<script>
export default{
    name: "PageMenu",
    data () {
        return {
            cards: [
                {
                    text: "DIGITAL COMICS",
                    url: "#",
                    img: "/img/buy-comics-digital-comics.png",
                    alt: "digital comics",
                    current: false,
                },
                {
                    text: "DC MERCHANDISE",
                    url: "#",
                    img: "/img/buy-comics-merchandise.png",
                    alt: "merchandise",
                    current: false,
                },
                {
                    text: "SHOP LOCATOR",
                    url: "#",
                    img: "/img/buy-comics-shop-locator.png",
                    alt: "shop locator",
                    current: false,
                },
                {
                    text: "SUBSCRIPTION",
                    url: "#",
                    img: "/img/buy-comics-subscriptions.png",
                    alt: "subscription",
                    current: false,
                },
                {
                    text: "DC POWER VISA",
                    url: "#",
                    img: "/img/buy-dc-power-visa.svg",
                    alt: "dc power visa",
                    current: false,
                },

            ]

            
        }
    }
}
</script>

<template>
    <section class="page-menu">
        <div v-for="card in cards" class="page-card">
            <a :href="card.url" :class="card.current ? 'active' : ''">
                <img :src="card.img" :alt="card.alt">
            </a>
            <a><span>{{ card.text }}</span></a>
        </div>
    </section>
  
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

/* insert info regarding class active*/
.page-menu {
    background-color: $secondary;
    @include center();
    color: white;

    .page-card {
        @include space-between;
        padding: 2rem;
        margin: 1rem;

        span {
            padding: 1rem;
            font-size: 12px;
            color: white;
            @include center();

            &.active,
            &:hover {
                border-bottom: solid 5px white;
            }
        }
    }

}

</style>