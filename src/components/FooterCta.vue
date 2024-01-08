<script>
export default{
    name: "FooterCta",
    
}
</script>

<template>
    <div class="footer-cta">
        <div>
            <a href="/" class="btn">SIGN UP NOW</a>
        </div>
        <div>

        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

.footer-cta{
    background-color: $primary;
    @include space-between;
}


</style>