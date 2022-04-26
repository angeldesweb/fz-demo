<script>
    
    import Home from 'svelte-material-icons/HomeOutline.svelte';
    import Mail from 'svelte-material-icons/Mail.svelte';
    import C from 'svelte-material-icons/AlphaCCircleOutline.svelte';
    import Right from 'svelte-material-icons/Send.svelte';
    import fb from './assets/facebook_icon.svg';
    import inst from './assets/instagram_icon.svg';
    //REAL IMPORTS
    import HeaderDefault from './lib/Headers/HeaderDefault.svelte';
    import FirstRow from './Views/Home/FirstRow.svelte';
    import SecondRow from './Views/Home/SecondRow.svelte';
    let size = '2rem';
</script>

<div class="main">
    <HeaderDefault/>
    <FirstRow/>
    <SecondRow/>
    <footer>
        <div class="row foot">
            <div class="col s12 m6">
                <div class="social">
                    <img class="logo-media" src={fb} alt="facebook">
                    <img class="logo-media" src={inst} alt="instagram">
                    <p style="font-size:.8rem"
                    >Términos y condiciones <span class="txt-sec">|</span>
                    Políticas de privacidad <span class="txt-sec">|</span> 
                    2022 <C/>  Food Zinder</p>
                </div>
            </div>
            <div class="col s12 m6">
                <div class="row">
                    <div class="col m6">
                        <p class="footer-sub" style="font-size:.8rem">CONTÁCTANOS</p>
                        <br>
                        <ul>
                            <li style="display:flex; ">
                                <i style="padding:.2em .5em"><Home size={'1.3rem'} /></i>
                                <p style="font-size:.8rem">
                                    La Cocotera Coworking
                                    San Rosendo N° 12
                                    Tarifa, Cádiz - España
                                </p>
                            </li>
                            <br>
                            
                            <li>
                                <i style='padding:.2em .5em 0 .5em'><Mail size={"1.3rem"} /></i>
                                <p style="font-size:.8rem">info@foodzinder.com</p>
                            </li>
                        </ul>
                    </div>
                    <div class="col m6">
                        <p class="footer-sub" style="font-size:.8rem">
                            SUSCRIBIRME AL BOLETÍN
                        </p>
                        <div class="input-field" style="width:100%">
                            <input style="color:#fff;width:80%;font-size:.8rem" id="boletin" class="left" type="text">
                            <label for="boletin">Tu email</label>
                            <div class="righted-btn right" style="">
                                <Right width={'.8em'} height={'100%'} color="#f67599"/>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</div>

<style>
    .main {
        max-width:100vw;
        min-height:100vh;
        display:flex;
        align-content: center;
        flex-direction: column;
        background-image: url('https://res.cloudinary.com/stand/image/upload/v1650943596/foodzinder/bg_mpu5mj.png');
    }
    .row {
        width:95%;
    }
    .col {
        display:flex;
        flex-direction:column;
        align-items:center;
        justify-content: space-around;
    }
    footer {
        background-color: #121921;
        width:100%;
        padding-bottom:1rem;
        margin-bottom:0;
    }
    .foot {
        padding:2em;
        width:100%;
        color:#fff;
        border-bottom:1px solid #929089;
        border-radius:0 0 10% 10%;    
    }
    li {
        display:flex;
        color:#929089;
    }
    .footer-sub {
        width:100%;
        font-weight:bolder;
        
    }
    .righted-btn {
        display:grid;
        place-content: center;
        width:20%;
        height:3rem;
        border:1px solid #f67599;
        border-radius:0 25% 25% 0;
    }
    .logo-media {
        width:2rem;
        display:inline;
        margin:1rem;
    }
    .txt-sec {
        color:#929089;
    }
</style>