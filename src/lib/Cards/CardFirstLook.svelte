<script>
    import Search from 'svelte-material-icons/StoreSearch.svelte';
    import Pin from 'svelte-material-icons/MapMarker.svelte';
    import Gps from 'svelte-material-icons/CrosshairsGps.svelte';
</script>

<div class="card z-depth-4 box">
    <div class="input-field">
        <i class="prefix"><Search color="#b4b4b4" width="2rem" /></i>
        <input id="icon_prefix" type="text" class="validate">
        <label for="icon_prefix">Nombre de restaurante o plato</label>
    </div>
    <div class="input-field">
        <i class="prefix"><Pin color="#b4b4b4" width="2rem" /></i>
        <input id="location" type="text"  list="lugares" class="validate">
        <label for="location">Localidad</label>
        <datalist id="lugares">
            <option value="Tarifa">Tarifa</option>
            <option value="Bolonia, Cádiz">Bolonia, Cádiz</option>
        </datalist>
    </div>
    <a style="margin:0;padding:0;color:#929089" class="waves-effect waves-light btn-flat" href="#/#" >
        <i class="left"><Gps color="#b4b4b4" width="2rem" /></i>
        Cerca de mi
    </a>
    <br>
    <a  style="width:100%" class="waves-effect waves-light btn" href="#/#">Buscar</a>
</div>

<style>
    .box {
        width:80%;
        padding:1rem;
        margin-top:2rem
    }
    .btn {
        background-color: #F67599;
    }
</style>