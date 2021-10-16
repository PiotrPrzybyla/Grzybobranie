<script>
import { each } from "svelte/internal";

    import Dane from "./Dane.svelte";
    let choroby = ["cukrzyca", "epilepsja"];
</script>
<h1>Panel Poszkodowanego</h1>
<Dane/>

<div class="pannels">
    <div class="choroby pannel">
       <p> Lista chorób: </p>
       <ul>
           {#each choroby as choroba}
           <li>{choroba}</li>
           {/each}
       </ul>
    </div>
    <div class="adres pannel"> <p>  Adres:</p>
        <p>Psie Pole, ul. Kocia 213/7</p>
      <p></p>
    </div>
    <div class="podziekowanie pannel"> <button>Przekaż podziękowanie dla ratownika</button>
    </div>
</div>
<style>
     h1{
        margin: 0;
        text-align: center;
        padding: 15px;
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