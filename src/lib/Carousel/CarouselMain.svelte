<script>
    import { fly } from 'svelte/transition';
    
    const img1 = 'https://res.cloudinary.com/stand/image/upload/v1650944252/foodzinder/dish_arhdru.png';
    const img2 = 'https://res.cloudinary.com/stand/image/upload/v1650943613/foodzinder/dish1_apwxhi.png';
    const img3 = 'https://res.cloudinary.com/stand/image/upload/v1650943637/foodzinder/dish2_qvubsj.png';

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