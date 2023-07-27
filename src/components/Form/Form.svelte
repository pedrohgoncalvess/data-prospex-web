<script lang="ts">
    import PhoneNumber from "./PhoneNumber.svelte";

    let name:string = '';
    let phoneNumber:string = '';
    let email:string = '';
    let segment:string = '';
    let message:string = '';

    function toTheSubmit() {
        console.log(name)
        console.log(email)
        console.log(phoneNumber)
        console.log(segment)
        console.log(message)
    }

</script>

<div class="form">
    <h2>Esclareça suas dúvidas e nos conte suas ideias!</h2>

    <form on:submit|preventDefault={toTheSubmit} class="inputs">
        <label>Nome<span class="required">*</span></label>
        <input type="text" bind:value={name} placeholder="Como devemos chamar você?" class="name-field" required>

        <label>Telefone<span class="required">*</span></label>
        <PhoneNumber bind:value={phoneNumber} class="number-field"/>

        <label>E-mail<span class="required">*</span></label>
        <input type="email" bind:value={email} placeholder="example@email.com" class="email-field" required>

        <label>Segmento da empresa</label>
        <input type="text" bind:value={segment} class="segment-field" placeholder="Ex: Contabilidade">

        <label>Fale sobre seu problema e/ou ideia</label>
        <textarea rows="3" cols="33" bind:value={message} class="message-input" placeholder="Descreva um problema/ideia ou cite alguma solução que trabalhamos."></textarea>

        <button type="submit" class="submit-form">Entrar em contato</button>
    </form>
</div>
<style>

    .form {
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 100%;
        margin:auto;
        font-size: 18px;
        background-image: linear-gradient(transparent, #013f4d);
    }

    .form h2 {
        color: white;
        margin: 1% auto 6% 3% ;
    }

    :global(::placeholder) {
        color: white;
    }

    .inputs {
        display:flex;
        flex-direction: column;
        margin: auto;
    }

    .inputs input {
        width: 95%;
        height: 35px;
        border-bottom-color: white;
        border-top: none;
        border-left: none;
        border-right: none;
        margin-bottom: 8%;
        background-color: transparent;
        color: white;
    }

    .inputs input:hover {
        border-radius: 5px;
        border-color: gray;
    }

    :global(.number-field) {
        width: 95%;
        height: 35px;
        border-bottom-color: white;
        border-top: none;
        border-left: none;
        border-right: none;
        margin-bottom: 10%;
        background-color: transparent;
        color: white;
    }

    :global(.number-field:hover) {
        border-radius: 5px;
        border-color: gray;
    }

    label {
        color: white;
    }

    .message-input {
        border-bottom-color: white;
        border-top: none;
        border-left: none;
        border-right: none;
        word-wrap: break-word;
        word-break: break-all;
        background-color: transparent;
        color:white;
        font-weight: bold;
    }

    .required {
        color:red;
    }

    .submit-form {
        border-radius: 13px;
        background-color: #01ace8;
        border: none;
        width: 160px;
        height: 45px;
        margin: 10% auto;
        color: white;
        font-size: 15px;
        font-weight: bold;
    }


</style>