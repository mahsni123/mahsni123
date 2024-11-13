<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Application de Devis en TND</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Gestion des Devis - Prix en TND</h1>

        <!-- Formulaire pour ajouter un produit -->
        <form id="formProduit">
            <h2>Ajouter un Produit</h2>
            <label for="nomProduit">Nom du Produit</label>
            <input type="text" id="nomProduit" required placeholder="Nom du produit">

            <label for="prixAchat">Prix d'Achat (en TND)</label>
            <input type="number" id="prixAchat" required placeholder="Prix d'achat" step="0.01">

            <label for="marge">Marge (%)</label>
            <input type="number" id="marge" required placeholder="Marge (%)" step="0.01">

            <button type="submit">Ajouter Produit</button>
        </form>

        <!-- Formulaire pour créer un devis -->
        <form id="formDevis">
            <h2>Créer un Devis</h2>
            <label for="clientDevis">Nom du Client</label>
            <input type="text" id="clientDevis" required placeholder="Nom du client">

            <label for="produitDevis">Sélectionner un Produit</label>
            <select id="produitDevis" required></select>

            <label for="quantite">Quantité</label>
            <input type="number" id="quantite" required value="1" min="1">

            <button type="submit">Ajouter au Devis</button>
        </form>

        <!-- Affichage du devis -->
        <div id="resumeDevis">
            <h2>Résumé du Devis</h2>
            <ul id="listDevis"></ul>
            <p id="totalDevis">Total : 0 TND</p>
        </div>

        <button id="generatePDF">Générer PDF</button>
    </div>

    <script src="script.js"></script>
</body>
</html>
