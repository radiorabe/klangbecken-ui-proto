<template>
	<div class="warpper">
		<v-text-field
			v-model="test"
			label="Last Name"
			solo
		></v-text-field>
		{{test}}
	</div>
</template>

<script>
export default {
	name: "Search",
	data() {
		return {
				test: '',
		}
	}
}
</script>



