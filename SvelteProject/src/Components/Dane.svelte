<script>
    let dane = ["Jan", "Kowalski", "60", "Mężczyzna"]
    </script>
<div class="dane">
    <ul>
        <li>Imię: {dane[0]}</li>
        <li>Nazwisko: {dane[1]} </li>
        <li>Wiek: {dane[2]} </li>
        <li>Płeć: {dane[3]}</li>

    </ul>
</div>
<style> 
div.dane{
    width: 100%;
    background-color: #659ca6;
    padding: 20px;
    height: 20vh;
    display: flex;
    align-items: center;
}

ul{
        list-style: none;
    }
li{
        font-size: 30px;
        font-weight: 600;
        color: #eee;
    }
</style>