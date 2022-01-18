<template>
    <div class="overlay d-flex flex-column align-items-center justify-content-center"> 
        <div class="paperclip d-flex align-items-center justify-content-center mb-3">
            <a href="#"><i class="fas fa-paperclip"></i></a>
        </div>
        {{text}} 
    </div>
</template>

<script>
export default {
    name: 'Overlay',
    props: {
        text: String
    }
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/variables.scss';

.paperclip{
        height: 50px;
        width: 50px;
        border-radius: 50%;
        background-color: white;
        color: black;
        font-size: 22px;
}
</style>