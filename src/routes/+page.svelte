<script>
import Header from "../components/Header.svelte";
import Services from "../components/Services.svelte";
import Informative from "../components/Informative.svelte";
import Form from "../components/form/Form.svelte";
import MaskInput from "svelte-input-mask";
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Página inicial da landing page" />
	<link href="https://fonts.googleapis.com/css2?family=Fira+Code&family=JetBrains+Mono:ital,wght@0,100;0,500;1,500;1,800&family=Poppins:wght@400;600;700;900&family=Roboto+Condensed:ital,wght@1,400;1,700&family=Roboto+Mono:wght@200&display=swap" rel="stylesheet">
	<script src="https://cdnjs.cloudflare.com/ajax/libs/inputmask/5.0.6/inputmask.min.js"></script>
</svelte:head>

<main>
<Header/>
<Services/>
<Informative/>
<Form/>
</main>
<style>
	@import "../global.css";
</style>
