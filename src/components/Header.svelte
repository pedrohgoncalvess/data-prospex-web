<script lang="ts">

    import Typewriter from "svelte-typewriter";

    function scrollToBottom() {
        const element = document.getElementById('contact');
        if (element) {
            element.scrollIntoView({ behavior: 'smooth' });
        }
    }

</script>

    <div class="enter-messages">

        <section class="welcome-message">
            <h2>
                Bem vindo a <span class="azurite-tech">Azurite Tech</span>.
            </h2>
            <Typewriter mode="loop"  interval={[80, 80, 80]}>
                <p class="typewriter-phrases">Tecnologia não precisa <b class="text-focus-neg">custar tanto.</b></p>
                <p class="typewriter-phrases">Tecnologia não precisa ser <b class="text-focus-neg">complicada.</b></p>
                <p class="typewriter-phrases">Tecnologia pode <b class="text-focus-pos">transformar</b>negócios.</p>
            </Typewriter>
        </section>

        <section class="buttons-redirect">
            <a class="contact-button" on:click={scrollToBottom}>
                Entre em contato<span class="arrow"></span>
            </a>
            <a class="blog-button">
                Leia nosso blog
            </a>
        </section>
    </div>

<style>

    .typewriter-phrases {
        font-family: "Fira Code";
        font-size: 22px;
    }

    .text-focus-neg {
        color: var(--negative_color);
        margin: 0;
        padding: 0;
    }

    .text-focus-pos {
        color:var(--font_secondary);
        margin:0;
        padding: 0;
    }


    .azurite-tech {
        color: var(--font_secondary);
        font-size: 40px;
    }

    .enter-messages {
        display: flex;
        flex-direction: column;
        justify-content: left;
        text-align: left;
        color: var(--font_primary);
        margin-left: 10%;
        margin-top: 3%;
        font-size: 20px;
    }


    .buttons-redirect {
        display: flex;
        font-size: 85%;
        align-items: center;
        margin-top: 5%;
        gap: 10%;

    }

    .blog-button {
        background-color: transparent;
        color: var(--font_primary);
        border: none;

    }

    .blog-button:hover {
        color: var(--font_third);
    }


    .contact-button {
        display: flex;
        color: var(--font_primary);
        background-color: var(--font_secondary);
        padding: 10px 13px;
        border-radius: 20px;
        transition: all .3s ease;
        font-weight: bold;
        cursor: pointer;
        align-items: center;
        font-size: 14px;
    }

    .contact-button > .arrow {
        width: 6px;
        height: 6px;
        border-right: 2px solid var(--font_primary);
        border-bottom: 2px solid var(--font_primary);
        position: relative;
        transform: rotate(-45deg);
        margin: 0 6px;
        transition: all .3s ease;
    }

    .contact-button > .arrow::before {
        display: block;
        background-color: currentColor;
        width: 3px;
        transform-origin: bottom right;
        height: 2px;
        position: absolute;
        opacity: 0;
        bottom: calc(-2px / 2);
        transform: rotate(45deg);
        transition: all .3s ease;
        content: "";
        right: 0;
    }

    .contact-button:hover > .arrow {
        transform: rotate(-45deg) translate(4px, 4px);
    }

    .contact-button:hover > .arrow::before {
        opacity: 1;
        width: 8px;
    }

    .contact-button:hover {
        background-color: #009887;
    }



    @media(min-width: 850px) {

        .enter-messages {
            display: flex;
            justify-content: center;
            margin: 5% auto;
            width: 60%;
        }

    }

    @media(min-width: 1650px) {
        .enter-messages {
            margin: 2% auto 1% auto;
        }
    }



</style>
