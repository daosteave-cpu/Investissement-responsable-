# Investissement-responsable-
Site web – Investissement Responsable
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Investissement Responsable</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background: #f4f6f8;
  color: #333;
}
header {
  background: #0b3c5d;
  color: white;
  padding: 25px;
  text-align: center;
}
section {
  background: white;
  margin: 20px;
  padding: 20px;
  border-radius: 8px;
}
h2 { color: #0b3c5d; }
input, button {
  width: 100%;
  padding: 12px;
  margin: 8px 0;
}
button {
  background: #0b3c5d;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 16px;
}
button:hover { opacity: 0.9; }
.small { font-size: 0.9em; color: #555; }
.warning {
  color: #b00020;
  font-size: 0.95em;
}
footer {
  text-align: center;
  font-size: 14px;
  padding: 15px;
  color: #666;
}
</style>
</head>

<body>

<header>
  <h1>Investissement Responsable</h1>
  <p>Plateforme d’information et d’investissement privé entre connaissances</p>
</header>

<section>
  <h2>Créer un compte</h2>
  <input id="name" placeholder="Nom complet">
  <input id="email" placeholder="Email">
  <input id="phone" placeholder="Téléphone">
  <button onclick="register()">Créer mon compte</button>
  <p class="small">Aucun dépôt ne se fait sur le site.</p>
</section>

<section>
  <h2>Connexion</h2>
  <input id="loginEmail" placeholder="Email">
  <button onclick="login()">Se connecter</button>
  <p id="welcome"></p>
</section>

<section>
  <h2>Projets disponibles</h2>
  <ul>
    <li><strong>Agriculture locale</strong> – Durée 6 à 12 mois (rendement estimatif 10–20%)</li>
    <li><strong>Immobilier</strong> – Durée 12 à 36 mois (rendement estimatif 8–15%)</li>
  </ul>
  <p class="small">Les rendements sont indicatifs et non garantis.</p>
</section>

<section>
  <h2>Dépôt & Contact</h2>
  <p>Les investissements se font uniquement après discussion privée.</p>
  <button onclick="window.location.href='https://wa.me/22666804845'">
    📲 Contacter via WhatsApp
  </button>
  <p><strong>Email :</strong> daosteave@gmail.com</p>
</section>

<section>
  <h2>Fonds d’investissement</h2>
  <ul>
    <li><strong>Fonds total :</strong> 1 250 000 FCFA</li>
    <li><strong>Projet Agriculture :</strong> 750 000 FCFA</li>
    <li><strong>Projet Immobilier :</strong> 500 000 FCFA</li>
  </ul>
  <p><em>Dernière mise à jour : 10/01/2026</em></p>
  <p class="warning">
    ⚠️ Données indicatives, mises à jour manuellement.  
    Contactez-nous pour confirmation.
  </p>
</section>

<section>
  <h2>Mentions légales & Avertissement</h2>
  <p class="warning">
    Ce site ne constitue pas un appel public à l’épargne.<br>
    Les investissements sont privés, basés sur la confiance entre parties.<br>
    Tout investissement comporte un risque de perte partielle ou totale du capital.<br>
    Aucun rendement n’est garanti.
  </p>
</section>

<footer>
  © 2026 – Investissement Responsable
</footer>

<script>
function register() {
  let user = {
    name: document.getElementById('name').value,
    email: document.getElementById('email').value,
    phone: document.getElementById('phone').value
  };
  if (!user.email) {
    alert("Email obligatoire");
    return;
  }
  localStorage.setItem(user.email, JSON.stringify(user));
  alert("Compte créé avec succès !");
}

function login() {
  let email = document.getElementById('loginEmail').value;
  let user = localStorage.getItem(email);
  if (user) {
    user = JSON.parse(user);
    document.getElementById('welcome').innerText =
      "Bienvenue " + user.name + ". Contactez-nous sur WhatsApp pour discuter.";
  } else {
    alert("Compte introuvable");
  }
}
</script>

</body>
</html>
