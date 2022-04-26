<script>
    import { fly } from 'svelte/transition'
    import img1 from '../../assets/dish.png';
    import img2 from '../../assets/dish1.png';
    import img3 from '../../assets/dish2.png';

    const images = [img1,img2,img3];
    $: active = 0;
    const changeSlide = () => {
        active === 0 ? active++ : active === 2 ? active = 0 : active++; 
    }

    setInterval(() => {changeSlide()},8000)
</script>

<div class="carousel">
    {#key active}
        <img in:fly={{y:-20,duration:2000}} src={images[active]} alt="dish" />
    {/key}
</div>

<style>
    img {
        width:75%;
    }
    .carousel {
        display:flex;
        justify-content: center;
        align-items:center;
        width:100%;
    }
</style>