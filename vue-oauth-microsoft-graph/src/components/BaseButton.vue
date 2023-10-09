<template>
    <div>
        <button>click here !</button>
        <button id="disabled">I'm disabled</button>
    </div>
</template>

<script>
export default {
    name: 'HomePage',
    data() {
        return {
            // Your data goes here
        }
    },
    methods: {
        // Your methods go here
    },
    mounted() {
        // Your mounted code goes here
    }
}
</script>

<style>
button{
    background-color: lightgreen;
    padding: 1em;
    text-align: center;
    border: none;
    border-radius: 5px;
    margin: 0.5em;
}

#disabled{
    background-color: grey;
    color: white;
    cursor: not-allowed;
}

button:hover{
    background-color: green;
}
</style>