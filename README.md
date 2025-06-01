# site-reflexoes-desordem
"Site do livro Reflexões da Desordem"
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Galeria de Personagens: Reflexões da Desordem</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #111827; /* bg-gray-900 mais escuro */
            color: #e2e8f0; /* text-gray-200 */
        }
        .character-card {
            background-color: #1f2937; /* bg-gray-800 */
            border: 1px solid #374151; /* border-gray-700 */
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        .character-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.3), 0 0 15px rgba(239, 68, 68, 0.3); /* Sombra com tom avermelhado */
        }
        .image-placeholder {
            width: 100%;
            min-height: 300px;
            background-color: #374151;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 0.5rem;
            flex-grow: 1;
            overflow: hidden;
        }
        .character-image {
            max-width: 100%;
            height: auto;
            max-height: 400px;
            object-fit: cover;
            border-radius: 0.5rem;
            border: 2px solid #ef4444;
        }
        .full-description {
            font-size: 0.875rem;
            color: #d1d5db;
            margin-top: 0.75rem;
            white-space: pre-wrap;
            max-height: 200px;
            overflow-y: auto;
            background-color: #111827;
            padding: 0.5rem;
            border-radius: 0.375rem;
            border: 1px solid #374151;
        }
        .book-summary {
            background-color: #1f2937;
            padding: 2.5rem;
            border-radius: 1rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.4);
            margin-bottom: 3rem;
            border: 2px solid #ef4444;
            text-align: center;
        }
        .book-summary h2 {
            font-size: 2.5rem;
            font-weight: 900;
            color: #f87171;
            margin-bottom: 1.5rem;
            text-shadow: 1px 1px 4px rgba(0,0,0,0.6);
        }
        .book-summary p {
            font-size: 1.15rem;
            line-height: 1.8;
            color: #cbd5e1;
            max-width: 900px;
            margin-left: auto;
            margin-right: auto;
        }
        .pix-section {
            background-color: #ef4444;
            color: white;
            padding: 2rem;
            text-align: center;
            border-top: 5px solid #b91c1c;
            font-weight: bold;
            font-size: 1.1rem;
        }
        .pix-section p {
            margin-bottom: 1rem;
        }
        .pix-section .pix-key {
            background-color: #dc2626;
            padding: 0.75rem 1.5rem;
            border-radius: 0.5rem;
            display: inline-block;
            font-size: 1.3rem;
            letter-spacing: 1px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.3);
            word-break: break-all;
        }
        .pix-section .pix-info {
            font-size: 0.9rem;
            margin-top: 0.5rem;
            color: #fca5a5;
        }
    </style>
