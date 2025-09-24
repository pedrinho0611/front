<script setup>

const projetos = [
    {
        titulo: 'Calculadora Vue',
        descricao: 'Uma calculadora de investimentos cria por mim onde baicamente o Usuário pode ver quanto ele vai ganhar investindo.',
        link: 'https://github.com/pedrinho0611/investment-calculator'
    },
    {
        titulo: 'Ticket Sales System',
        descricao: 'Sistema de vendas de ingressos com gerenciamento de eventos e usuários.',
        link: 'https://github.com/pedrinho0611/-ticket-sales-system'
    }
]
</script>

<template>
    <div class="portfolio-container">
      
        <h1 class="portfolio-title">Pedro Rodrigues</h1>

       
    <img class="profile-img" src="../somativa/Captura de tela 2025-04-23 080651.png" alt="Foto de perfil" />

        
        <p class="portfolio-desc">Estudante de Desenvolvimento de Sistemas, gosto muito de praticar esportes como futebol, academia e correr.</p>

        
        <h2 class="section-title">Projetos</h2>
        <div class="projects-list">
            <div v-for="projeto in projetos" :key="projeto.titulo" class="project-card">
                <h3>{{ projeto.titulo }}</h3>
                <p>{{ projeto.descricao }}</p>
                <a :href="projeto.link" target="_blank" rel="noopener" class="project-link">Ver projeto</a>
            </div>
        </div>

       
        <h2 class="section-title">Contato</h2>
        <div class="contact-info">
            <p>Email: <a href="mailto:pedrohenrique@email.com">pedrorodrigues@email.com</a></p>
            <p>GitHub: <a href="https://github.com/pedrinho0611" target="_blank" rel="noopener">pedrinho0611</a></p>
        </div>
    </div>
</template>



<style scoped>
.portfolio-container {
    max-width: 600px;
    margin: 32px auto;
    padding: 24px;
    background: #ffffff;
    border-radius: 12px;
    box-shadow: 0 4px 24px rgba(0,0,0,0.08);
    text-align: center;
}
.portfolio-title {
    font-size: 2.2rem;
    margin-bottom: 8px;
    color: #1976d2;
}
.profile-img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 12px;
    border: 3px solid #1976d2;
}
.portfolio-desc {
    font-size: 1.1rem;
    color: #444;
    margin-bottom: 24px;
}
.section-title {
    font-size: 1.3rem;
    color: #333;
    margin: 24px 0 12px 0;
    border-bottom: 1px solid #ffffff;
    padding-bottom: 4px;
}
.projects-list {
    display: flex;
    flex-direction: column;
    gap: 16px;
    margin-bottom: 24px;
}
.project-card {
    background: #ffffff;
    border: 1.5px solid #1976d2;
    border-radius: 8px;
    padding: 16px;
    text-align: left;
    box-shadow: 0 2px 8px rgba(25, 118, 210, 0.07);
}
.project-card h3 {
    margin: 0 0 6px 0;
    color: #1976d2;
}
.project-link {
    color: #ffffff;
    background: #1976d2;
    padding: 4px 12px;
    border-radius: 4px;
    text-decoration: none;
    font-size: 0.98rem;
    transition: background 0.2s;
}
.project-link:hover {
    background: #125ea2;
}
.contact-info {
    margin-top: 8px;
    font-size: 1rem;
}
.contact-info a {
    color: #1976d2;
    text-decoration: underline;
}
</style>