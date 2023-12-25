<script>
</script>

<footer>
	<h1>Gralypho</h1>
	<p>Mail: gralypho@gmail.com  Tel: 06 51 85 85 85</p>
<div class="wrapper-media">
<a href="https://facebook.com/intent/tweet?url=URL_DU_SITE&text=Texte_du_tweet&via=NomUtilisateurTwitter" target="_blank" ><i class="fa-brands fa-square-facebook"></i></a>
<a href="https://twitter.com/intent/tweet?url=URL_DU_SITE&text=Texte_du_tweet&via=NomUtilisateurTwitter" target="_blank"><i class="fa-brands fa-square-twitter"></i></a>
<a href="https://instagram.com/intent/tweet?url=URL_DU_SITE&text=Texte_du_tweet&via=NomUtilisateurTwitter" target="_blank"><i class="fa-brands fa-square-instagram"></i></a>
<a href="https://tiktok.com/intent/tweet?url=URL_DU_SITE&text=Texte_du_tweet&via=NomUtilisateurTwitter" target="_blank"><i class="fa-brands fa-tiktok"></i></a>
</div>
<h4>© 2023 Nom de l'Entreprise. Tous droits réservés.</h4>

</footer>





<style>
	footer {
		display: grid;
		grid-template-columns: repeat(12, 1fr);
		grid-template-rows: auto;
		height: 100%;
		margin-top: 150px;
		font-size: 16px;
		background-color: var(--colorO);
		color: white;
		text-align: center;
		font-family: epilogue;
	}
	footer h1 {
		grid-column: 1/5;
		grid-row: 1;
		font-weight: 200;
		font-size: 1.2em;
		color: white;
	}
	footer p {
		grid-column: 1/11;
		grid-row: 2;
	
		font-family: epilogue;
		font-weight: 200;
		font-size: 0.8em;
		color: var(--colorC);
	}
	footer h4{
		grid-column: 4/12;
		grid-row: 4;
		/* margin-top: 100px; */
		font-family: epilogue;
		font-weight: 200;
		font-size: 0.6em;
		color: var(--colorC);
		text-align: left;

	}
	.wrapper-media{
		grid-column: 1/4 ;
		grid-row: 3;
	}
</style>
