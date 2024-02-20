<template>
    <div class="back">
        <div class="container">
            <h1>Color<span :style="{color:colors}">Flip</span></h1>
            <ul>
                <li>Hex</li>
                <li>Color</li>
                <li>RGB</li>
            </ul>

        </div>
    </div>
</template>

<script>
export default {
    name: "MenuSimple",
    props: ['colors']
}
</script>

<style scoped>
.back{
    background-color: rgb(146, 166, 255);
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}
.container{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 700px;
    height: 60px;
}
.container span{
    color: black;
}

.container h1 {
    padding-left: 1rem ;
    color: white;
}

.container ul{
    display: flex;
    color: white;
    list-style: none;
    
}

.container ul li {
    cursor: pointer;
    margin: 1rem;
    transition: .3s ease-in-out;
}

.container ul li:hover{
    transform: scale(1.1);
    font-weight: 600;
    border-bottom: 1px solid white;
}
.container ul li:focus{
    transform: scale(1.1);
    font-weight: 600;
}
</style>