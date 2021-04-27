<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal" :class="{sale : theme === 'sle' }" >
            <h1>{{ header }}</h1>
            <p>{{ text }}</p>
        </div>
    </div>
</template>
<script>
export default {
    props:["header", "theme", "text"],
    methods:{
        closeModal(){
            this.$emit('closeM')
        }
    }
}
</script>

<style>
.backdrop{
    background-color: rgba(0, 0, 0, 0.5);
    top: 0;
    position: fixed;
    height: 100%;
    width:100%;
}
.modal{
    background: white;
    border-radius: 2rem;
    margin: 10% auto;
    width:30rem;
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 1.5rem;
    height:20rem;
    padding: 2rem;
}
.modal.sale{
    background-color: crimson;
    color:white;
}
</style>