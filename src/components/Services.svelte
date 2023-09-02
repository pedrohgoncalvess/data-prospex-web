<script>
    import Softwares from "$lib/images/services-icons/softwares-development.png"
    import DataManagement from "$lib/images/services-icons/data-management.png"
    import Reports from "$lib/images/services-icons/reports.png"
    import Chatbots from "$lib/images/services-icons/chatbots.png"
    import Automation from "$lib/images/services-icons/automation.png"
    import DataEnchriment from "$lib/images/services-icons/data-enrichment.png"
</script>

<div class="services-container">
    <div class="title-services">
        <b>
            Nós trabalhamos com toda a régua de produção dos dados <i class="fa-solid fa-caret-down"></i>
        </b>
    </div>
    <div class="information-services">
        <div class="principal-service">
            <h2>Softwares</h2>
            <img class="conf-image" src={Softwares} alt="Icone que representa engreganem de analytics">
            <h2 class="sub-title-services">Criação de sistemas de informação (ex CRM, ERP)</h2>
        </div>
        <div class="principal-service">
            <h2>Ambientes de dados</h2>
            <img class="conf-image" src={DataManagement} alt="Icone que representa bancos de dados">
            <h2 class="sub-title-services">Desenvolvimento e gerenciamento de ambientes de dados</h2>
        </div>
        <div class="principal-service">
            <h2>Relatórios</h2>
            <img class="conf-image" src={Reports} alt="Icone que representa relatórios">
            <h2 class="sub-title-services">Elaboração, criação de relatórios estratégicos e operacionais</h2>
        </div>

    </div>
    <div class="title-other-services">
        <b>
            Nós também desenvolvemos outras soluções <i class="fa-solid fa-caret-down"></i>
        </b>
    </div>
    <div class="information-other-services">
        <div class="secondary-service">
            <h2>Chatbots</h2>
            <img class="conf-image" src={Chatbots} alt="Icone chatbot robô">
            <h2 class="sub-title-services">Criação de chatbots para WhatsApp, Telegram e Web.</h2>
        </div>
        <div class="secondary-service">
            <h2>Automação</h2>
            <img class="conf-image" src={Automation} alt="Icone robo automação">
            <h2 class="sub-title-services">Automação de tarefas com desenvolvimento de RPA's.</h2>
        </div>
        <div class="secondary-service">
            <h2>Enriquecimento de dados</h2>
            <img class="conf-image" src={DataEnchriment} alt="Icone enriquecimento de dados web">
            <h2 class="sub-title-services">Desenvolvimento de web scraplings, rotinas de consumo de API's e aberturas de web hooks.</h2>
        </div>
    </div>
</div>

<style>

    .services-container {
        display: flex;
        flex-flow: column wrap;
        margin-top: 7%;
    }

    .conf-image {
        width: 30%;
    }

    .services-container h2 {
        font-size: 15px;
    }

    .title-services {
        justify-content: space-around;
        margin: 3% 5% 3% 10%;
        color: var(--font_primary);
        font-size: 20px;
    }

    .information-services {
        display: flex;
        flex-flow: column;
        justify-content: center;
        margin: 5% 10% 3% 10%;
    }

    .principal-service {
        text-align: center;
        background-color: var(--background_service);
        opacity: 0.6;
        border-radius: 10px;
        margin: 4% auto;
        width: 70%;
        max-width: 370px;
        max-height: 290px;
    }

    .principal-service:hover {
        opacity: 1;
        transform: scale(1.1);
        transition: 0.8s;
    }

    /*====================*/

    .sub-title-services  {
        padding-top: 8%;
        padding-bottom: 6%;
    }

    .title-other-services {
        justify-content: space-around;
        margin: 7% 0 0 10%;
        color: var(--font_primary);
        font-size: 20px;
    }

    .information-other-services {
        display: flex;
        flex-flow: column;
        justify-content: center;
        margin: 0 10%;
    }


    .secondary-service {
        text-align: center;
        background-color: var(--background_service);
        opacity: 0.6;
        border-radius: 10px;
        margin: 4% auto;
        width: 70%;
        max-width: 370px;
        max-height: 290px;
    }

    .secondary-service:hover {
        opacity: 1;
        transform: scale(1.1);
        transition: 0.8s;
    }

    @media(min-width: 850px) {

        .services-container {
            display: flex;
            flex-flow: column wrap;
            margin-top: 7%;
        }

        .information-services {
            display: flex;
            flex-flow: row wrap;
            gap: 5%;
            margin-top: 0;
        }

        .principal-service {
            flex:1;
            text-align: center;
            align-items: center;
            background-color: #c9c8c8;
            opacity: 0.6;
            border-radius: 10px;
        }

        .information-other-services {
            display: flex;
            flex-flow: row wrap;
            gap: 5%;
            margin-top: 0;
            margin-bottom: 0;
        }

        .secondary-service {
            flex:1;
            text-align: center;
            align-items: center;
            background-color: var(--background_service);
            opacity: 0.6;
            border-radius: 10px;
        }
    }

    @media(min-width: 1650px) {

        .services-container {
            display: flex;
            flex-flow: column wrap;
            margin-top: 0;
        }

        .information-services {
            margin:0;
            padding: 0;
            gap: 5%;
        }

        .principal-service {
            margin: 0;
            padding: 0;
        }


        .information-other-services {
            margin:0;
            padding: 0;
            gap: 5%;
        }

        .secondary-service {
            margin: 0;
            padding: 0;
        }

    }

</style>