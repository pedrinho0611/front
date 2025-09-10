
<template>
	<div class="card">
		<header class="card-header">
			<slot nome="header"></slot>
		</header>
		<main class="card-content">
			<slot></slot>
		</main>
		<footer class="card-footer">
			<slot nome="footer"></slot>
		</footer>
	</div>
</template>

<script setup>
// Nenhuma lógica extra necessária para slots nomeados
</script>

<style scoped>
.card {
	border: 1px solid #ccc;
	border-radius: 8px;
	padding: 16px;
	margin: 16px 0;
	background: #fafafa;
}
.card-header {
	font-weight: bold;
	margin-bottom: 8px;
}
.card-content {
	margin-bottom: 8px;
}
.card-footer {
	font-size: 0.95em;
	color: #666;
}
</style>
