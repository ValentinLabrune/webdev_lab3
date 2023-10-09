<template>
    <div>
        <button :disabled="isPending" @click="AsyncClick">Asunc Button</button>
    </div>
</template>

<script>
export default {
    name: 'HomePage',
    data() {
        return {
            isPending : false
        }
    },
    methods: {
        async AsyncClick() {
            console.log('AsyncClick')
            if (this.isPending) {
                return; 
            }
            
            this.isPending = true;

            try {
                await this.$emit('async-click');
            } catch (error) {
                console.error('Error:', error);
            } finally {
                setTimeout(() => {
                this.isPending = false;
            }, 2000);
            }
        }
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

button:disabled {
  background-color: grey;
  color: white;
  cursor: not-allowed;
}

button:disabled:hover{
    background-color: red;
}

button:hover{
    background-color: green;
}
</style>