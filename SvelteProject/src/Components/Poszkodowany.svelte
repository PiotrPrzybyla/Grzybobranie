<script>
import { each } from "svelte/internal";

    import Dane from "./Dane.svelte";
    let choroby = ["cukrzyca", "epilepsja"];
    let lista_urzadzen = ["Zegarek (Garmin Fenix 6x Zahir)", "Telefon (Iphone 13 pro)", "Pas do mierzenia tętna (Garmin HTML dual)"];
</script>
<h1>Panel Poszkodowanego</h1>
<Dane/>

<div class="pannels">
    <div class="choroby pannel">
       <!-- <p> Lista chorób: </p> -->
       <ul>
           <li> <h2>   Lista chorób: </h2></li>
           {#each choroby as choroba}
           <li>{choroba}</li>
           {/each}
       </ul>
    </div>
    <div class="adres pannel"> 
        <ul>
            <li> <h2>   Adres:  </h2></li>
        Psie Pole, ul. Kocia 213/7 <br> 3 piętro
    </ul>
    </div>
    <div class="urzadzenie pannel"> 
        <ul>
            <li> <h2>   Lista urządzeń </h2></li>
            {#each lista_urzadzen as listaUrzadzen}
            <li>{listaUrzadzen}</li>
            {/each}
        </ul>
    </div> 
    <div class="podziekowanie pannel"><ul><button>Przekaż podziękowanie dla ratownika</button></ul> 
    </div>
</div>
<style>
     h1{
        margin: 0;
        text-align: center;
        padding: 15px;
    }
    h2{
        font-size: 35px;
        margin-bottom: 10px;
    }
    div.pannels{
        width: 100%;
        display: flex;
        justify-content: space-between;
    }
    div.pannel{
        width: 100%;
        padding: 20px;
        height: 70vh;
        font-size: 30px;
       
    }
    ul{
        list-style: none;
        text-align: left;
        border: 2px solid #7cc1be;
        border-radius: 20px;
        background-color: rgba(141,210,207,.3);
        height: 45vh;
    }
    li{
        text-align: left;
        display: block;
        height: 100px;
    }
    div.podziekowanie{
        text-align: center;
    }
    button{
        background-color: #ceebea;
        cursor: pointer;
        border: 2px solid black;
        padding: 20px;
        border-radius: 20px;
        margin: 20px;
        
    }
</style>