<template>
    <div class="wrapper">
        <div class="header">
            <h4>Notification</h4>
        </div>
        <div class="feedbacks">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id iusto qui earum possimus. Recusandae, unde. Quis quas doloribus totam ex ea alias, accusantium nihil?</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Feedbacks'

}
</script>

<style lang="scss" scoped>
@import "/scss/style.scss";
.wrapper{
    // height: 50vh;
    height: 350px;
    width: 70%;
    background: #FFFFFF;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    margin: 30px 0 0 25%;
    @media screen and (max-width: 1500px) {
        // height: 80vh;
        height: 350px;
    }
    @media screen and (max-width: 900px) {
        height: 120vh;
    }
    @media screen and (max-width: 450px) {
        height: 150vh
    }
    .header{
        @include font(5, 300, 7vh, $white);
        top: 0;
        left: 0;
        height: 7vh;
        background: #00A4DB;
        text-align: start;
        text-indent: 3%;
    }
    .feedbacks{
        text-align: start;
        height: 100%;
        margin:20px 0 15px 19px;
        & p{
            @include font(14px, 400, 21px, $black);
            @include style(normal, 'Poppins');
        }
    }
}
</style>
