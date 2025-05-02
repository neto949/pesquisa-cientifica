<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pichação vs Patrimônio Cultural</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #8B4513; /* Marrom terroso */
            --secondary: #E67E22; /* Laranja */
            --accent: #C0392B; /* Vermelho */
            --light: #F5F5F5;
            --dark: #333333;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
            color: var(--primary);
        }
        
        /* Header */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1591382386627-349b692688ff');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            padding: 0 2rem;
            margin-top: 70px;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: white;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #A5281B;
        }
        
        /* Stats Section */
        .stats {
            padding: 4rem 5%;
            background-color: white;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .stat-card {
            background-color: var(--light);
            padding: 2rem;
            border-radius: 8px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
        }
        
        .stat-card i {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 1rem;
        }
        
        .stat-card h3 {
            font-size: 2rem;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }
        
        /* Problem Section */
        .problem {
            padding: 4rem 5%;
            background-color: var(--light);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .section-title p {
            max-width: 700px;
            margin: 0 auto;
        }
        
        .comparison {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        @media (max-width: 768px) {
            .comparison {
                grid-template-columns: 1fr;
            }
        }
        
        .comparison-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        .comparison-card.grafite {
            border-top: 5px solid #27AE60;
        }
        
        .comparison-card.pichacao {
            border-top: 5px solid var(--accent);
        }
        
        .comparison-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
        
        .comparison-content {
            padding: 1.5rem;
        }
        
        .comparison-content h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }
        
        .comparison-content ul {
            list-style-position: inside;
            margin-bottom: 1rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 5%;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            text-align: left;
        }
        
        .footer-column h3 {
            color: white;
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 0.5rem;
        }
        
        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: white;
        }
        
        .copyright {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid #444;
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">Patrimônio Cultural</div>
            <div class="nav-links">
                <a href="#problem">O Problema</a>
                <a href="#difference">Diferenças</a>
                <a href="#impact">Impactos</a>
                <a href="#laws">Legislação</a>
                <a href="#solutions">Soluções</a>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Pichação vs Patrimônio Cultural</h1>
        <p>Como a depreciação do patrimônio cultural afeta nossas cidades e o que podemos fazer para proteger nossa história</p>
        <a href="#problem" class="btn">Saiba Mais</a>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="stats-container">
            <div class="stat-card">
                <i class="fas fa-money-bill-wave"></i>
                <h3>R$ 15 milhões</h3>
                <p>Gastos anualmente com limpeza e restauração</p>
            </div>
            <div class="stat-card">
                <i class="fas fa-landmark"></i>
                <h3>127</h3>
                <p>Monumentos tombados vandalizados em 2023</p>
            </div>
            <div class="stat-card">
                <i class="fas fa-chart-line"></i>
                <h3>42%</h3>
                <p>Aumento nas denúncias nos últimos 5 anos</p>
            </div>
        </div>
    </section>

    <!-- Problem Section -->
    <section class="problem" id="problem">
        <div class="section-title">
            <h2>O Problema da Pichação</h2>
            <p>A pichação compromete a integridade estética e histórica de bens culturais, resultando em sua depreciação e custos elevados de restauração</p>
        </div>
    </section>

    <!-- Difference Section -->
    <section class="difference" id="difference">
        <div class="section-title">
            <h2>Grafite vs Pichação</h2>
            <p>Entenda as diferenças fundamentais entre essas duas formas de intervenção urbana</p>
        </div>
        
        <div class="comparison">
            <div class="comparison-card grafite">
                <img src="https://images.unsplash.com/photo-1547354141-c3ab79215566" alt="Exemplo de grafite">
                <div class="comparison-content">
                    <h3>✅ Grafite</h3>
                    <ul>
                        <li>Expressão artística autorizada</li>
                        <li>Valoriza o espaço urbano</li>
                        <li>Planejamento e técnica</li>
                        <li>Reconhecido como arte urbana</li>
                        <li>Lei nº 12.408/2011</li>
                    </ul>
                </div>
            </div>
            
            <div class="comparison-card pichacao">
                <img src="https://images.unsplash.com/photo-1591382386627-349b692688ff" alt="Exemplo de pichação">
                <div class="comparison-content">
                    <h3>❌ Pichação</h3>
                    <ul>
                        <li>Atuação sem autorização</li>
                        <li>Deprecia o patrimônio</li>
                        <li>Marcas rápidas e ilegíveis</li>
                        <li>Considerada crime ambiental</li>
                        <li>Lei nº 9.605/98, Art. 65</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-column">
                <h3>Sobre o Projeto</h3>
                <p>Pesquisa acadêmica sobre os impactos da pichação no patrimônio cultural brasileiro.</p>
            </div>
            <div class="footer-column">
                <h3>Links Rápidos</h3>
                <ul>
                    <li><a href="#problem">O Problema</a></li>
                    <li><a href="#difference">Diferenças</a></li>
                    <li><a href="#impact">Impactos</a></li>
                    <li><a href="#laws">Legislação</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Contato</h3>
                <ul>
                    <li><i class="fas fa-envelope"></i> contato@patrimoniocultural.com</li>
                    <li><i class="fas fa-phone"></i> (11) 98765-4321</li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 Patrimônio Cultural. Todos os direitos reservados.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Animation for stat cards
        const statCards = document.querySelectorAll('.stat-card');
        
        const animateOnScroll = () => {
            statCards.forEach(card => {
                const cardPosition = card.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.3;
                
                if (cardPosition < screenPosition) {
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }
            });
        };
        
        // Set initial state
        statCards.forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'all 0.6s ease';
        });
        
        window.addEventListener('scroll', animateOnScroll);
        window.addEventListener('load', animateOnScroll);
    </script>
</body>
</html>
