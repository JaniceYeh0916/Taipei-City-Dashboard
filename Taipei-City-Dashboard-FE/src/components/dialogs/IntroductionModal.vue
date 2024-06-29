<script>
export default {
	name: 'IntroduceModal',
	props: {
		show: {
			type: Boolean,
			required: true
		}
	},
	emits: ['close'],
	methods: {
		closeModal() {
			this.$emit('close');
		}
	}
}
</script>

<template>
  <div
    v-if="show"
    class="modal-background"
    @click.self="closeModal"
  >
    <div class="modal-content">
      <h2>Introduce</h2>
      <p>This is the content of the modal.</p>
    </div>
  </div>
</template>
  
<style scoped lang="scss">
.modal-background {
	position: fixed;
	top: 0;
	left: 0;
	width: 100vw;
	height: 100vh;
	background-color: rgba(0, 0, 0, 0.5);
	display: flex;
	justify-content: center;
	align-items: center;
	z-index: 1000;
}
  
.modal-content {
	width: fit-content;
	height: fit-content;
	background-color: rgba(0, 0, 0, 0.5);
	padding: 20px;
	border-radius: 10px;
	overflow: auto;
}
</style>
  