</head>
<body class="antialiased text-gray-200">

    <header class="py-10 text-center bg-gray-900 border-b-4 border-red-600">
        <div class="container mx-auto px-4">
            <h1 class="text-4xl md:text-5xl font-black text-red-500" style="text-shadow: 1px 1px 3px rgba(0,0,0,0.5);">Galeria de Personagens</h1>
            <p class="text-lg text-gray-400">Visualizações conceptuais para "Reflexões da Desordem"</p>
        </div>
    </header>

    <main class="container mx-auto px-4 py-8">
        <section id="book-summary-section" class="book-summary hidden"></section>

        <div id="gallery" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">
            </div>
    </main>

    <section id="pix-section-container" class="pix-section mt-12 hidden"></section>

    <footer class="bg-gray-900 border-t-2 border-gray-700 py-6 text-center">
        <p class="text-gray-500 text-sm">&copy; 2025 Erivelton Teixeira Ramos. Todos os direitos reservados.</p>
    </footer>

    <script>
        const projectData = {
            bookTitle: "Reflexões da Desordem",
            bookSummary: `
                Em um futuro distópico, onde a realidade se fragmenta e a sanidade é uma mercadoria rara, **"Reflexões da Desordem"** mergulha nas profundezas de uma cidade corroída pelo caos. Acompanhe Elias, um homem atormentado por visões premonitórias, enquanto ele tenta desvendar a verdade por trás do **"Chamado"**, uma força cósmica que distorce mentes e o próprio tecido da existência.

                Pela perspectiva de Arthur, o cronista da loucura, e Júlia, a sobrevivente do paradoxo, a narrativa explora os horrores de uma sociedade à beira do abismo, onde a única ordem que resta é a imposta pela brutal **Ordem da Cicatriz**. Uma jornada visceral por um mundo onde a luz se apaga e a escuridão revela as mais terríveis verdades sobre a natureza humana e cósmica. O mundo, agora, é um cemitério de estrelas em chamas, onde a esperança é uma memória distante e o sofrimento, a única certeza.

                A chegada do Sangue de Ne!lim trouxe não apenas a destruição, mas a revelação de que os horrores ocultos são parte da verdade, e a vida é uma dança macabra de dor e amor. Onde a beleza se esconde sob um véu de sofrimento, e a redenção se encontra nas chamas da agonia. Os horrores do passado ressurgiram, e cada lágrima derramada foi um feitiço, um chamado à existência dos antigos, um pacto selado em sangue e desejo. Quando a última estrela se apagou, o Sangue de Ne!lim regerá, reescrevendo as leis da criação, num ciclo interminável de dor e desespero. E no !m, quando tudo parecer perdido, quando as almas se tornarem ecos, um novo mundo surgirá das cinzas, marcado pelo toque profano do Ne!lim.
            `,
            pixKey: "cb432a73-18a0-4454-9639-de83b8c7d7a1",
            pixInfo: "Chave Pix: CPF (Erivelton Teixeira Ramos)",
            pixMessage: "Gostou do projeto \"Reflexões da Desordem\"? Sua ajuda é fundamental para continuar desenvolvendo este universo! Qualquer valor é bem-vindo e faz toda a diferença. Apoie o projeto via Pix:"
        };

        const characters = [
            {
                name: "Elias",
                shortDescription: "O visionário atormentado, preso entre mundos.",
                // IMAGEM AGORA APONTA PARA A PASTA 'imagens'
                imageUrl: "imagens/elias.jpg",
                longDescription: "Elias é um indivíduo que percebe fissuras na realidade antes que se tornem abismos. Constantemente assombrado por visões de um 'anjo' e pela sensação de um colapso iminente da sanidade e do mundo ao seu redor, ele tenta desvendar a verdade por trás do caos. Sua mente é um campo de batalha, onde cada dia é uma luta para discernir o que é real e o que é apenas uma projeção de sua própria perturbação. Ele é o protagonista do 'Eco do Vazio'."
            },
            {
                name: "Arthur",
                shortDescription: "O cronista da loucura, observador frio da brutalidade.",
                // IMAGEM AGORA APONTA PARA A PASTA 'imagens'
                imageUrl: "imagens/arthur.jpg",
                longDescription: "Arthur é moldado por uma brutalidade fria, buscando entender e registrar a insanidade. A sua mente é um laboratório de distorções, obcecado pelo sangue e por uma nova percepção da arte, tornando-se o cronista do horror. Ele documenta os eventos mais sombrios da cidade com uma frieza quase acadêmica, vendo a desordem como uma nova forma de ordem. Sua perspectiva é crucial para 'A Verdade Fragmentada'."
            },
            {
                name: "Júlia",
                shortDescription: "A sobrevivente do paradoxo, em busca de um eco de normalidade.",
                // IMAGEM AGORA APONTA PARA A PASTA 'imagens'
                imageUrl: "imagens/julia.jpg",
                longDescription: "Júlia é uma sobrevivente do abandono e do paradoxo, forçada a confrontar a deformidade do familiar. A sua realidade é um eco amplificado do colapso universal, lutando contra o peso do silêncio e a distorção da sua percepção. Ela busca desesperadamente por qualquer vestígio de normalidade em um mundo que perdeu o sentido, agarrando-se a memórias que podem não ser dela. Sua história é contada em 'A Distorção da Carne'."
            },
            {
                name: "Kael",
                shortDescription: "Líder implacável da Ordem da Cicatriz, psicopata calculista.",
                // IMAGEM AGORA APONTA PARA A PASTA 'imagens'
                imageUrl: "imagens/kael.jpg",
                longDescription: "Kael é o líder implacável da Ordem da Cicatriz, um homem de olhos gélidos e psicopatia calculista. Ele impõe medo e controla a cidade através da violência e da distribuição do 'Cristal da Loucura', uma substância que amplifica as visões e a desordem. Sua liderança é absoluta, baseada no terror e na promessa de uma nova era de caos. Ele representa a introdução brutal da Ordem."
            },
            {
                name: "Dante",
                shortDescription: "Tenente de Kael, o executor brutal da Ordem.",
                // IMAGEM AGORA APONTA PARA A PASTA 'imagens'
                imageUrl: "imagens/dante.jpg",
                longDescription: "Dante, ex-boxeador com um rosto marcado, é o braço armado e leal tenente de Kael. Conhecido pela sua ferocidade em combate e pela sua lealdade inabalável, ele é o executor das ordens mais sombrias da Ordem da Cicatriz. Sua brutalidade é lendária nas ruas, e poucos ousam desafiar sua presença imponente. Ele é a encarnação da violência emergente."
            },
            {
                name: "Klen (Representante)",
                shortDescription: "Um soldado da desordem, viciado e submisso.",
                // IMAGEM AGORA APONTA PARA A PASTA 'imagens'
                imageUrl: "imagens/klen.jpg",
                longDescription: "Os Klens são os soldados rasos de Kael, leais por medo, dependência do 'Cristal da Loucura' ou uma crença distorcida na nova ordem. Com cabelos coloridos e olhares vazios, eles vagam pelas ruas, alguns começando a sentir o 'Chamado' em primeira mão, encontrando um propósito distorcido na desordem que espalham. Este cartão representa a face genérica desses jovens perdidos que formam a milícia da Ordem."
            },
            {
                name: "Rainha das Sombras e Engano",
                shortDescription: "A Primeira Escolhida, mestra da manipulação e ilusões.",
                // IMAGEM AGORA APONTA PARA A PASTA 'imagens'
                imageUrl: "imagens/rainha.jpeg", // Notei que esta imagem é .jpeg
                longDescription: "A Rainha das Sombras e Engano é a Primeira Escolhida para reinar no apocalipse que se aproxima. Enigmática e poderosa, ela manipula as sombras e tece ilusões com uma destreza ancestral. Seu olhar penetrante sugere um conhecimento profundo de segredos cósmicos e um poder que pode facilmente quebrar ou moldar realidades. Ela é a personificação da manipulação e do terror sutil, um dos Deuses Abissais que retornam."
            },
        ];

        const gallery = document.getElementById('gallery');
        const bookSummarySection = document.getElementById('book-summary-section');
        const pixSectionContainer = document.getElementById('pix-section-container');

        function createCharacterCard(character) {
            const card = document.createElement('div');
            card.className = 'character-card p-4 md:p-6 rounded-lg shadow-xl flex flex-col';
            
            card.innerHTML = `
                <h3 class="text-2xl font-bold mb-2 text-red-400">${character.name}</h3>
                <p class="text-sm text-gray-400 mb-3">${character.shortDescription}</p>
                
                <div class="image-placeholder">
                    <img src="${character.imageUrl}" alt="Imagem de ${character.name}" class="character-image">
                </div>
                
                <div class="full-description">
                    <p>${character.longDescription}</p>
                </div>
            `;
            gallery.appendChild(card);
        }

        function populateBookSummary() {
            bookSummarySection.innerHTML = `
                <h2>Sobre "${projectData.bookTitle}"</h2>
                <p>${projectData.bookSummary}</p>
            `;
            bookSummarySection.classList.remove('hidden');
        }

        function populatePixSection() {
            pixSectionContainer.innerHTML = `
                <div class="container mx-auto px-4">
                    <p>${projectData.pixMessage}</p>
                    <p class="text-2xl mb-4"></p>
                    <div class="pix-key-container">
                        <span class="pix-key">${projectData.pixKey}</span>
                    </div>
                    <p class="pix-info">${projectData.pixInfo}</p>
                    <p class="pix-info">Muito obrigado pelo seu apoio!</p>
                </div>
            `;
            pixSectionContainer.classList.remove('hidden');
        }

        function initializePage() {
            populateBookSummary();
            characters.forEach(character => {
                createCharacterCard(character);
            });
            populatePixSection();
        }

        window.onload = initializePage;
    </script>
</body>
</html>
