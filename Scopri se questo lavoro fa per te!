<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sei adatto per l'animazione turistica? Fai il test!</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; background-color: #f4f4f4; padding: 20px; }
        .container { max-width: 600px; background: white; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); margin: auto; }
        h1 { color: #ff5733; }
        .question { margin: 20px 0; font-weight: bold; }
        .options { display: flex; flex-direction: column; }
        .options label { background: #ffcccb; padding: 10px; margin: 5px; border-radius: 5px; cursor: pointer; }
        .options input { display: none; }
        .submit-btn { background: #ff5733; color: white; padding: 10px 20px; border: none; cursor: pointer; border-radius: 5px; margin-top: 20px; }
        .submit-btn:hover { background: #e04e2f; }
        .result { display: none; font-size: 18px; font-weight: bold; margin-top: 20px; }
        .contact-form { display: none; margin-top: 20px; }
        .contact-form input, .contact-form button { margin: 5px 0; padding: 10px; width: 90%; border-radius: 5px; border: 1px solid #ccc; }
        .contact-form button { background: #25D366; color: white; cursor: pointer; }
        .contact-form button:hover { background: #1ebe5d; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Sei adatto a diventare un animatore turistico?</h1>
        <form id="quizForm">
            <div class="question">1. Ti piace stare a contatto con le persone?</div>
            <div class="options">
                <label><input type="radio" name="q1" value="3"> Sì, mi piace socializzare e divertirmi con nuove persone</label>
                <label><input type="radio" name="q1" value="2"> Dipende, preferisco stare nel mio gruppo</label>
                <label><input type="radio" name="q1" value="1"> No, preferisco lavori più solitari</label>
            </div>
            
            <div class="question">2. Ti senti a tuo agio a parlare davanti a un pubblico?</div>
            <div class="options">
                <label><input type="radio" name="q2" value="3"> Assolutamente sì</label>
                <label><input type="radio" name="q2" value="2"> Non sempre, ma potrei farcela</label>
                <label><input type="radio" name="q2" value="1"> No, odio parlare in pubblico</label>
            </div>

            <button type="button" class="submit-btn" onclick="calculateScore()">Scopri il tuo risultato</button>
        </form>
        
        <div id="result" class="result"></div>
        
        <div id="contactForm" class="contact-form">
            <h2>Lascia i tuoi dati per candidarti!</h2>
            <input type="text" id="name" placeholder="Nome e Cognome" required>
            <input type="email" id="email" placeholder="Email" required>
            <input type="tel" id="phone" placeholder="Telefono" required>
            <button onclick="sendToWhatsApp()">Invia candidatura su WhatsApp</button>
        </div>
    </div>

    <script>
        function calculateScore() {
            let score = 0;
            let totalQuestions = 2;
            let answers = document.querySelectorAll('input[type="radio"]:checked');
            
            answers.forEach(answer => {
                score += parseInt(answer.value);
            });
            
            let resultText = "";
            if (score >= 5) {
                resultText = "🔥 PERFETTO! Hai tutte le carte in regola! Candidati subito qui sotto.";
            } else if (score >= 3) {
                resultText = "💡 BUON POTENZIALE! Lascia i tuoi dati per saperne di più!";
            } else {
                resultText = "🤔 FORSE NON È IL LAVORO GIUSTO, ma possiamo aiutarti a migliorare! Lascia i tuoi dati per ricevere consigli.";
            }
            
            document.getElementById("result").innerHTML = resultText;
            document.getElementById("result").style.display = "block";
            document.getElementById("contactForm").style.display = "block";
        }
        
        function sendToWhatsApp() {
            let name = document.getElementById("name").value;
            let email = document.getElementById("email").value;
            let phone = document.getElementById("phone").value;
            let whatsappNumber = "393317478393"; // Inserisci il numero WhatsApp corretto
            
            if (name && email && phone) {
                let message = `Ciao! Mi chiamo ${name}, la mia email è ${email} e il mio numero di telefono è ${phone}. Vorrei candidarmi per l'animazione turistica!`;
                let whatsappUrl = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;
                window.open(whatsappUrl, "_blank");
            } else {
                alert("Compila tutti i campi per inviare la candidatura.");
            }
        }
    </script>
</body>
</html>
