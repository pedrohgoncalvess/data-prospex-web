<script>
import {displayPopUp} from "./stores/displaySitu.js";

</script>

{#if $displayPopUp}
    <div class="pop-up">
        <div class="pop-up-finish">
            <button class="fa-solid fa-xmark close-pop-up" on:click={() => {displayPopUp.set(false)}}></button>
            <h3 class="text-pop-up"> 🥳 Estamos ansiosos para conversar com você, logo logo entraremos em contato! 🎉</h3>
        </div>
    </div>
{/if}

<style>

    .pop-up {
        display: flex;
        width: 100%;
        justify-content: center;
    }

    .pop-up-finish {
        display: flex;
        align-items: start;
        width: 50%;
        position: fixed;
        top: 2%;
        border-radius: 5px;
        background-color: #c4c4c4;
        opacity: 50%;
        text-align: center;
    }

    .close-pop-up {
        margin-top: 1%;
        width: 9%;
        font-size: 20px;
        color: red;
        background-color: transparent;
        border: none;
    }

    .text-pop-up {
        margin: 0;
        padding: 1% 2% 1% 0;
    }

</style>



