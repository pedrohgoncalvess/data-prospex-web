<script lang="ts">
    import MaskInput from "svelte-input-mask";
    import {displayPopUp} from "./stores/displaySitu.js";


    let name:string = '';
    let email:string = '';
    let segment:string = '';
    let message:string = '';
    let phoneNumber:string = ''

    let mask = "(00) 0 0000-0000";

    const maskInput = ({ detail }) => {
        phoneNumber = detail.inputState.maskedValue;
    }


    function toTheSubmit() {
        if (phoneNumber.includes("*") || (phoneNumber.length === 0)) {
            console.log(phoneNumber)
            console.log("Preencha corretamente o número de telefone.")
        }
        if (name.length === 0) {
            //console.log("Preencha corretamente o nome.")
        }
        if (email.length === 0) {
            //console.log("Preencha corretamente o e-mail.")
        }
        else {
            displayPopUp.set(true)
        }
    }

</script>

<div class="form">
    <h2>Esclareça suas dúvidas e nos conte suas ideias!</h2>

    <form class="inputs" on:submit|preventDefault={toTheSubmit}>
        <label>Nome<span class="required">*</span></label>
        <input type="text" bind:value={name}  placeholder="Como devemos chamar você?" class="name-field">

        <label>Telefone<span class="required">*</span></label>
        <MaskInput class="number-field" on:change={maskInput} alwaysShowMask maskChar="*" {mask} />

        <label>E-mail<span class="required">*</span></label>
        <input type="email" bind:value={email} placeholder="example@email.com" class="email-field">

        <label>Segmento da empresa</label>
        <input type="text" bind:value={segment} class="segment-field" placeholder="Ex: Contabilidade">

        <label>Fale sobre seu problema e/ou ideia</label>
        <textarea rows="3" cols="33" bind:value={message} class="message-input" placeholder="Descreva um problema/ideia ou cite alguma solução que trabalhamos."></textarea>

        <button id="contact" class="submit-form">Entrar em contato</button>
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
        color: var(--font_primary);
        margin: 10% auto 6% 6% ;
    }

    :global(::placeholder) {
        color: var(--font_primary);
    }

    .inputs {
        display:flex;
        flex-direction: column;
        margin: auto;
    }

    .inputs input {
        width: 95%;
        height: 35px;
        border-bottom-color: var(--font_primary);
        border-top: none;
        border-left: none;
        border-right: none;
        margin-bottom: 8%;
        background-color: transparent;
        color: var(--font_primary);
    }

    .inputs input:hover {
        border-radius: 5px;
        border-color: gray;
    }

    :global(.number-field) {
        width: 95%;
        height: 35px;
        border-bottom-color: var(--font_primary);
        border-top: none;
        border-left: none;
        border-right: none;
        margin-bottom: 10%;
        background-color: transparent;
        color: var(--font_primary);
    }

    :global(.number-field:hover) {
        border-radius: 5px;
        border-color: gray;
    }

    label {
        color: var(--font_primary);
    }

    .message-input {
        border-bottom-color: var(--font_primary);
        border-top: none;
        border-left: none;
        border-right: none;
        word-wrap: break-word;
        word-break: break-all;
        background-color: transparent;
        color:var(--font_primary);
        font-weight: bold;
        margin-top: 3%;
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
        color: var(--font_primary);
        font-size: 15px;
        font-weight: bold;
    }

    .submit-form:hover {
        background-color: #009830;
        transition: all 0.5s ease;
    }

    @media(min-width: 850px) {
        .form h2 {
            margin-left: auto;
            margin-top: 5%;
        }
    }


</style>