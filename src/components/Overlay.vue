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
// Overlay
.overlay{
    color: white;
    font-weight: 600;
    text-align: center;
    font-size: 25px;
    display: none;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background: linear-gradient(rgba(252,117,35,0.5), rgba(252,117,35,1));
}
.paperclip{
        height: 50px;
        width: 50px;
        border-radius: 50%;
        background-color: white;
        color: black;
        font-size: 22px;
}
</style>