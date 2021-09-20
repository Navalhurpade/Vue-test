<template>
<h1>Counter</h1>
	<div>
	<h1>{{ counter }}</h1>	
		<button @click="counter--" >-</button>
		<button @click="counter++" >+</button> 
	</div>
</template>

<script>
export default {
	name: "Counter",
	data() {
		return {
			counter: 0,
		};
	},
};
</script>

<style>
h1{
  font-size: 4rem;
}
button {
padding: 10px 30px;
border-radius: 10px;
background-color: rgb(67, 121, 201);
border: none;
margin: 0 20px;
color: white;
font-size: 20px;
}

</style>