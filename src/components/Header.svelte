<script>
</script>

<nav>

    <ul class="nav-container">
        <li class="nav-item">
            <a href="#">
                <span class="fa-solid fa-house nav-icon"></span>
                <span class="nav-text">Inicio</span>
            </a>
        </li>

        <li class="nav-item">
            <a href="#">
                <span class="fa-solid fa-diagram-project nav-icon"></span>
                <span class="nav-text">Projetos</span>
            </a>
        </li>

        <li class="nav-item">
            <a href="#">
                <span class="fa-solid fa-newspaper nav-icon"></span>
                <span class="nav-text">Data Garden</span>
            </a>
        </li>

        <li class="nav-item">
            <a href="#">
                <span class="fa-solid fa-users nav-icon"></span>
                <span class="nav-text">Sobre nós</span>
            </a>
        </li>

    </ul>

</nav>

    <div class="enter-messages">

        <section class="welcome-message">
            <h2>
                Bem vindo a <b>Data ProspeX</b>.
                <br>
                Resolvemos problemas com dados.
            </h2>
        </section>

        <section class="buttons-redirect">
            <a class="contact-button">
                Entre em contato<span class="arrow"></span>
            </a>
            <a class="blog-button">
                Leia nosso blog
            </a>
        </section>
    </div>

<style>

    :root {
        --font_primary:white;
        --font_secondary: #039dd3;
        --font_third: #4fceff;
        --italic-font: #c4c4c4;
    }

    .nav-container {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0;
        margin: 0;
        gap: 10%;
        position: fixed;
        bottom: 0;
        width: 100%;
        height: 8%;
        background-color: rgb(0, 56, 63, 0.3);
        backdrop-filter: blur(7px);
        border-radius: 7px;
    }

    .nav-text {
        display: none;
    }

    .enter-messages {
        display: flex;
        flex-direction: column;
        justify-content: left;
        text-align: left;
        color: var(--font_primary);
        margin-left: 3%;
        margin-top: 3%;
    }

    .nav-item a {
        color: var(--font_primary);
        font-size: 25px;
    }

    /*BUTTONS*/

    .buttons-redirect {
        display: flex;
        font-size: 85%;
        align-items: center;
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
        border-color: text-hover-color;
    }

    .contact-button:hover > .arrow::before {
        opacity: 1;
        width: 8px;
    }

    .contact-button:hover {
        background-color: #009887;
    }



    @media(min-width: 1080px) {

        .nav-icon {
            display: none;
        }

        .nav-text {
            display: flex;
            justify-content: center;
            color: azure;
        }

        .nav-container {
            position: fixed;
            top: 0;
        }
    }



</style>
