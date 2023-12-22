<script>
export default{
    name: "AppHeader"
}
</script>

<template>
  <header>
    <a href="/">
        <img src="/img/dc-logo.png" alt="DC Logo">
    </a>
    <ul>
        <li><a href="/">CHARACTERS</a></li>
        <li><a href="/">COMICS</a></li>
        <li><a href="/">MOVIES</a></li>
        <li><a href="/">TV</a></li>
        <li><a href="/">GAMES</a></li>
        <li><a href="/">COLLECTIBLES</a></li>
        <li><a href="/">VIDEOS</a></li>
        <li><a href="/">FANS</a></li>
        <li><a href="/">NEWS</a></li>
        <li><a href="/">SHOP</a></li>
    </ul>


  </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

header {
    text-align: center;
    @include space-between();

    a {
        padding: 1rem;

    }

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