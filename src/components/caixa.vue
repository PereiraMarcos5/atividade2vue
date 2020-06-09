<template>
    <div id="caixa">
        <input type="text" placeholder="Criar Tarefa" class="placeHolder" v-model="texto">
        <button class="button" @click="criar">Criar</button>
    </div>
</template>

<script>
export default {
    name : 'caixa',
    data: function(){
        return{
            texto: ''
        }
    }, methods: {
        criar: function(){
            this.$emit('criar', {texto: this.texto})
            this.texto = "";
        }
    }
}
</script>

<style>
    #caixa{
        width: 300px;
        height: 60px;
        margin: 30px auto 50px auto;
        display: flex;
        flex-wrap: wrap;
        border-radius: 2px;
    }
    .placeHolder{
        width: 300px;
        height: 20px;
        margin: 50px 0 0 0px;
    }
    .button{
        height: 26px;
        margin-top: 0px;
        margin-left: 256px;
        margin-bottom: 20px ;
        background-color: white;
        border-radius: 2px;
        outline: none;
        color: black    ;
    }
</style>