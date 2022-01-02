<template>

<div class="menu">
    <div class="menu-item-wrapper">
        <div class="menu-item" id="logo">
            <img src="../assets/logo.png" alt="Logo">
        </div>
        <div class="menu-item">
        <!-- </div>
        <div class="menu-item"> -->
            <!-- <a href="farzanali1296@gmail.com" target="blank">
                <fa :icon="['fas', 'envelope']" />
                <p>farzanali1296@gmail.com</p>
            </a> -->
            <a href="https://google.ca" target="blank">
                <div class="menu-text">
                    Resume
                </div>
            </a>
        </div>
    </div>
</div>

</template>

<script>
export default {
    name: 'Menu'
}
</script>

<style>

.menu {
    display: flex;
    align-items: center;
    justify-content: space-around;
    margin-top: 10px;
    height: 60px;
}
.menu-item-wrapper{
    display: flex;
    justify-content: space-between;
    width: 80%;
    max-width: 1344px;
}
.menu-item {
    /* flex: 1; */
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 0 0 50px;
}
.menu-item img{
    width: 50px;
}
#logo{
    margin: 0;
}
.menu-item p{
    color: #c278ff;
    margin: 0 30px 0 15px;
}
.menu-item svg{
    font-size: 25px;
    color: #c278ff;
}
.menu-item a{
    text-decoration: none;
    display: flex;
}
.menu-text{
    font-family: 'Roboto Mono', monospace;
    font-size: 14px;
    color: #5dedcd;
    cursor: pointer;
    padding: 10px;
    border: 2px solid #5dedcd;
    /* border-bottom: 2px solid #080808; */
    width: fit-content;
    transition: all 0.1s linear;

}
.menu-text:hover {
    /* border-bottom: 2px solid #c278ff; */
    background: #5dedcd;
    color: #fff;
}
.menu-center {
    font-size: 36px;
    color: #EAEAEA;
}

</style>