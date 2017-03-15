<template>
    <div>
        New Quote
        <button @click="counter++">Counter++</button>
        {{counter}}
    </div>
</template>

<script>
    export default{
        data(){
            return {
                counter:0
            }
        },
        destroyed(){
            console.log('destroyed')
        },
        deactivated(){
            console.log('deactivated')
        },
        activated(){
            console.log('activated')
        }
    }
</script>