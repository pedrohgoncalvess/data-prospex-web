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

<style>

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

    .nav-item a {
        color: var(--font_primary);
        font-size: 25px;
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