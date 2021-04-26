<template>
    <header class="py-4 border-b-3 header">
        <div class=" header-container">
           <h1> {{logo}} </h1>
        </div>
        
    </header>
</template>

<script>
export default {
    data(){
        return {
            logo: "CAT"
        }
    }
}
</script>

<style scoped>
.header{
    position: fixed;
    width: 100%;
    background: #fff;
}
.header-container{
width: 90%;
margin: 0 auto;
}

.header-container h1{
    font-size: 1.5rem;
    font-family: 'Great Vibes', cursive;
}
</style>