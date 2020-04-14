<template>
  <div id="Form">
  <input id="texto" type="text" placeholder="Nova Tarefa?" v-model="novaTarefa">
  <button id="botao" @click="adicionarTarefa">OK</button>
  </div>
</template>

<script>
export default {
    name: "TodoForm",
    data: function(){
        return{
            novaTarefa: ''
        }
    }, methods:{
        adicionarTarefa: function(){
            this.$emit('addTarefa',{novaTarefa: this.novaTarefa})
        }
    }
}
</script>

<style>
    #Form{
        background-color: rgb(236, 119, 9);
        width: 500px;
        height: 170px;
        margin: 50px auto 0px auto;
        border: 2px black solid;
        border-radius: 20px;
    }

    #texto{
        margin: 80px 0 0 27%;
        height: 20px;
        width: 200px;
        border: black 2px solid;
    }

    #botao{
       width: 50px;
       height: 20px;
       color: red;
       outline: none;
       cursor: pointer;
       margin: 0px 5px;
    }
</style>