<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sunnyday Selections</title>
  <link rel="icon" type="image/png" href="https://img.icons8.com/emoji/48/sun-emoji.png">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      background-color: #fff8e1;
      color: #333;
    }
    header {
      background: linear-gradient(to right, #ffd54f, #ffb300);
      padding: 40px 20px;
      text-align: center;
      color: #fff;
    }
    header h1 {
      margin: 0;
      font-size: 2.5rem;
    }
    header p {
      font-size: 1.2rem;
      margin-top: 10px;
    }
    .cta-button {
      background-color: #fff;
      color: #ff8f00;
      border: none;
      padding: 12px 24px;
      font-size: 1rem;
      margin-top: 20px;
      border-radius: 30px;
      cursor: pointer;
      font-weight: bold;
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }
    .features {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    .feature {
      background: #fff3e0;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .feature h3 {
      margin-top: 0;
      color: #ff6f00;
    }
    .about {
      background: #fffde7;
      border-radius: 12px;
      padding: 20px;
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 10px;
      background: #fff8e1;
      padding: 20px;
      border-radius: 12px;
    }
    input, textarea, button {
      padding: 10px;
      border-radius: 6px;
      border: 1px solid #ccc;
      font-size: 1rem;
    }
    button[type="submit"] {
      background-color: #ffb300;
      color: white;
      border: none;
      font-weight: bold;
      cursor: pointer;
    }
    footer {
      background-color: #ffe082;
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
    }
    .lang-toggle {
      text-align: right;
      padding: 10px 20px;
    }
    .lang-toggle button {
      background: none;
      border: none;
      font-weight: bold;
      color: #ff6f00;
      cursor: pointer;
    }
    #thankYouMessage {
      display: none;
      color: green;
      font-weight: bold;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <div class="lang-toggle">
    <button onclick="toggleLanguage()" id="langButton">🇫🇷 Français</button>
  </div>

  <header>
    <h1 id="title">Sunnyday Selections</h1>
    <p id="subtitle">Tailored Snacks, Delivered With Sunshine!</p>
    <p id="featuresLine">Hassle-free service • Custom selection • Full support</p>
    <button class="cta-button" onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });" id="ctaBtn">
      Bring a Machine to My Location
    </button>
  </header>

  <section>
    <img src="c:\Users\emmac\OneDrive\Pictures\Screenshots\Screenshot 2025-06-01 225254.png" alt="Sunnyday vending machine" style="width: 100%; max-width: 800px; border-radius: 12px; margin: 20px auto; display: block;" />
  </section>

  <section class="features">
    <div class="feature">
      <h3 id="feature1Title">🎯 Personalized Selection</h3>
      <p id="feature1Text">We stock your machine with snacks and drinks chosen just for your team, students, or guests.</p>
    </div>
    <div class="feature">
      <h3 id="feature2Title">⚙️ Full-Service Management</h3>
      <p id="feature2Text">From delivery to restocking and maintenance — we’ve got it covered, so you don’t have to worry.</p>
    </div>
    <div class="feature">
      <h3 id="feature3Title">🚚 Fast, Friendly Setup</h3>
      <p id="feature3Text">We’ll bring your machine right to your location and get it up and running fast!</p>
    </div>
  </section>

  <section id="contact">
  <h2 id="contactTitle">Let’s Get Snacking!</h2>
  <form action="https://formspree.io/f/mvgroojz" method="POST">
    <input type="text" name="name" placeholder="Your Name" required />
    <input type="text" name="business" placeholder="Business Name (optional)" />
    <input type="email" name="email" placeholder="Email" required />
    <input type="text" name="location" placeholder="Your Location" required />
    <textarea name="message" rows="4" placeholder="What kind of vending service are you looking for?" required></textarea>
    <button type="submit">Send My Info!</button>
  </form>
  <p id="thankYouMessage">Thanks for contacting us! We’ll get back to you soon.</p>
  <div style="margin-top: 20px; font-size: 0.95rem;">
    <p><strong>Or reach us directly:</strong></p>
    <p>Email: <a href="mailto:sunnydayselections@gmail.com">sunnydayselections@gmail.com</a><br />
    Phone: <a href="tel:+5146213120">(514) 621-3120</a></p>
  </div>
