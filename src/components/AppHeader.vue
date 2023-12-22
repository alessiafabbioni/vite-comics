<script>
export default{
    name: "AppHeader"
}
</script>

<template>
  <header>
    <a href="/">
        <img src=".public/img/ds-logo.png" alt="DC Logo">
    </a>


  </header>
</template>

<style lang="scss" scoped>
@use './styles/partials/variables.scss' as *;
@use './styles/mixins.scss' as *;

header {
    text-align: center;

    ul {
        list-style: none;
        margin: 2.5rem 1rem 4rem;
        @include center();

        li a{
            display: inline-block;
            padding: 1rem;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.5s;

            &.active,
            &:hover {
                color: $secondary;
                border-bottom: solid 3px $secondary; 
            }


        }
    };
}

</style>