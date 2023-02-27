<template>
    <div class="background py-5">
            <img class="circular--square me-4" src="../assets/picture.png" alt="Avatar">
            <span class="profile-name">HUANG Xiaohan</span>

    </div>
    
</template>

<script>
export default{
    name: 'profile-header'
}
</script>

<style>
.background {
    background: url("../assets/bg-image.png") no-repeat;
    background-size: 100%;
    text-align: center;
}

.circular--square { 
    width: 150px;
    height: 150px;
    border-radius: 50%;
    border-color:antiquewhite;
    border-style: double;
    border-width: 8px;
 }

.profile-name {
    font-weight: 600;
    font-size: 40px;
    line-height:65px;
    letter-spacing: 2px;
    text-align: center;
    text-transform: uppercase;
}
</style>