<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saman Lancei service</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Définition de la police Inter pour tout le corps du document */
        body {
            font-family: 'Inter', sans-serif;
        }
        /* Styles pour les couleurs arc-en-ciel du logo et du titre */
        .rainbow-text .char {
            display: inline-block;
            /* Couleurs arc-en-ciel */
            /* Ces couleurs sont appliquées via JavaScript ou manuellement pour chaque span */
        }
        /* Style pour les étoiles */
        .star-rating .star {
            color: #ccc; /* Couleur par default des étoiles non remplies */
            cursor: pointer;
            transition: color 0.2s;
        }
        .star-rating .star.filled {
            color: #FFD700; /* Couleur des étoiles remplies (or) */
        }
        /* Style pour les questions/réponses de la FAQ */
        .faq-item {
            border-bottom: 1px solid #e2e8f0; /* gray-200 */
        }
        .faq-question {
            cursor: pointer;
            padding: 1rem 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 600;
            color: #1a202c; /* gray-900 */
        }
        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            padding: 0 1rem;
            color: #4a5568; /* gray-700 */
        }
        .faq-answer.open {
            max-height: 200px; /* Ajustez si le contenu est plus long */
            transition: max-height 0.5s ease-in;
            padding-bottom: 1rem;
        }
        .faq-question svg {
            transition: transform 0.3s ease-out;
        }
        .faq-question.active svg {
            transform: rotate(180deg);
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-900 flex flex-col min-h-screen">

    <header class="bg-gradient-to-r from-blue-700 to-blue-500 text-white p-4 shadow-xl rounded-b-xl">
        <div class="container mx-auto flex flex-col sm:flex-row justify-between items-center">
            <div class="text-center sm:text-left mb-4 sm:mb-0">
                <div id="logo-slkk" class="text-5xl font-extrabold tracking-wider rainbow-text">
                    <span class="char" style="color: #FF0000;">S</span><span class="char" style="color: #FF7F00;">L</span><span class="char" style="color: #FFFF00;">K</span><span class="char" style="color: #00FF00;">K</span>
                </div>
                <div id="logo-saman" class="text-lg sm:text-xl font-semibold mt-1 rainbow-text">
                    <span class="char" style="color: #0000FF;">S</span><span class="char" style="color: #4B0082;">a</span><span class="char" style="color: #9400D3;">m</span><span class="char" style="color: #FF0000;">a</span><span class="char" style="color: #FF7F00;">n</span>
                    <span class="char" style="color: #FFFF00;">L</span><span class="char" style="color: #00FF00;">a</span><span class="char" style="color: #0000FF;">n</span><span class="char" style="color: #4B0082;">c</span><span class="char" style="color: #9400D3;">e</span><span class="char" style="color: #FF0000;">i</span>
                    <span class="char" style="color: #FF7F00;">K</span><span class="char" style="color: #FFFF00;">a</span><span class="char" style="color: #00FF00;">b</span><span class="char" style="color: #0000FF;">a</span>
                    <span class="char" style="color: #4B0082;">K</span><span class="char" style="color: #9400D3;">e</span><span class="char" style="color: #FF0000;">i</span><span class="char" style="color: #FF7F00;">t</span><span class="char" style="color: #FFFF00;">a</span>
                </div>
                <h1 class="text-3xl font-bold mt-2 rainbow-text">
                    <span class="char" style="color: #FF0000;">S</span><span class="char" style="color: #FF7F00;">a</span><span class="char" style="color: #FFFF00;">m</span><span class="char" style="color: #00FF00;">a</span><span class="char" style="color: #0000FF;">n</span>
                    <span class="char" style="color: #4B0082;">L</span><span class="char" style="color: #9400D3;">a</span><span class="char" style="color: #FF0000;">n</span><span class="char" style="color: #FF7F00;">c</span><span class="char" style="color: #FFFF00;">e</span><span class="char" style="color: #00FF00;">i</span>
                    <span class="char" style="color: #0000FF;">s</span><span class="char" style="color: #4B0082;">e</span><span class="char" style="color: #9400D3;">r</span><span class="char" style="color: #FF0000;">v</span><span class="char" style="color: #FF7F00;">i</span><span class="char" style="color: #FFFF00;">c</span><span class="char" style="color: #00FF00;">e</span>
                </h1>
            </div>
            <nav>
                <ul class="flex space-x-4 mt-4 sm:mt-0 text-lg">
                    <li><a href="#" class="hover:text-blue-200 transition-colors duration-300">Accueil</a></li>
                    <li><a href="#" class="hover:text-blue-200 transition-colors duration-300">À Propos</a></li>
                    <li><a href="#" class="hover:text-blue-200 transition-colors duration-300">Services</a></li>
                    <li><a href="#contact" class="hover:text-blue-200 transition-colors duration-300">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main class="container mx-auto p-4 flex-grow">
        <section class="bg-gradient-to-br from-blue-50 to-indigo-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-4xl font-extrabold text-blue-800 mb-6 leading-tight">Notre Mission</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto">
                « Notre mission, au sein de cet atelier d'infographie à Conakry, est de **doter les individus et les organisations des compétences et des outils nécessaires pour transformer des données complexes en récits visuels clairs, percutants et engageants.** Nous nous engageons à démocratiser la création d'infographies de qualité professionnelle, favorisant ainsi une meilleure communication, une prise de décision éclairée et une diffusion efficace de l'information au sein de la communauté et au-delà. »
            </p>
            <button class="mt-8 bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                Découvrir nos solutions
            </button>
        </section>

        <section class="bg-green-500 text-white p-5 rounded-xl shadow-lg mb-8 text-center">
            <h3 class="text-2xl font-bold mb-2">Disponibilité 24h/24</h3>
            <p class="text-xl">Nous sommes là pour vous, à tout moment, jour et nuit ! Votre satisfaction est notre priorité.</p>
        </section>

        <section class="bg-yellow-500 text-white p-5 rounded-xl shadow-lg mb-8 text-center">
            <h3 class="text-2xl font-bold mb-2">Livraison Partout en Guinée</h3>
            <p class="text-xl">Où que vous soyez en Guinée, nous livrons nos services directement à votre porte !</p>
        </section>

        <section class="bg-white p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-blue-700 mb-8 text-center">Notre Processus de Travail</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 text-center">
                <div class="p-4 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                    <div class="text-4xl font-bold text-blue-500 mb-3">1</div>
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Prise de Contact</h3>
                    <p class="text-gray-700 text-sm">Discutons de vos besoins et de vos idées pour votre projet.</p>
                </div>
                <div class="p-4 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                    <div class="text-4xl font-bold text-blue-500 mb-3">2</div>
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Conception & Validation</h3>
                    <p class="text-gray-700 text-sm">Nous créons un design initial et le soumettons pour votre approbation.</p>
                </div>
                <div class="p-4 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                    <div class="text-4xl font-bold text-blue-500 mb-3">3</div>
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Production</h3>
                    <p class="text-gray-700 text-sm">Une fois validé, nous passons à la réalisation de votre commande.</p>
                </div>
                <div class="p-4 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                    <div class="text-4xl font-bold text-blue-500 mb-3">4</div>
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Livraison</h3>
                    <p class="text-gray-700 text-sm">Votre commande est livrée rapidement et en toute sécurité, partout en Guinée.</p>
                </div>
            </div>
        </section>

        <section class="bg-white p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-blue-700 mb-6">Nos Compétences</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="p-4 rounded-lg bg-blue-50 border border-blue-100 shadow-sm">
                    <h3 class="text-2xl font-semibold text-blue-600 mb-2">Fiabilité</h3>
                    <p class="text-gray-700">Des résultats constants et de haute qualité sur lesquels vous pouvez compter.</p>
                </div>
                <div class="p-4 rounded-lg bg-green-50 border border-green-100 shadow-sm">
                    <h3 class="text-2xl font-semibold text-green-600 mb-2">Rapidité</h3>
                    <p class="text-gray-700">Des délais de livraison optimisés sans compromettre la qualité de notre travail.</p>
                </div>
                <div class="p-4 rounded-lg bg-purple-50 border border-purple-100 shadow-sm">
                    <h3 class="text-2xl font-semibold text-purple-600 mb-2">Performance</h3>
                    <p class="text-700">Des solutions efficaces qui génèrent un impact réel et mesurable pour votre projet.</p>
                </div>
            </div>
        </section>

        <section class="bg-white p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-blue-700 mb-8 text-center">Nos Services</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="bg-gray-50 p-6 rounded-xl shadow-md border border-gray-100 hover:shadow-lg hover:border-blue-300 transition-all duration-300 transform hover:-translate-y-1">
                    <h3 class="text-2xl font-semibold text-blue-600 mb-3">Décoration personnalisée</h3>
                    <p class="text-gray-700 leading-relaxed">Décoration de maillots, képis et t-shirts pour un style unique et percutant.</p>
                </div>
                <div class="bg-gray-50 p-6 rounded-xl shadow-md border border-gray-100 hover:shadow-lg hover:border-blue-300 transition-all duration-300 transform hover:-translate-y-1">
                    <h3 class="text-2xl font-semibold text-blue-600 mb-3">Confection de Banderoles</h3>
                    <p class="text-gray-700 leading-relaxed">Création et confection de banderoles sur mesure pour vos événements et promotions.</p>
                </div>
                <div class="bg-gray-50 p-6 rounded-xl shadow-md border border-gray-100 hover:shadow-lg hover:border-blue-300 transition-all duration-300 transform hover:-translate-y-1">
                    <h3 class="text-2xl font-semibold text-blue-600 mb-3">Création de Logos</h3>
                    <p class="text-gray-700 leading-relaxed">Conception de logos professionnels et mémorables pour renforcer votre identité visuelle.</p>
                </div>
            </div>
        </section>

        <section class="bg-gradient-to-br from-indigo-50 to-blue-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-indigo-800 mb-6">Communication High-Tech (HTC)</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Explorez nos solutions de communication numérique et de services high-tech.
                Nous vous aidons à optimiser votre présence en ligne et à interagir efficacement avec votre audience.
            </p>
            <button class="mt-4 bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                Découvrir les solutions HTC
            </button>
        </section>

        <section class="bg-white p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-blue-700 mb-8 text-center">Nos Réalisations</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-064af053-02ab-4de6-843d-1321bf6edc2e" alt="Carte de faire-part de mariage" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Carte de faire-part</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-caf6a116-6397-4ccc-b499-9dcd1a6b82c1" alt="T-shirt ADER Association" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">T-shirt ADER</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-0a25da61-314d-4377-aa76-83e9076aa2ba" alt="Affiche Excursion Groupe Scolaire Bill-Clinton" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Excursion Scolaire</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-011a1566-ea61-4a92-8b0f-d932d273875f" alt="Maillot de sport CAMAVINGA 11" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Maillot Camavinga</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-4f97627d-d210-45cb-84fe-ee484c56640b" alt="T-shirt BANKAN avec arbre" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">T-shirt Bankan</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-c1f9a1a7-dbcb-432f-81f8-c699e4dacbfc" alt="Maillot de sport ZABALE KONKON 14" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Maillot Zabale Konkon</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-62737abd-56f7-4f53-a3b8-d80f7383ad74" alt="Groupe de personnes en T-shirt d'équipe" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Équipe en T-shirts</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-f9c0341d-85a2-400a-9fc9-3754a514c6c5" alt="Maillot de sport MOHAMED CAMARA 13" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Maillot Mohamed Camara</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-1fb69d64-2c49-45e9-b966-36c858510aa1" alt="Maillot de sport ESP. POPCAN" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Maillot ESP. POPCAN</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-55e6dcc1-0b0e-4aef-abcb-837ae5aff3b6" alt="Publicité S22 Ultra Samanla" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Publicité S22 Ultra</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-gradient-to-br from-red-50 to-orange-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-red-800 mb-6">Vidéo de Publicité</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Découvrez nos services en action ! Regardez notre vidéo promotionnelle pour en savoir plus sur ce que nous faisons.
            </p>
            <div class="relative w-full max-w-2xl mx-auto" style="padding-bottom: 56.25%;">
                <iframe
                    class="absolute top-0 left-0 w-full h-full rounded-xl shadow-lg"
                    src="https://www.youtube.com/embed/dQw4w9WgXcQ"  title="Vidéo de Publicité Saman Lancei service"
                    frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
            <p class="text-sm text-gray-500 mt-4">
                *Veuillez remplacer le lien de la vidéo ci-dessus par le lien de votre propre vidéo YouTube, Vimeo ou autre plateforme d'hébergement.
            </p>
        </section>

        <section class="bg-gradient-to-br from-purple-50 to-pink-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-purple-800 mb-6">Vos Avis et Satisfaction</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Votre opinion est précieuse pour nous ! Partagez votre expérience et votre degré de satisfaction avec nos services.
                Vos retours nous aident à nous améliorer continuellement.
            </p>
            <button class="mt-4 bg-purple-600 hover:bg-purple-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                Donner votre avis
            </button>
        </section>

        <section class="bg-gradient-to-br from-teal-50 to-green-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-teal-800 mb-6">Confirmation de Réception</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Nous sommes ravis d'apprendre que vous avez bien reçu votre colis !
                Votre satisfaction est notre plus grande récompense. N'hésitez pas à nous faire part de vos impressions.
            </p>
            <button class="mt-4 bg-teal-600 hover:bg-teal-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                Confirmer la réception
            </button>
        </section>

        <section class="bg-gradient-to-br from-yellow-50 to-orange-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-orange-800 mb-6">Évaluez notre Service</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Combien d'étoiles nous donneriez-vous pour votre expérience globale ?
            </p>
            <div class="star-rating text-5xl flex justify-center space-x-2">
                <span class="star" data-value="1">★</span>
                <span class="star" data-value="2">★</span>
                <span class="star" data-value="3">★</span>
                <span class="star" data-value="4">★</span>
                <span class="star" data-value="5">★</span>
            </div>
            <p id="rating-message" class="mt-4 text-lg text-gray-600">Cliquez sur les étoiles pour évaluer !</p>
        </section>

        <section class="bg-gradient-to-br from-blue-50 to-purple-50 p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-blue-800 mb-8 text-center">Ce que nos clients disent de nous</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-white p-6 rounded-xl shadow-md border border-blue-100">
                    <p class="text-gray-700 italic mb-4">"Service exceptionnel ! La décoration de nos maillots a dépassé toutes nos attentes. Rapidité et qualité au rendez-vous. Nous recommandons vivement Saman Lancei service."</p>
                    <p class="font-semibold text-blue-600">- Client satisfait 1</p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md border border-purple-100">
                    <p class="text-gray-700 italic mb-4">"Nous avons commandé des banderoles pour notre événement et le résultat était parfait. L'équipe est très professionnelle et la livraison a été effectuée dans les temps. Bravo !"</p>
                    <p class="font-semibold text-purple-600">- Client satisfait 2</p>
                </div>
                </div>
        </section>

        <section class="bg-gradient-to-br from-blue-100 to-cyan-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-blue-800 mb-6">Passez Vos Commandes</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Prêt à transformer vos idées en réalité ? Contactez-nous dès aujourd'hui pour discuter de votre projet et passer commande.
                Notre équipe est à votre écoute pour vous offrir un service personnalisé et de qualité.
            </p>
            <a href="#contact" class="mt-4 bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1 inline-block">
                Contacter pour commander
            </a>
        </section>

        <section class="bg-gray-100 p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Foire Aux Questions (FAQ)</h2>
            <div class="max-w-3xl mx-auto">
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Quels sont vos délais de livraison ?</span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-down"><path d="m6 9 6 6 6-6"/></svg>
                    </div>
                    <div class="faq-answer">
                        <p>Nos délais de livraison varient en fonction de la complexité du projet et de la quantité commandée. Nous nous efforçons de livrer dans les plus brefs délais, généralement entre 3 et 7 jours ouvrables après validation de la conception.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Proposez-vous des maquettes avant la production ?</span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-down"><path d="m6 9 6 6 6-6"/></svg>
                    </div>
                    <div class="faq-answer">
                        <p>Oui, absolument ! Pour la plupart de nos services, nous fournissons des maquettes numériques ou physiques pour validation avant de lancer la production finale, afin de garantir votre entière satisfaction.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Puis-je commander en grande quantité ?</span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-down"><path d="m6 9 6 6 6-6"/></svg>
                    </div>
                    <div class="faq-answer">
                        <p>Oui, nous acceptons les commandes en grande quantité et nous pouvons discuter de tarifs préférentiels pour les volumes importants. Contactez-nous pour un devis personnalisé.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Comment puis-je suivre ma commande ?</span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-down"><path d="m6 9 6 6 6-6"/></svg>
                    </div>
                    <div class="faq-answer">
                        <p>Une fois votre commande confirmée et la production lancée, nous vous tiendrons informé de son avancement. Pour les livraisons, un numéro de suivi pourra vous être fourni si applicable.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-gradient-to-br from-gray-100 to-gray-200 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-gray-800 mb-6">Rechercher sur Google</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Vous avez une question spécifique ou souhaitez trouver plus d'informations ?
                Utilisez le moteur de recherche Google directement depuis notre site.
            </p>
            <form action="https://www.google.com/search" method="get" target="_blank" class="flex flex-col sm:flex-row items-center justify-center space-y-4 sm:space-y-0 sm:space-x-4 max-w-xl mx-auto">
                <input
                    type="text"
                    name="q"
                    placeholder="Rechercher sur Google..."
                    class="w-full sm:w-2/3 p-3 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                >
                <button
                    type="submit"
                    class="w-full sm:w-1/3 bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-6 rounded-lg shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-0.5"
                >
                    Rechercher
                </button>
            </form>
        </section>


        <section id="contact" class="bg-gradient-to-br from-green-50 to-teal-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-green-800 mb-6">Contactez-nous</h2>
            <div class="text-xl text-gray-700 leading-relaxed max-w-2xl mx-auto flex flex-col items-center">
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-mail mr-2 text-blue-600"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
                    <span class="font-semibold">Email :</span> <a href="mailto:klancei064@gmail.com" class="text-blue-600 hover:underline ml-1">klancei064@gmail.com</a>
                </p>
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-map-pin mr-2 text-blue-600"><path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/></svg>
                    <span class="font-semibold">Adresse :</span> Conakry/Gbessia
                </p>
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-phone mr-2 text-blue-600"><path d="M22 16.92v3a2 2 0 0 1-2.18 2.02 15.15 15.15 0 0 1-12.62-6.38A15.15 15.15 0 0 1 2.02 4.18 2 2 0 0 1 4 2h3a2 2 0 0 1 2 2.18 10.15 10.15 0 0 0 2.4 7.22 10.15 10.15 0 0 0 7.22 2.4A2 2 0 0 1 22 16.92z"/></svg>
                    <span class="font-semibold">Téléphone :</span> <a href="tel:+224625850315" class="text-blue-600 hover:underline ml-1">625 85 03 15</a>
                </p>
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-message-circle mr-2 text-green-600"><path d="M7.9 20A9 9 0 1 0 4 16.1L2 22Z"/></svg>
                    <span class="font-semibold">WhatsApp :</span> <a href="https://wa.me/224662218429" target="_blank" rel="noopener noreferrer" class="text-green-600 hover:underline ml-1">662 21 84 29</a>
                </p>
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-globe mr-2 text-gray-600"><circle cx="12" cy="12" r="10"/><path d="M12 2a14.5 14.5 0 0 0 0 20 14.5 14.5 0 0 0 0-20"/><path d="M2 12h20"/></svg>
                    <span class="font-semibold">Site Web :</span> <a href="http://SamanLancei.service.com" target="_blank" rel="noopener noreferrer" class="text-blue-600 hover:underline ml-1">SamanLancei.service.com</a>
                </p>
                <div class="flex space-x-6 mt-4">
                    <a href="https://www.facebook.com/SamanLancei" target="_blank" rel="noopener noreferrer" class="text-blue-700 hover:text-blue-900 transition-colors duration-300">
                        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" fill="currentColor" stroke="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-facebook"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
                        <span class="sr-only">Page Facebook Saman Lancei</span>
                    </a>
                    <a href="https://www.instagram.com/Samanlancei" target="_blank" rel="noopener noreferrer" class="text-pink-600 hover:text-pink-800 transition-colors duration-300">
                        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucude-instagram"><rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.5" y1="6.5" y2="6.5"/></svg>
                        <span class="sr-only">Page Instagram Samanlancei</span>
                    </a>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-gray-900 text-gray-300 p-6 mt-12 rounded-t-xl">
        <div class="container mx-auto text-center text-sm">
            <p>© 2025 Mon Super Site Web. Tous droits réservés.</p>
            <p class="mt-3">
                <a href="#" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a> |
                <a href="#" class="hover:text-white transition-colors duration-300">Conditions d'utilisation</a>
            </p>
        </div>
    </footer>

    <script>
        // JavaScript pour la fonctionnalité d'évaluation par étoiles
        document.addEventListener('DOMContentLoaded', () => {
            const stars = document.querySelectorAll('.star-rating .star');
            const ratingMessage = document.getElementById('rating-message');

            stars.forEach(star => {
                star.addEventListener('click', () => {
                    const value = parseInt(star.dataset.value);
                    // Remplir les étoiles jusqu'à la valeur sélectionnée
                    stars.forEach((s, index) => {
                        if (index < value) {
                            s.classList.add('filled');
                        } else {
                            s.classList.remove('filled');
                        }
                    });
                    ratingMessage.textContent = `Vous avez donné ${value} étoile(s) ! Merci pour votre avis.`;
                });

                star.addEventListener('mouseover', () => {
                    const value = parseInt(star.dataset.value);
                    stars.forEach((s, index) => {
                        if (index < value) {
                            s.classList.add('filled');
                        } else {
                            s.classList.remove('filled');
                        }
                    });
                });

                star.addEventListener('mouseout', () => {
                    // Réinitialiser les étoiles si aucune n'est cliquée
                    let clickedValue = 0;
                    stars.forEach(s => {
                        if (s.classList.contains('filled')) {
                            clickedValue = Math.max(clickedValue, parseInt(s.dataset.value));
                        }
                    });

                    if (clickedValue === 0) {
                        stars.forEach(s => s.classList.remove('filled'));
                        ratingMessage.textContent = 'Cliquez sur les étoiles pour évaluer !';
                    } else {
                        stars.forEach((s, index) => {
                            if (index < clickedValue) {
                                s.classList.add('filled');
                            } else {
                                s.classList.remove('filled');
                            }
                        });
                    }
                });
            });

            // JavaScript pour la fonctionnalité de la FAQ (accordeon)
            const faqQuestions = document.querySelectorAll('.faq-question');

            faqQuestions.forEach(question => {
                question.addEventListener('click', () => {
                    const answer = question.nextElementSibling;
                    const isActive = question.classList.contains('active');

                    // Fermer toutes les autres réponses
                    faqQuestions.forEach(q => {
                        if (q !== question && q.classList.contains('active')) {
                            q.classList.remove('active');
                            q.nextElementSibling.classList.remove('open');
                            q.nextElementSibling.style.maxHeight = null;
                        }
                    });

                    // Ouvrir ou fermer la réponse cliquée
                    if (isActive) {
                        question.classList.remove('active');
                        answer.classList.remove('open');
                        answer.style.maxHeight = null;
                    } else {
                        question.classList.add('active');
                        answer.classList.add('open');
                        answer.style.maxHeight = answer.scrollHeight + "px"; // Ajuste la hauteur de la réponse
                    }
                });
            });
        });
    </script>
</body>
</html>


<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saman Lancei service</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Définition de la police Inter pour tout le corps du document */
        body {
            font-family: 'Inter', sans-serif;
        }
        /* Styles pour les couleurs arc-en-ciel du logo et du titre */
        .rainbow-text .char {
            display: inline-block;
            /* Couleurs arc-en-ciel */
            /* Ces couleurs sont appliquées via JavaScript ou manuellement pour chaque span */
        }
        /* Style pour les étoiles */
        .star-rating .star {
            color: #ccc; /* Couleur par default des étoiles non remplies */
            cursor: pointer;
            transition: color 0.2s;
        }
        .star-rating .star.filled {
            color: #FFD700; /* Couleur des étoiles remplies (or) */
        }
        /* Style pour les questions/réponses de la FAQ */
        .faq-item {
            border-bottom: 1px solid #e2e8f0; /* gray-200 */
        }
        .faq-question {
            cursor: pointer;
            padding: 1rem 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 600;
            color: #1a202c; /* gray-900 */
        }
        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            padding: 0 1rem;
            color: #4a5568; /* gray-700 */
        }
        .faq-answer.open {
            max-height: 200px; /* Ajustez si le contenu est plus long */
            transition: max-height 0.5s ease-in;
            padding-bottom: 1rem;
        }
        .faq-question svg {
            transition: transform 0.3s ease-out;
        }
        .faq-question.active svg {
            transform: rotate(180deg);
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-900 flex flex-col min-h-screen">

    <header class="bg-gradient-to-r from-blue-700 to-blue-500 text-white p-4 shadow-xl rounded-b-xl">
        <div class="container mx-auto flex flex-col sm:flex-row justify-between items-center">
            <div class="text-center sm:text-left mb-4 sm:mb-0">
                <div id="logo-slkk" class="text-5xl font-extrabold tracking-wider rainbow-text">
                    <span class="char" style="color: #FF0000;">S</span><span class="char" style="color: #FF7F00;">L</span><span class="char" style="color: #FFFF00;">K</span><span class="char" style="color: #00FF00;">K</span>
                </div>
                <div id="logo-saman" class="text-lg sm:text-xl font-semibold mt-1 rainbow-text">
                    <span class="char" style="color: #0000FF;">S</span><span class="char" style="color: #4B0082;">a</span><span class="char" style="color: #9400D3;">m</span><span class="char" style="color: #FF0000;">a</span><span class="char" style="color: #FF7F00;">n</span>
                    <span class="char" style="color: #FFFF00;">L</span><span class="char" style="color: #00FF00;">a</span><span class="char" style="color: #0000FF;">n</span><span class="char" style="color: #4B0082;">c</span><span class="char" style="color: #9400D3;">e</span><span class="char" style="color: #FF0000;">i</span>
                    <span class="char" style="color: #FF7F00;">K</span><span class="char" style="color: #FFFF00;">a</span><span class="char" style="color: #00FF00;">b</span><span class="char" style="color: #0000FF;">a</span>
                    <span class="char" style="color: #4B0082;">K</span><span class="char" style="color: #9400D3;">e</span><span class="char" style="color: #FF0000;">i</span><span class="char" style="color: #FF7F00;">t</span><span class="char" style="color: #FFFF00;">a</span>
                </div>
                <h1 class="text-3xl font-bold mt-2 rainbow-text">
                    <span class="char" style="color: #FF0000;">S</span><span class="char" style="color: #FF7F00;">a</span><span class="char" style="color: #FFFF00;">m</span><span class="char" style="color: #00FF00;">a</span><span class="char" style="color: #0000FF;">n</span>
                    <span class="char" style="color: #4B0082;">L</span><span class="char" style="color: #9400D3;">a</span><span class="char" style="color: #FF0000;">n</span><span class="char" style="color: #FF7F00;">c</span><span class="char" style="color: #FFFF00;">e</span><span class="char" style="color: #00FF00;">i</span>
                    <span class="char" style="color: #0000FF;">s</span><span class="char" style="color: #4B0082;">e</span><span class="char" style="color: #9400D3;">r</span><span class="char" style="color: #FF0000;">v</span><span class="char" style="color: #FF7F00;">i</span><span class="char" style="color: #FFFF00;">c</span><span class="char" style="color: #00FF00;">e</span>
                </h1>
            </div>
            <nav>
                <ul class="flex space-x-4 mt-4 sm:mt-0 text-lg">
                    <li><a href="#" class="hover:text-blue-200 transition-colors duration-300">Accueil</a></li>
                    <li><a href="#" class="hover:text-blue-200 transition-colors duration-300">À Propos</a></li>
                    <li><a href="#" class="hover:text-blue-200 transition-colors duration-300">Services</a></li>
                    <li><a href="#contact" class="hover:text-blue-200 transition-colors duration-300">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main class="container mx-auto p-4 flex-grow">
        <section class="bg-gradient-to-br from-blue-50 to-indigo-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-4xl font-extrabold text-blue-800 mb-6 leading-tight">Notre Mission</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto">
                « Notre mission, au sein de cet atelier d'infographie à Conakry, est de **doter les individus et les organisations des compétences et des outils nécessaires pour transformer des données complexes en récits visuels clairs, percutants et engageants.** Nous nous engageons à démocratiser la création d'infographies de qualité professionnelle, favorisant ainsi une meilleure communication, une prise de décision éclairée et une diffusion efficace de l'information au sein de la communauté et au-delà. »
            </p>
            <button class="mt-8 bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                Découvrir nos solutions
            </button>
        </section>

        <section class="bg-green-500 text-white p-5 rounded-xl shadow-lg mb-8 text-center">
            <h3 class="text-2xl font-bold mb-2">Disponibilité 24h/24</h3>
            <p class="text-xl">Nous sommes là pour vous, à tout moment, jour et nuit ! Votre satisfaction est notre priorité.</p>
        </section>

        <section class="bg-yellow-500 text-white p-5 rounded-xl shadow-lg mb-8 text-center">
            <h3 class="text-2xl font-bold mb-2">Livraison Partout en Guinée</h3>
            <p class="text-xl">Où que vous soyez en Guinée, nous livrons nos services directement à votre porte !</p>
        </section>

        <section class="bg-white p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-blue-700 mb-8 text-center">Notre Processus de Travail</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 text-center">
                <div class="p-4 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                    <div class="text-4xl font-bold text-blue-500 mb-3">1</div>
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Prise de Contact</h3>
                    <p class="text-gray-700 text-sm">Discutons de vos besoins et de vos idées pour votre projet.</p>
                </div>
                <div class="p-4 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                    <div class="text-4xl font-bold text-blue-500 mb-3">2</div>
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Conception & Validation</h3>
                    <p class="text-gray-700 text-sm">Nous créons un design initial et le soumettons pour votre approbation.</p>
                </div>
                <div class="p-4 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                    <div class="text-4xl font-bold text-blue-500 mb-3">3</div>
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Production</h3>
                    <p class="text-gray-700 text-sm">Une fois validé, nous passons à la réalisation de votre commande.</p>
                </div>
                <div class="p-4 rounded-xl bg-gray-50 border border-gray-100 shadow-sm">
                    <div class="text-4xl font-bold text-blue-500 mb-3">4</div>
                    <h3 class="text-xl font-semibold text-blue-600 mb-2">Livraison</h3>
                    <p class="text-gray-700 text-sm">Votre commande est livrée rapidement et en toute sécurité, partout en Guinée.</p>
                </div>
            </div>
        </section>

        <section class="bg-white p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-blue-700 mb-6">Nos Compétences</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="p-4 rounded-lg bg-blue-50 border border-blue-100 shadow-sm">
                    <h3 class="text-2xl font-semibold text-blue-600 mb-2">Fiabilité</h3>
                    <p class="text-gray-700">Des résultats constants et de haute qualité sur lesquels vous pouvez compter.</p>
                </div>
                <div class="p-4 rounded-lg bg-green-50 border border-green-100 shadow-sm">
                    <h3 class="text-2xl font-semibold text-green-600 mb-2">Rapidité</h3>
                    <p class="text-gray-700">Des délais de livraison optimisés sans compromettre la qualité de notre travail.</p>
                </div>
                <div class="p-4 rounded-lg bg-purple-50 border border-purple-100 shadow-sm">
                    <h3 class="text-2xl font-semibold text-purple-600 mb-2">Performance</h3>
                    <p class="text-700">Des solutions efficaces qui génèrent un impact réel et mesurable pour votre projet.</p>
                </div>
            </div>
        </section>

        <section class="bg-white p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-blue-700 mb-8 text-center">Nos Services</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="bg-gray-50 p-6 rounded-xl shadow-md border border-gray-100 hover:shadow-lg hover:border-blue-300 transition-all duration-300 transform hover:-translate-y-1">
                    <h3 class="text-2xl font-semibold text-blue-600 mb-3">Décoration personnalisée</h3>
                    <p class="text-gray-700 leading-relaxed">Décoration de maillots, képis et t-shirts pour un style unique et percutant.</p>
                </div>
                <div class="bg-gray-50 p-6 rounded-xl shadow-md border border-gray-100 hover:shadow-lg hover:border-blue-300 transition-all duration-300 transform hover:-translate-y-1">
                    <h3 class="text-2xl font-semibold text-blue-600 mb-3">Confection de Banderoles</h3>
                    <p class="text-gray-700 leading-relaxed">Création et confection de banderoles sur mesure pour vos événements et promotions.</p>
                </div>
                <div class="bg-gray-50 p-6 rounded-xl shadow-md border border-gray-100 hover:shadow-lg hover:border-blue-300 transition-all duration-300 transform hover:-translate-y-1">
                    <h3 class="text-2xl font-semibold text-blue-600 mb-3">Création de Logos</h3>
                    <p class="text-gray-700 leading-relaxed">Conception de logos professionnels et mémorables pour renforcer votre identité visuelle.</p>
                </div>
            </div>
        </section>

        <section class="bg-gradient-to-br from-indigo-50 to-blue-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-indigo-800 mb-6">Communication High-Tech (HTC)</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Explorez nos solutions de communication numérique et de services high-tech.
                Nous vous aidons à optimiser votre présence en ligne et à interagir efficacement avec votre audience.
            </p>
            <button class="mt-4 bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                Découvrir les solutions HTC
            </button>
        </section>

        <section class="bg-white p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-blue-700 mb-8 text-center">Nos Réalisations</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-064af053-02ab-4de6-843d-1321bf6edc2e" alt="Carte de faire-part de mariage" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Carte de faire-part</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-caf6a116-6397-4ccc-b499-9dcd1a6b82c1" alt="T-shirt ADER Association" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">T-shirt ADER</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-0a25da61-314d-4377-aa76-83e9076aa2ba" alt="Affiche Excursion Groupe Scolaire Bill-Clinton" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Excursion Scolaire</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-011a1566-ea61-4a92-8b0f-d932d273875f" alt="Maillot de sport CAMAVINGA 11" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Maillot Camavinga</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-4f97627d-d210-45cb-84fe-ee484c56640b" alt="T-shirt BANKAN avec arbre" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">T-shirt Bankan</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-c1f9a1a7-dbcb-432f-81f8-c699e4dacbfc" alt="Maillot de sport ZABALE KONKON 14" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Maillot Zabale Konkon</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-62737abd-56f7-4f53-a3b8-d80f7383ad74" alt="Groupe de personnes en T-shirt d'équipe" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Équipe en T-shirts</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-f9c0341d-85a2-400a-9fc9-3754a514c6c5" alt="Maillot de sport MOHAMED CAMARA 13" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Maillot Mohamed Camara</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-1fb69d64-2c49-45e9-b966-36c858510aa1" alt="Maillot de sport ESP. POPCAN" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Maillot ESP. POPCAN</p>
                    </div>
                </div>
                <div class="relative overflow-hidden rounded-xl shadow-lg group">
                    <img src="uploaded:image.png-55e6dcc1-0b0e-4aef-abcb-837ae5aff3b6" alt="Publicité S22 Ultra Samanla" class="w-full h-48 object-cover rounded-xl transition-transform duration-300 group-hover:scale-105">
                    <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl">
                        <p class="text-white text-lg font-semibold">Publicité S22 Ultra</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-gradient-to-br from-red-50 to-orange-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-red-800 mb-6">Vidéo de Publicité</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Découvrez nos services en action ! Regardez notre vidéo promotionnelle pour en savoir plus sur ce que nous faisons.
            </p>
            <div class="relative w-full max-w-2xl mx-auto" style="padding-bottom: 56.25%;">
                <iframe
                    class="absolute top-0 left-0 w-full h-full rounded-xl shadow-lg"
                    src="https://www.youtube.com/embed/dQw4w9WgXcQ"  title="Vidéo de Publicité Saman Lancei service"
                    frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
            <p class="text-sm text-gray-500 mt-4">
                *Veuillez remplacer le lien de la vidéo ci-dessus par le lien de votre propre vidéo YouTube, Vimeo ou autre plateforme d'hébergement.
            </p>
        </section>

        <section class="bg-gradient-to-br from-purple-50 to-pink-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-purple-800 mb-6">Vos Avis et Satisfaction</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Votre opinion est précieuse pour nous ! Partagez votre expérience et votre degré de satisfaction avec nos services.
                Vos retours nous aident à nous améliorer continuellement.
            </p>
            <button class="mt-4 bg-purple-600 hover:bg-purple-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                Donner votre avis
            </button>
        </section>

        <section class="bg-gradient-to-br from-teal-50 to-green-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-teal-800 mb-6">Confirmation de Réception</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Nous sommes ravis d'apprendre que vous avez bien reçu votre colis !
                Votre satisfaction est notre plus grande récompense. N'hésitez pas à nous faire part de vos impressions.
            </p>
            <button class="mt-4 bg-teal-600 hover:bg-teal-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                Confirmer la réception
            </button>
        </section>

        <section class="bg-gradient-to-br from-yellow-50 to-orange-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-orange-800 mb-6">Évaluez notre Service</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Combien d'étoiles nous donneriez-vous pour votre expérience globale ?
            </p>
            <div class="star-rating text-5xl flex justify-center space-x-2">
                <span class="star" data-value="1">★</span>
                <span class="star" data-value="2">★</span>
                <span class="star" data-value="3">★</span>
                <span class="star" data-value="4">★</span>
                <span class="star" data-value="5">★</span>
            </div>
            <p id="rating-message" class="mt-4 text-lg text-gray-600">Cliquez sur les étoiles pour évaluer !</p>
        </section>

        <section class="bg-gradient-to-br from-blue-50 to-purple-50 p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-blue-800 mb-8 text-center">Ce que nos clients disent de nous</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-white p-6 rounded-xl shadow-md border border-blue-100">
                    <p class="text-gray-700 italic mb-4">"Service exceptionnel ! La décoration de nos maillots a dépassé toutes nos attentes. Rapidité et qualité au rendez-vous. Nous recommandons vivement Saman Lancei service."</p>
                    <p class="font-semibold text-blue-600">- Client satisfait 1</p>
                </div>
                <div class="bg-white p-6 rounded-xl shadow-md border border-purple-100">
                    <p class="text-gray-700 italic mb-4">"Nous avons commandé des banderoles pour notre événement et le résultat était parfait. L'équipe est très professionnelle et la livraison a été effectuée dans les temps. Bravo !"</p>
                    <p class="font-semibold text-purple-600">- Client satisfait 2</p>
                </div>
                </div>
        </section>

        <section class="bg-gradient-to-br from-blue-100 to-cyan-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-blue-800 mb-6">Passez Vos Commandes</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Prêt à transformer vos idées en réalité ? Contactez-nous dès aujourd'hui pour discuter de votre projet et passer commande.
                Notre équipe est à votre écoute pour vous offrir un service personnalisé et de qualité.
            </p>
            <a href="#contact" class="mt-4 bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1 inline-block">
                Contacter pour commander
            </a>
        </section>

        <section class="bg-gray-100 p-8 rounded-2xl shadow-xl mb-8">
            <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Foire Aux Questions (FAQ)</h2>
            <div class="max-w-3xl mx-auto">
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Quels sont vos délais de livraison ?</span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-down"><path d="m6 9 6 6 6-6"/></svg>
                    </div>
                    <div class="faq-answer">
                        <p>Nos délais de livraison varient en fonction de la complexité du projet et de la quantité commandée. Nous nous efforçons de livrer dans les plus brefs délais, généralement entre 3 et 7 jours ouvrables après validation de la conception.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Proposez-vous des maquettes avant la production ?</span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-down"><path d="m6 9 6 6 6-6"/></svg>
                    </div>
                    <div class="faq-answer">
                        <p>Oui, absolument ! Pour la plupart de nos services, nous fournissons des maquettes numériques ou physiques pour validation avant de lancer la production finale, afin de garantir votre entière satisfaction.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Puis-je commander en grande quantité ?</span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-down"><path d="m6 9 6 6 6-6"/></svg>
                    </div>
                    <div class="faq-answer">
                        <p>Oui, nous acceptons les commandes en grande quantité et nous pouvons discuter de tarifs préférentiels pour les volumes importants. Contactez-nous pour un devis personnalisé.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Comment puis-je suivre ma commande ?</span>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-down"><path d="m6 9 6 6 6-6"/></svg>
                    </div>
                    <div class="faq-answer">
                        <p>Une fois votre commande confirmée et la production lancée, nous vous tiendrons informé de son avancement. Pour les livraisons, un numéro de suivi pourra vous être fourni si applicable.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="bg-gradient-to-br from-gray-100 to-gray-200 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-gray-800 mb-6">Rechercher sur Google</h2>
            <p class="text-xl text-gray-700 leading-relaxed max-w-3xl mx-auto mb-6">
                Vous avez une question spécifique ou souhaitez trouver plus d'informations ?
                Utilisez le moteur de recherche Google directement depuis notre site.
            </p>
            <form action="https://www.google.com/search" method="get" target="_blank" class="flex flex-col sm:flex-row items-center justify-center space-y-4 sm:space-y-0 sm:space-x-4 max-w-xl mx-auto">
                <input
                    type="text"
                    name="q"
                    placeholder="Rechercher sur Google..."
                    class="w-full sm:w-2/3 p-3 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                >
                <button
                    type="submit"
                    class="w-full sm:w-1/3 bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-6 rounded-lg shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-0.5"
                >
                    Rechercher
                </button>
            </form>
        </section>


        <section id="contact" class="bg-gradient-to-br from-green-50 to-teal-100 p-8 rounded-2xl shadow-xl mb-8 text-center">
            <h2 class="text-3xl font-bold text-green-800 mb-6">Contactez-nous</h2>
            <div class="text-xl text-gray-700 leading-relaxed max-w-2xl mx-auto flex flex-col items-center">
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-mail mr-2 text-blue-600"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
                    <span class="font-semibold">Email :</span> <a href="mailto:klancei064@gmail.com" class="text-blue-600 hover:underline ml-1">klancei064@gmail.com</a>
                </p>
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-map-pin mr-2 text-blue-600"><path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/></svg>
                    <span class="font-semibold">Adresse :</span> Conakry/Gbessia
                </p>
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-phone mr-2 text-blue-600"><path d="M22 16.92v3a2 2 0 0 1-2.18 2.02 15.15 15.15 0 0 1-12.62-6.38A15.15 15.15 0 0 1 2.02 4.18 2 2 0 0 1 4 2h3a2 2 0 0 1 2 2.18 10.15 10.15 0 0 0 2.4 7.22 10.15 10.15 0 0 0 7.22 2.4A2 2 0 0 1 22 16.92z"/></svg>
                    <span class="font-semibold">Téléphone :</span> <a href="tel:+224625850315" class="text-blue-600 hover:underline ml-1">625 85 03 15</a>
                </p>
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-message-circle mr-2 text-green-600"><path d="M7.9 20A9 9 0 1 0 4 16.1L2 22Z"/></svg>
                    <span class="font-semibold">WhatsApp :</span> <a href="https://wa.me/224662218429" target="_blank" rel="noopener noreferrer" class="text-green-600 hover:underline ml-1">662 21 84 29</a>
                </p>
                <p class="mb-3 flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-globe mr-2 text-gray-600"><circle cx="12" cy="12" r="10"/><path d="M12 2a14.5 14.5 0 0 0 0 20 14.5 14.5 0 0 0 0-20"/><path d="M2 12h20"/></svg>
                    <span class="font-semibold">Site Web :</span> <a href="http://SamanLancei.service.com" target="_blank" rel="noopener noreferrer" class="text-blue-600 hover:underline ml-1">SamanLancei.service.com</a>
                </p>
                <div class="flex space-x-6 mt-4">
                    <a href="https://www.facebook.com/SamanLancei" target="_blank" rel="noopener noreferrer" class="text-blue-700 hover:text-blue-900 transition-colors duration-300">
                        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" fill="currentColor" stroke="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-facebook"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
                        <span class="sr-only">Page Facebook Saman Lancei</span>
                    </a>
                    <a href="https://www.instagram.com/Samanlancei" target="_blank" rel="noopener noreferrer" class="text-pink-600 hover:text-pink-800 transition-colors duration-300">
                        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucude-instagram"><rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.5" y1="6.5" y2="6.5"/></svg>
                        <span class="sr-only">Page Instagram Samanlancei</span>
                    </a>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-gray-900 text-gray-300 p-6 mt-12 rounded-t-xl">
        <div class="container mx-auto text-center text-sm">
            <p>© 2025 Mon Super Site Web. Tous droits réservés.</p>
            <p class="mt-3">
                <a href="#" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a> |
                <a href="#" class="hover:text-white transition-colors duration-300">Conditions d'utilisation</a>
            </p>
        </div>
    </footer>

    <script>
        // JavaScript pour la fonctionnalité d'évaluation par étoiles
        document.addEventListener('DOMContentLoaded', () => {
            const stars = document.querySelectorAll('.star-rating .star');
            const ratingMessage = document.getElementById('rating-message');

            stars.forEach(star => {
                star.addEventListener('click', () => {
                    const value = parseInt(star.dataset.value);
                    // Remplir les étoiles jusqu'à la valeur sélectionnée
                    stars.forEach((s, index) => {
                        if (index < value) {
                            s.classList.add('filled');
                        } else {
                            s.classList.remove('filled');
                        }
                    });
                    ratingMessage.textContent = `Vous avez donné ${value} étoile(s) ! Merci pour votre avis.`;
                });

                star.addEventListener('mouseover', () => {
                    const value = parseInt(star.dataset.value);
                    stars.forEach((s, index) => {
                        if (index < value) {
                            s.classList.add('filled');
                        } else {
                            s.classList.remove('filled');
                        }
                    });
                });

                star.addEventListener('mouseout', () => {
                    // Réinitialiser les étoiles si aucune n'est cliquée
                    let clickedValue = 0;
                    stars.forEach(s => {
                        if (s.classList.contains('filled')) {
                            clickedValue = Math.max(clickedValue, parseInt(s.dataset.value));
                        }
                    });

                    if (clickedValue === 0) {
                        stars.forEach(s => s.classList.remove('filled'));
                        ratingMessage.textContent = 'Cliquez sur les étoiles pour évaluer !';
                    } else {
                        stars.forEach((s, index) => {
                            if (index < clickedValue) {
                                s.classList.add('filled');
                            } else {
                                s.classList.remove('filled');
                            }
                        });
                    }
                });
            });

            // JavaScript pour la fonctionnalité de la FAQ (accordeon)
            const faqQuestions = document.querySelectorAll('.faq-question');

            faqQuestions.forEach(question => {
                question.addEventListener('click', () => {
                    const answer = question.nextElementSibling;
                    const isActive = question.classList.contains('active');

                    // Fermer toutes les autres réponses
                    faqQuestions.forEach(q => {
                        if (q !== question && q.classList.contains('active')) {
                            q.classList.remove('active');
                            q.nextElementSibling.classList.remove('open');
                            q.nextElementSibling.style.maxHeight = null;
                        }
                    });

                    // Ouvrir ou fermer la réponse cliquée
                    if (isActive) {
                        question.classList.remove('active');
                        answer.classList.remove('open');
                        answer.style.maxHeight = null;
                    } else {
                        question.classList.add('active');
                        answer.classList.add('open');
                        answer.style.maxHeight = answer.scrollHeight + "px"; // Ajuste la hauteur de la réponse
                    }
                });
            });
        });
    </script>
</body>
</html>


cd /chemin/vers/votre/dossier/site-web
https://github.com/Samanlancei/Samanlancei-.git
