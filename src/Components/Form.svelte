<script>
  // import nodemailer from "nodemailer";
  // import img from "../Assets/png-gralypho/grabouillons.svg";

   export let nom; 
     export let prenom; 
       export let societe; 
         export let email; 
           export let telephone; 
             export let demande; 

  function handleSubmit(event) {
    event.preventDefault();

    const data = {
      nom,
      prenom,
      societe,
      email,
      telephone,
      demande,
    };

    // Configuration du transport SMTP
    // const transporter = nodemailer.createTransport({
    //   service: "YOUR_SMTP_SERVICE", // Remplacer par le service choisi
    //   auth: {
    //     user: "YOUR_SMTP_USERNAME", // Remplacer par votre nom d'utilisateur
    //     pass: "YOUR_SMTP_PASSWORD", // Remplacer par votre mot de passe
    //   },
    // });

    // Options de l'email
    // const mailOptions = {
    //   from: "votre_email@votre_domaine.com", // Remplacer par votre adresse email
    //   to: "contact@gralypho.com",
    //   subject: "Formulaire de contact",
    //   text: JSON.stringify(data),
    };

    // Envoi de l'email
    // transporter.sendMail(mailOptions, (error, info) => {
    //   if (error) {
    //     console.log("Envoi du mail impossible:", error);
    //   } else {
    //     console.log("Email envoyé avec succès !");
    //   }
    // });
  // }
</script>



<section class="section-form">
  <h1>Contactez-nous dès aujourdhui!</h1>
<div class="coordonnees">
 <h4>Téléphone: 0672 901 614</h4> 
  <h4>Mail: contact@gralypho.com</h4> 
</div>
<form on:submit={handleSubmit} class="form">
  <label for="nom">Nom :</label>
  <input type="text" id="nom" bind:value={nom} />

  <label for="prenom">Prénom :</label>
  <input type="text" id="prenom" bind:value={prenom} />

  <label for="societe">Société (optionnel):</label>
  <input type="text" id="societe" bind:value={societe} placeholder="Champ vide si vous n'avez pas de nom de société" />

  <label for="email">Email :</label>
  <input type="email" id="email" bind:value={email} />

  <label for="telephone">Téléphone :</label>
  <input type="tel" id="telephone" bind:value={telephone} />

  <label for="demande">Votre demande : </label>
  <textarea id="demande" bind:value={demande} class="demande"></textarea>

  <button type="submit">Envoyer</button>
</form>
</section>

<style>
  .section-form {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: auto;
    background-color: white;
    padding: 20px;
  }
  section.section-form h1{
    grid-column: span 12;
    grid-row: 1;
    margin: 0 auto;
    text-align: center;
    font-family: epilogue;
    font-weight: 700;
    font-size: var(--l);
    color: var(--primary);
    letter-spacing: -0.050em;
    margin-top: 50px;

  }
  .form{
    grid-column: 2/7;
    grid-row: 2;
    display: flex;
  flex-direction: column;
    gap: 20px;
    padding: 20px;
    margin-top: 50px;
  }
   input , .demande{
       border: 1px solid var(--primary);
       font-family: epilogue;
        font-weight: 400;
        padding: 10px;
        border-radius: 8px;
        box-shadow: 0px 0px 15px 0px rgba(128, 128, 128, 0.14)
   }
   label{
       border: none;
            font-family: Poppins;
        font-weight: 500;
        color: var(--primary);
        letter-spacing: -0.050em;
   }
   button{
       border: none;
       background-color: var(--CTA);
       color: white;
       font-family: epilogue;
        font-weight: 500;
        margin: 10px 100px;
        padding: 10px;
        border-radius: 8px;
        box-shadow: 0px 0px 15px 0px rgba(128, 128, 128, 0.14)
      }
      .coordonnees{
        grid-column: 8/12;
        grid-row: 2;
    margin-top: 100px;
    font-family: poppins;
    font-weight: 500;
    letter-spacing: -0.040em;
    font-size: 0.8em;
    color: grey;
      }


</style>
