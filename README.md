# comprend-pas-
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Questionnaire pour Victoire</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #ffe6f0;
      color: #333;
      text-align: center;
      padding: 40px;
    }
    #questionnaire {
      display: none;
      margin-top: 30px;
    }
    .question {
      margin: 20px 0;
    }
    select {
      padding: 5px;
      font-size: 16px;
    }
    input[type="text"] {
      padding: 10px;
      font-size: 16px;
      margin-bottom: 10px;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
    }
    #message {
      margin-top: 20px;
      font-weight: bold;
      color: red;
    }
  </style>
</head>
<body>

  <h1>Bienvenue</h1>
  <p>Entre ton prénom pour continuer :</p>
  <input type="text" id="nameInput" placeholder="Ton prénom ici">
  <br>
  <button onclick="checkName()">Valider</button>

  <div id="message"></div>

  <div id="questionnaire">
    <h2>Petit questionnaire pour toi</h2>

    <div class="question">
      <p>1) Comment tu vas mon cœur ?</p>
      <select>
        <option value="">Choisis une note</option>
        <option value="1">1</option>
        <option value="2">2</option>
        <option value="3">3</option>
        <option value="4">4</option>
      </select>
    </div>

    <div class="question">
      <p>2) Je te manque ?</p>
      <select>
        <option value="">Choisis une note</option>
        <option value="1">1</option>
        <option value="2">2</option>
        <option value="3">3</option>
        <option value="4">4</option>
      </select>
    </div>

    <div class="question">
      <p>3) Est-ce que tu m’aimes ?</p>
      <select>
        <option value="">Choisis une note</option>
        <option value="1">1</option>
        <option value="2">2</option>
        <option value="3">3</option>
        <option value="4">4</option>
      </select>
    </div>
  </div>

  <script>
    function checkName() {
      const name = document.getElementById("nameInput").value.trim().toLowerCase();
      const acceptedNames = ["victoire", "la femme de ta vie"];
      const messageDiv = document.getElementById("message");
      const questionnaire = document.getElementById("questionnaire");

      if (acceptedNames.includes(name)) {
        questionnaire.style.display = "block";
        messageDiv.textContent = "";
      } else {
        questionnaire.style.display = "none";
        messageDiv.textContent = "désolé ce site ne t’est pas dédié";
      }
    }
  </script>

</body>
</html>