</section>

  <footer>
    &copy; 2025 Sunnyday Selections. All rights reserved.
  </footer>

  <script>
    let isFrench = false;

    function toggleLanguage() {
      isFrench = !isFrench;

      document.getElementById("langButton").innerText = isFrench ? "EN English" : "FR Français";
      document.getElementById("title").innerText = isFrench ? "Sunnyday Sélections" : "Sunnyday Selections";
      document.getElementById("subtitle").innerText = isFrench ? "Des collations personnalisées, livrées avec du soleil!" : "Tailored Snacks, Delivered With Sunshine!";
      document.getElementById("featuresLine").innerText = isFrench ? "Service sans tracas • Sélection personnalisée • Support complet" : "Hassle-free service • Custom selection • Full support";
      document.getElementById("ctaBtn").innerText = isFrench ? "Installer une machine chez moi" : "Bring a Machine to My Location";
      document.getElementById("feature1Title").innerText = isFrench ? "🎯 Sélection personnalisée" : "🎯 Personalized Selection";
      document.getElementById("feature1Text").innerText = isFrench ? "Nous remplissons votre machine avec des collations et boissons choisies pour votre équipe, vos étudiants ou vos invités." : "We stock your machine with snacks and drinks chosen just for your team, students, or guests.";
      document.getElementById("feature2Title").innerText = isFrench ? "⚙️ Gestion complète" : "⚙️ Full-Service Management";
      document.getElementById("feature2Text").innerText = isFrench ? "De la livraison à l'entretien — on s'occupe de tout pour vous." : "From delivery to restocking and maintenance — we’ve got it covered, so you don’t have to worry.";
      document.getElementById("feature3Title").innerText = isFrench ? "🚚 Installation rapide et conviviale" : "🚚 Fast, Friendly Setup";
      document.getElementById("feature3Text").innerText = isFrench ? "Nous apportons la machine directement chez vous et la mettons en marche rapidement!" : "We’ll bring your machine right to your location and get it up and running fast!";
      document.getElementById("aboutTitle").innerText = isFrench ? "À propos de nous" : "About Us";
      document.getElementById("aboutText").innerHTML = isFrench ?
        "<strong>Sunnyday Sélections</strong> rend la distribution automatique facile et agréable. Nous livrons et gérons des machines personnalisées adaptées à votre espace et à vos goûts—en prenant tout en charge, de l'installation au réapprovisionnement. Avec un service amical et une touche professionnelle ensoleillée, nous apportons commodité (et un peu de soleil) à votre quotidien." :
        "<strong>Sunnyday Selections</strong> makes vending effortless and enjoyable. We deliver and manage customized snack machines tailored to your space and your tastes—handling everything from setup to restocking. With friendly service and a bright, professional touch, we bring convenience (and a little sunshine) to your day.";
      document.getElementById("contactTitle").innerText = isFrench ? "Discutons de vos besoins!" : "Let’s Get Snacking!";
      // Optional: you can translate the thank you message too
      document.getElementById("thankYouMessage").innerText = isFrench ? "Merci de nous avoir contactés ! Nous vous répondrons bientôt." : "Thanks for contacting us! We’ll get back to you soon.";
    }

    // Form submission with fetch API to show thank-you message
    const form = document.querySelector('form[action="https://formspree.io/f/mvgroojz"]');
    const thankYouMessage = document.getElementById('thankYouMessage');

    form.addEventListener('submit', function(event) {
      event.preventDefault();

      const formData = new FormData(form);

      fetch(form.action, {
        method: 'POST',
        body: formData,
        headers: { 'Accept': 'application/json' }
      }).then(response => {
        if (response.ok) {
          thankYouMessage.style.display = 'block';
          form.reset();
        } else {
          alert('Oops! There was a problem submitting your form.');
        }
      }).catch(() => {
        alert('Oops! There was a problem submitting your form.');
      });
    });
  </script>
</body>
</html>
![Screenshot 2025-06-01 225254](https://github.com/user-attachments/assets/39093262-91c6-4e0a-8b93-7f085de72542)
