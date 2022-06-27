<template>
    <Form @onSubmit="handLeSubmit"></Form>
    <List @onRemove="handLeRemove" :items="notes"></List>
</template>

<script>
import Form from '@/components/Nodes/Form.vue';
import List from '@/components/Nodes/List.vue';
export default {
    components:{
        Form,
        List
    },

    data(){
        return{
             notes:["task1", "task1", "task2"],
        }
    },

    methods:{
        handLeSubmit(note){
            this.notes.push(note)
        },

        handLeRemove(index){
            this.notes.splice(index,1);
        }
    }
}
</script>