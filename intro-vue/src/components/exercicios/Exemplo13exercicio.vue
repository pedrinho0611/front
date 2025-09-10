
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
/* Card principal */
.card {
	border: 2px solid #1976d2;
	border-radius: 16px;
	box-shadow: 0 4px 16px rgba(25, 118, 210, 0.12);
	padding: 32px 24px;
	margin: 32px auto;
	background: linear-gradient(135deg, #e3f2fd 0%, #fff 100%);
	max-width: 400px;
	transition: box-shadow 0.2s;
}
.card:hover {
	box-shadow: 0 8px 32px rgba(25, 118, 210, 0.18);
}

/* Cabeçalho */
.card-header {
	font-weight: bold;
	font-size: 1.5rem;
	color: #fff;
	background: linear-gradient(90deg, #1976d2 60%, #42a5f5 100%);
	padding: 16px;
	border-radius: 12px 12px 0 0;
	box-shadow: 0 2px 8px rgba(25, 118, 210, 0.10);
	margin-bottom: 16px;
	text-align: center;
	letter-spacing: 1px;
}

/* Conteúdo principal */
.card-content {
	font-size: 1.1rem;
	color: #333;
	margin-bottom: 16px;
	text-align: center;
}

/* Rodapé */
.card-footer {
	font-size: 1rem;
	color: #fff;
	background: linear-gradient(90deg, #42a5f5 0%, #1976d2 100%);
	padding: 12px;
	border-radius: 0 0 12px 12px;
	box-shadow: 0 -2px 8px rgba(25, 118, 210, 0.08);
	text-align: center;
	margin-top: 8px;
	letter-spacing: 0.5px;
}
</style>
