<template>
  <div class="note-from__wrapper">
    <form class="note-form" @submit.prevent="onSubmit">
        <textarea v-model="value" required placeholder="Type ur note"></textarea>
        <button class="btn btnPrimary" type="submit">Add new note</button>
    </form>
	</div>
</template>

<style scoped> 
.note-form{
	display: flex;
	flex-direction: column;
	max-width: 600px;
	width: 100%;
}

.note-from__wrapper{
	display: flex;
	flex-direction: column;
	align-items: center;
}
</style>

<script>
export default {
	data(){
		return{
			value:''
		}
	},

	methods:{
		onSubmit(){
			this.$emit('onSubmit', this.value)
			this.value = ''
		}
	}
}
</script>