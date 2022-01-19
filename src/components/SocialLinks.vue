<template>
    <div>
        <ul>
            <li class="d-inline-block">
                <a href="https://www.facebook.com"><i class="fab fa-facebook-f"></i></a>
            </li>
            <li class="d-inline-block">
                <a href="https://www.instagram.com"><i class="fab fa-instagram"></i></a>
            </li>
            <li class="d-inline-block">
                <a href="https://www.twitter.com"><i class="fab fa-twitter"></i></a>
            </li>
            <li class="d-inline-block">
                <a href="https://www.youtube.com"><i class="fab fa-youtube"></i></a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'SocialLinks'
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

i{
    color: $secondary_text_color;
    margin: 0 15px;
}
</style>