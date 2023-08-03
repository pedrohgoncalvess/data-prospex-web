<script>
import SearchEngine from "$lib/images/informative/search-engine.png"
import DashboardAnalytics from "$lib/images/informative/data-analysis.png"
</script>
<div class="data-information">
    <div class="data-forrester">
        <div class="image-container">
            <img class="informative-image" src={SearchEngine} alt="Engine de busque desenhada">
        </div>
        <div class="informative-text">
            <h2>Quais os benefícios de ter uma cultura analítica?</h2>
            <p>
                Uma pesquisa publicada pela Forrester que entrevistou 150 tomadores de decisão de empresas americanas, revelou claras
                vantagens competitivas para as empresas que possuíam uma cultura data driven.
                <br>
            </p>
            <i>
                "Companies with advanced analytics cultures averaged a 9.1% increase
                in marketing ROI over the last one to two years — a
                1.7x performance improvement over those without."
            </i>
            <br>
            <p>
                Isto é, organizações que possuem uma cultura analitica em estágio avançado tem 9 pontos percentuais de aumento em ROI em marketing e cresceram quase 2 vezes mais dos que não tem essa cultura.
                <br>
                <i>
                    A pesquisa também pontua que a cultura e os benefícios não se limitam a área de marketing.
                </i>
            </p>
            <a href="https://screenforce.nl/wp-content/uploads/2019/01/Neustar-ANA-Forrester-Consulting-Report.pdf">Pesquisa completa</a>
        </div>
    </div>
    <div class="data-driven">
        <div class="informative-text">
            <h2>Oque é uma cultura analítica?</h2>
            <p>
                Ter uma cultura analítica ou ser data driven significa tomar decisões com base em dados concretos, em vez de depender apenas de intuição ou suposições.
            </p>
            <p>
                Isso permite uma compreensão mais clara da situação, minimizando o viés pessoal e aumentando a probabilidade de tomar decisões mais assertivas.
            </p>
        </div>
        <div class="image-container">
            <img class="informative-image" src={DashboardAnalytics} alt="Dashboards analytics">
        </div>
    </div>
</div>
<div class="data-prospex">
    <div>
        <div class="informative-text">
            <h1>
                Quais problemas a <b>Data ProspeX</b> pode me ajudar a resolver?
            </h1>
            <p>
                A Data ProspeX trabalha desenvolvendo soluções em todo escopo de dados. Desde a produção do dado bruto, até a coleta, limpeza, armazenamento, analíse e até criação de modelos de inteligência artificial para atacar problemas mais complexos.
            <p>
                Seja seu problema com falta de software para desempenhar melhor sua operação, perca de tempo com tarefas repetitivas, elaboração de relatórios ou analise de dados, nós podemos ti auxiliar.
            </p>
        </div>
    </div>
</div>


<style>
    .data-information {
        display: flex;
        flex-direction: column;
        margin-bottom: 5%;
    }

    .informative-text {
        display: flex;
        flex-direction: column;
        color: white;
    }

    .informative-text b {
        color: var(--font_secondary);
    }


    /*data forrester*/

    .data-forrester {
        display: flex;
        justify-content: center;
        margin: 3% auto;
        width: 80%;
    }

    .data-forrester i {
        font-family: "JetBrains Mono", sans-serif;
        color: var(--italic-font);
    }

    .data-forrester a {
        text-decoration: none;
        color: grey;
        font-size: 80%;
    }

    .data-forrester a:hover {
        color: var(--font_third);
    }


    /*cultura data driven*/

    .data-driven {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 3% auto;
        width: 80%;
    }

    .data-driven p {
        margin-top: 2%;
        font-size: 18px;
    }


    .image-container {
        display: none;
    }

    /*data prospex*/

    .data-prospex {
        display: flex;
        justify-content: center;
        margin: 2% auto;
        color: var(--font_primary);
        width: 80%;
    }

    .data-prospex p {
        margin-top: 0;
    }

    .data-prospex h1 {
        font-size: 25px;
    }

    .informative-text p{
        font-size: 18px;
    }

    @media(min-width: 850px) {

        .data-information {
            margin-top: 0;
        }

        .image-container {
            display: flex;
            justify-content: center;
            margin-left: 5%;
            margin-right: 5%;
        }

        .informative-image {
            width: 200px;
            max-height: 300px;
            margin: auto;
        }

        .data-driven {
            margin-top: 10%;
        }

        .data-prospex {
            margin-top: 10%;
        }
    }

</style>