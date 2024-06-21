<template>
	<div class="max-w-md mx-auto mt-10">
		<h1 class="text-2xl font-bold mb-5">Register</h1>
		<form @submit.prevent="register">
			<div class="mb-4">
				<label class="block mb-2">Name</label>
				<input v-model="name" type="text" class="border p-2 w-full" />
			</div>
			<div class="mb-4">
				<label class="block mb-2">Email</label>
				<input v-model="email" type="email" class="border p-2 w-full" />
			</div>
			<div class="mb-4">
				<label class="block mb-2">Password</label>
				<input v-model="password" type="password" class="border p-2 w-full" />
			</div>
			<div class="mb-4">
				<label class="block mb-2">Role</label>
				<select v-model="role" class="border p-2 w-full">
					<option value="buyer">Buyer</option>
					<option value="seller">Seller</option>
				</select>
			</div>
			<button type="submit" class="bg-blue-500 text-white p-2 w-full">
				Register
			</button>
		</form>
	</div>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const name = ref('');
const email = ref('');
const password = ref('');
const role = ref('buyer');
const router = useRouter();

const register = async () => {};
</script>
