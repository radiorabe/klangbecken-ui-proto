<template>
	<div class="warpper">
		<input 
			type="text"
			class="search"
      v-model="search"
      placeholder="Search..."
		>
	</div>
</template>

<script>
export default {
  name: "Searctexth",
  props: ['list'],
	data() {
		return {
      search: '',
        
		}
  }, 
  computed: {
    filteredList() {
      return this.list.filter(post => {
        return post.title.toLowerCase().includes(this.search.toLowerCase())
      })
    }
  }
}
</script>

<style scoped>
.search{
  border-radius: 15px;
  background: rgba(210, 210, 210, 0.11);
  height: 30px;
  width: 50%;
  padding: 0 15px;
}
</style>




