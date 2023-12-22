<script>
export default{
    name: "PageMenu"
}
</script>

<template>
    <section class="page-menu">
        <div class="page-card">
            <a href="/">
                <img src="/img/buy-comics-digital-comics.png" alt="digital comics">
            </a>
            <span>DIGITAL COMICS</span>
        </div>
        <div class="page-card">
            <a href="/">
                <img src="/img/buy-comics-merchandise.png" alt="merchandise">
            </a>
            <span>DC MERCHANDISE</span>
        </div>
        <div class="page-card">
            <a href="/">
                <img src="/img/buy-comics-shop-locator.png" alt="shop locator">
            </a>
            <span>SHOP LOCATOR</span>
        </div>
        <div class="page-card">
            <a href="/">
                <img src="/img/buy-comics-subscriptions.png" alt="subscriptions">
            </a>
            <span>SUBSCRIPTION</span>
        </div>
        <div class="page-card">
            <a href="/">
                <img src="/img/buy-dc-power-visa.svg" alt="power visa">
            </a>
            <span>DC POWER VISA</span>
        </div>
        
    </section>
  
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

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
        }
    }
}

</style>