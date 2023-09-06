<script lang="ts">
    import Softwares from "$lib/images/services-icons/softwares-development.png"
    import DataManagement from "$lib/images/services-icons/data-management.png"
    import Reports from "$lib/images/services-icons/reports.png"
    import Chatbots from "$lib/images/services-icons/chatbots.png"
    import Automation from "$lib/images/services-icons/automation.png"
    import DataEnchriment from "$lib/images/services-icons/data-enrichment.png"

    import { register } from 'swiper/element/bundle'

    register()
</script>

<div class="container-services">
    <div class="title-services">
        <h2>Serviços que prestamos</h2>
    </div>
    <swiper-container slides-per-view="1" speed="3" loop="true" css-mode="true" navigation="true" autoplay="false" pagination="true">

        <swiper-slide>
            <div class="principal-service">
                <h2>Softwares</h2>
                <img class="conf-image" src={Softwares} alt="Icone que representa engreganem de analytics">
                <h2 class="text-explaning-service">Criação de sistemas de informação (ex CRM, ERP)</h2>
            </div>
        </swiper-slide>
        <swiper-slide>
            <div class="principal-service">
                <h2>Ambientes de dados</h2>
                <img class="conf-image" src={DataManagement} alt="Icone que representa bancos de dados">
                <h2 class="text-explaning-service">Desenvolvimento e gerenciamento de ambientes de dados</h2>
            </div>
        </swiper-slide>
        <swiper-slide>
            <div class="principal-service">
                <h2>Relatórios</h2>
                <img class="conf-image" src={Reports} alt="Icone que representa relatórios">
                <h2 class="text-explaning-service">Elaboração, criação de relatórios estratégicos e operacionais</h2>
            </div>
        </swiper-slide>
        <swiper-slide>
            <div class="principal-service">
                <h2>Chatbots</h2>
                <img class="conf-image" src={Chatbots} alt="Icone chatbot robô">
                <h2 class="text-explaning-service">Criação de chatbots para WhatsApp, Telegram e Web.</h2>
            </div>
        </swiper-slide>
        <swiper-slide>
            <div class="principal-service">
                <h2>Automação</h2>
                <img class="conf-image" src={Automation} alt="Icone robo automação">
                <h2 class="text-explaning-service">Automação de tarefas com desenvolvimento de RPA's.</h2>
            </div>
        </swiper-slide>
        <swiper-slide>
            <div class="principal-service">
                <h2>Enriquecimento de dados</h2>
                <img class="conf-image" src={DataEnchriment} alt="Icone enriquecimento de dados web">
                <h2 class="text-explaning-service">Desenvolvimento de web scraplings, rotinas de consumo de API's e aberturas de web hooks.</h2>
            </div>
        </swiper-slide>
    </swiper-container>
</div>

<style>

    .title-services {
        color: var(--font_primary);
        font-size: 17px;
    }

    .container-services {
        width: 60%;
        margin: auto;
        text-align: center;
    }

    .conf-image {
        width: 30%;
    }

    .services-container h2 {
        font-size: 15px;
    }

    .principal-service {
        text-align: center;
        background-color: var(--background_service);
        opacity: 0.6;
        border-radius: 10px;
        margin: 4% auto;
        width: 70%;
        padding: 0 0 0 3%;
    }

    .principal-service:hover {
        opacity: 1;
        transform: scale(1.1);
        transition: 0.8s;
    }

    .text-explaning-service  {
        padding-top: 8%;
        padding-bottom: 6%;
        font-size: 15px;
    }

    @media(min-width: 850px) {

        .principal-service {
            flex: 1;
            text-align: center;
            align-items: center;
            background-color: #c9c8c8;
            opacity: 0.6;
            border-radius: 10px;
        }

        .principal-service {
            max-width: 330px;
            max-height: 350px;
        }
    }

</style>