<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ESSENTIALS | Fear of God Inspired</title>
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap" rel="stylesheet">
    <style>
        :root {
            --preto: #000;
            --branco: #FFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Bebas Neue', cursive;
        }

        body {
            background: var(--branco);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        header {
            background: var(--preto);
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            gap: 1rem;
        }

        .logo {
            color: var(--branco);
            font-size: 2.5rem;
            letter-spacing: 3px;
            flex-shrink: 0;
        }

        .search-bar {
            padding: 0.8rem;
            width: 100%;
            max-width: 400px;
            border: none;
            font-size: 1.1rem;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            align-items: center;
        }

        .nav-links a {
            color: var(--branco);
            text-decoration: none;
            font-size: 1.2rem;
            transition: opacity 0.3s;
        }

        .nav-links a:hover {
            opacity: 0.7;
        }

        main {
            flex: 1;
            margin-top: 80px;
            padding-bottom: 60px;
        }

        /* Estilos do Carrossel */
        .carousel {
            width: 100%;
            height: 70vh;
            position: relative;
            overflow: hidden;
        }

        .carousel-inner {
            width: 100%;
            height: 100%;
            display: flex;
            transition: transform 0.5s ease-in-out;
        }

        .carousel-item {
            min-width: 100%;
            height: 100%;
            position: relative;
        }

        .carousel-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            filter: grayscale(30%);
            transition: filter 0.3s;
        }

        .carousel-item:hover img {
            filter: grayscale(0);
        }

        .carousel-caption {
            position: absolute;
            bottom: 20%;
            left: 5%;
            color: var(--branco);
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .carousel-caption h2 {
            font-size: 4rem;
            margin-bottom: 1rem;
        }

        .carousel-control {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background: none;
            border: none;
            color: var(--branco);
            font-size: 3rem;
            cursor: pointer;
            opacity: 0.5;
            transition: opacity 0.3s;
        }

        .carousel-control:hover {
            opacity: 1;
        }

        .carousel-prev {
            left: 2rem;
        }

        .carousel-next {
            right: 2rem;
        }

        .carousel-indicators {
            position: absolute;
            bottom: 2rem;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 1rem;
        }

        .carousel-indicator {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: rgba(255,255,255,0.5);
            cursor: pointer;
            transition: all 0.3s;
        }

        .carousel-indicator.active {
            background: var(--branco);
            transform: scale(1.3);
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 2rem;
            margin-top: 2rem;
        }

        .product-card {
            text-align: center;
            padding: 1rem;
            border: 1px solid #eee;
        }

        .product-image {
            width: 100%;
            height: 400px;
            object-fit: cover;
            margin-bottom: 1rem;
        }

        footer {
            background: var(--preto);
            color: var(--branco);
            padding: 2rem;
            margin-top: auto;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .copyright {
            text-align: center;
            margin-top: 3rem;
            opacity: 0.5;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">ESSENTIALS</div>
        <input type="text" class="search-bar" placeholder="PESQUISAR PRODUTOS...">
        <nav class="nav-links">
            <a href="#" onclick="toggleLogin()">LOGIN</a>
            <a href="#" onclick="toggleCart()">CARRINHO (<span id="cart-count">0</span>)</a>
        </nav>
    </header>

    <main>
        <div class="carousel">
            <div class="carousel-inner">
                <div class="carousel-item">
                    <img src="https://images.unsplash.com/photo-1483985988355-763728e1935b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Coleção 1">
                    <div class="carousel-caption">
                        <h2>NOVA COLEÇÃO</h2>
                        <p>Descubra as peças essenciais para 2024</p>
                    </div>
                </div>
                <div class="carousel-item">
                    <img src="https://images.unsplash.com/photo-1543087903-1ac2ec7aa8c5?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Coleção 2">
                    <div class="carousel-caption">
                        <h2>ESTILO URBANO</h2>
                        <p>Conforto e sofisticação em cada detalhe</p>
                    </div>
                </div>
                <div class="carousel-item">
                    <img src="https://images.unsplash.com/photo-1529139574466-a303027c1d8b?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Coleção 3">
                    <div class="carousel-caption">
                        <h2>EDIÇÃO LIMITADA</h2>
                        <p>Peças exclusivas em estoque limitado</p>
                    </div>
                </div>
            </div>
            
            <button class="carousel-control carousel-prev" onclick="moveSlide(-1)">‹</button>
            <button class="carousel-control carousel-next" onclick="moveSlide(1)">›</button>
            
            <div class="carousel-indicators" id="carouselIndicators"></div>
        </div>

        <div class="products-grid"></div>
    </main>

    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h4>SOBRE</h4>
                <ul class="footer-links">
                    <li><a href="#">Nossa História</a></li>
                    <li><a href="#">Coleções</a></li>
                    <li><a href="#">Sustentabilidade</a></li>
                    <li><a href="#">Trabalhe Conosco</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h4>ATENDIMENTO</h4>
                <ul class="footer-links">
                    <li><a href="#">FAQ</a></li>
                    <li><a href="#">Trocas e Devoluções</a></li>
                    <li><a href="#">Entregas</a></li>
                    <li><a href="#">Contato</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h4>CONECTE-SE</h4>
                <div class="social-links">
                    <a href="#"><ion-icon name="logo-instagram"></ion-icon></a>
                    <a href="#"><ion-icon name="logo-twitter"></ion-icon></a>
                    <a href="#"><ion-icon name="logo-facebook"></ion-icon></a>
                </div>
            </div>
        </div>
        <div class="copyright">
            &copy; 2024 ALL BLACK FACTORY. Todos os direitos reservados.
        </div>
    </footer>


    <script type="module" src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"></script>
    <script nomodule src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>

    <script>
        // Carrossel
        let currentSlide = 0;
        const carouselInner = document.querySelector('.carousel-inner');
        const indicatorsContainer = document.getElementById('carouselIndicators');
        const totalSlides = document.querySelectorAll('.carousel-item').length;

        // Criar indicadores
        for(let i = 0; i < totalSlides; i++) {
            const indicator = document.createElement('div');
            indicator.classList.add('carousel-indicator');
            indicator.addEventListener('click', () => goToSlide(i));
            indicatorsContainer.appendChild(indicator);
        }

        function updateCarousel() {
            carouselInner.style.transform = `translateX(-${currentSlide * 100}%)`;
            document.querySelectorAll('.carousel-indicator').forEach((indicator, index) => {
                indicator.classList.toggle('active', index === currentSlide);
            });
        }

        function moveSlide(direction) {
            currentSlide = (currentSlide + direction + totalSlides) % totalSlides;
            updateCarousel();
            resetAutoplay();
        }

        function goToSlide(index) {
            currentSlide = index;
            updateCarousel();
            resetAutoplay();
        }

        // Autoplay
        let autoplayInterval = setInterval(() => moveSlide(1), 5000);

        function resetAutoplay() {
            clearInterval(autoplayInterval);
            autoplayInterval = setInterval(() => moveSlide(1), 5000);
        }

        // Pausar autoplay ao interagir
        document.querySelector('.carousel').addEventListener('mouseenter', () => {
            clearInterval(autoplayInterval);
        });

        document.querySelector('.carousel').addEventListener('mouseleave', () => {
            autoplayInterval = setInterval(() => moveSlide(1), 5000);
        });

        // Inicializar
        updateCarousel();

        // Produtos
        const products = [
            {
                id: 1,
                name: "Hoodie Essentials",
                price: 799.90,
                image: "https://via.placeholder.com/400x500/EEE?text=HOODIE",
                rating: 4
            },
            {
                id: 2,
                name: "T-Shirt Oversized",
                price: 349.90,
                image: "https://via.placeholder.com/400x500/EEE?text=T-SHIRT",
                rating: 5
            },
            {
                id: 3,
                name: "Sweatpants Jogger",
                price: 599.90,
                image: "https://via.placeholder.com/400x500/EEE?text=SWEATPANTS",
                rating: 4
            }
        ];

        function initProducts() {
            const grid = document.querySelector('.products-grid');
            grid.innerHTML = products.map(product => `
                <div class="product-card">
                    <img src="${product.image}" class="product-image" alt="${product.name}">
                    <h3>${product.name}</h3>
                    <div class="price">R$ ${product.price.toFixed(2).replace('.', ',')}</div>
                    <button class="cart-btn" onclick="addToCart(${product.id})">ADICIONAR AO CARRINHO</button>
                </div>
            `).join('');
        }

        initProducts();

        // Carrinho
        let cart = JSON.parse(localStorage.getItem('cart')) || [];
        
        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            cart.push({...product, quantity: 1});
            updateCart();
            showAlert(`${product.name} adicionado ao carrinho`);
        }

        function updateCart() {
            localStorage.setItem('cart', JSON.stringify(cart));
            document.getElementById('cart-count').textContent = cart.length;
        }

        function showAlert(message) {
            const alert = document.createElement('div');
            alert.textContent = message;
            alert.style.position = 'fixed';
            alert.style.bottom = '20px';
            alert.style.right = '20px';
            alert.style.background = 'var(--preto)';
            alert.style.color = 'var(--branco)';
            alert.style.padding = '1rem 2rem';
            alert.style.borderRadius = '4px';
            document.body.appendChild(alert);
            
            setTimeout(() => {
                alert.remove();
            }, 3000);
        }
    </script>
</body>
</html>
