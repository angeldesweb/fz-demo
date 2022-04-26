<script>
    import HeaderHome from '../../../lib/Headers/HeaderHome.svelte';
    import CardFirstLook from '../../../lib/Cards/CardFirstLook.svelte';
</script>

<article class="col s12 m6">
    <HeaderHome/>
    <CardFirstLook/>
</article>

<style>
    .col {
        display:flex;
        flex-direction:column;
        align-items:center;
        justify-content: space-around;
    }
</style>