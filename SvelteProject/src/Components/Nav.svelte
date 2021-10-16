<script>
export let isLogged = true;
import BurgerMenu from 'svelte-burger-menu';
</script>

   
    <BurgerMenu menuColor = {'#000'} padding = {'25px'} backgroundColor = {'#548B95'} >
        <li>Tutorial</li>
        <li>Mapa Aptek</li>
        <li>Oceń aplikację</li>
        {#if isLogged}
        <li>Wyloguj</li>
        {:else}
        <li>Zaloguj</li>
        {/if}
    </BurgerMenu>

    <!-- <i class="fas fa-align-left"></i> -->
    

<style>

    li{
        font-size: 30px;
        margin: 10px;
        text-transform: uppercase;
        letter-spacing: 1px;
        list-style: none;
        cursor: progress;
    }
</style>