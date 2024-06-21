<template>
	<div class="max-w-md mx-auto mt-10">
		<h1 class="text-2xl font-bold mb-5">Login</h1>
		<form @submit.prevent="login">
			<div class="mb-4">
				<label class="block mb-2">Email</label>
				<input v-model="email" type="email" class="border p-2 w-full" />
			</div>
			<div class="mb-4">
				<label class="block mb-2">Password</label>
				<input v-model="password" type="password" class="border p-2 w-full" />
			</div>
			<button type="submit" class="bg-blue-500 text-white p-2 w-full">
				Login
			</button>
		</form>
	</div>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const email = ref('');
const password = ref('');
const router = useRouter();

const login = async () => {
	try {
		router.push('/');
	} catch (error) {
		console.error('Login failed', error);
	}
};
</script>
