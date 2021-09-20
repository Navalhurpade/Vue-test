<template>
<h1>Todo List</h1>
    <ul>
        <div class="listItem"  v-bind:key="item" v-for="(item, index) in items">
           <li >{{item}}</li>
           <button class="delete" @click="remove(index)" >Delete</button>
        </div>
    </ul>
    <input placeholder="add a Item..." v-model="newItem" type="text">
    <button @click="add(newItem)" >Add </button>
</template>

<script>

export default {
    name: "Todo",
    data: () => {
        return{
        items: ["vue", "react", "angular"],
        newItem: ""
    }
    },
    methods: {
        add(newItem) {
            if(!newItem) return
         this.items.push(newItem)
         this.newItem = ""
       },
       remove(index){
        this.items.splice(index, 1)
       }
    }
}
</script>

<style scoped>
.listItem {
    display: flex;
    flex-direction: "row";
    align-items: center;
    /* background-color: blue; */
    width: 25%;
    margin: 10px auto ;
}

.delete{
    background-color: rgb(218, 72, 72);
    margin-left: auto;
    padding: 5px 15px;
    font-size: 18px;
}

input{
    padding: 10px;
    border-radius: 10px;
    border: 2px solid rgb(216, 216, 216);
}
</style>