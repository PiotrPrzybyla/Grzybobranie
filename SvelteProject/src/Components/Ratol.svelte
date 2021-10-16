<script>
    import Dane from "./Dane.svelte";
    let radius = 500;
    let iloscAkcji = 5;
</script>
<!-- <Nav/> -->
<h1>Panel Ratownika</h1>

<Dane/>
<div class="pannels">
    <div class="promien pannel">
        <ul>
            <li><h2> Powiadom mnie gdy poszkodowany <br> będzie w odległości:</h2></li>
        
        <input type="number" bind:value={radius}> m
    </ul>
    </div>
    <div class="powiadomienia pannel"> 
        <ul>
           <li> <h2> Powiadomienia: </h2></li>
            <li>
                <label for="mail">Powiadom mnie mailowo</label>
                <input name="mail" type="checkbox">

            </li>
            <li>
                <label for="sms">Powiadom mnie SMSem</label>
                <input name="sms" type="checkbox">

            </li>
            <li>
                <label for="mail">Powiadomienia pop up </label>
                <input name="mail" type="checkbox">

            </li>
        </ul>
    </div>
    <div class="iloscAkcji pannel"><ul> <li><h2>Ilość wykonanych akcji:</h2></li>    <p>{iloscAkcji}</p></ul>
    </div>
    

</div>
<style>
    label{
        display: inline-block;
    }
   
    div.pannel{
        width: 100%;
        padding: 20px;
        height: 70vh;
        font-size: 30px;
    }
    div.pannels{
        width: 100%;
        display: flex;
        justify-content: space-between;
    }
    h1{
        margin: 0;
        text-align: center;
        padding: 15px;
    }
    ul{
        list-style: none;
        text-align: left;
        border: 2px solid #7cc1be;
        border-radius: 20px;
        background-color: rgba(141,210,207,.3);
        height: 45vh;
    }
   
</style>