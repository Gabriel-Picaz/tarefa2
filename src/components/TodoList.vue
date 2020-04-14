<template>
  <div id="todoList">
      <div class="tarefasCaixas" v-for="(todoList, index) in tarefas" :key="index">
        {{todoList.descricao}}
      </div>
  </div>
</template>

<script>
export default {
    name:"TodoList",
    props:['tarefas']
}
</script>

<style>
    #todoList{
        background-color: rgb(236, 119, 9);
        width: 500px;
        height: 150px;
        margin: 10px auto 0px auto;
        display: flex;
        flex-wrap: wrap;
        overflow: auto; /* barra de rolagem*/
        border: black 2px solid;
        border-radius: 20px;
    }

    .tarefasCaixas{
        width: (tarefas);
        background-color: #06beb6;
        height: 50px;
        border: 2px solid black;
        margin: 5px 20px 0 10px;
        text-align: center;
        line-height: 50px;
        cursor: pointer;
        color: black; 
        overflow: hidden; /* esconde uma parte do texto dentro da caixa*/
    }
</style>