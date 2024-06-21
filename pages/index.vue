<template>
	<div class="max-w-7xl mx-auto mt-10">
		<div class="flex justify-between items-center mb-8">
			<h1 class="text-3xl font-bold">Welcome to Our E-commerce Store</h1>
			<div>
				<nuxt-link to="/auth/login" class="text-blue-500 hover:underline mx-2"
					>Login</nuxt-link
				>
				<nuxt-link
					to="/auth/register"
					class="text-blue-500 hover:underline mx-2"
					>Register</nuxt-link
				>
			</div>
		</div>
		<div>
			<h2 class="text-2xl font-bold mb-4">Products</h2>
			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
				<div
					v-for="product in products"
					:key="product.id"
					class="border p-4 rounded"
				>
					<h3 class="text-xl font-semibold">{{ product.name }}</h3>
					<p class="text-gray-600">{{ product.description }}</p>
					<p class="text-green-600 font-bold">${{ product.price }}</p>
					<nuxt-link
						:to="`/products/${product.id}`"
						class="text-blue-500 hover:underline"
						>View Details</nuxt-link
					>
				</div>
			</div>
		</div>
	</div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const products = ref([]);
</script>
