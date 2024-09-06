<script>
import ComillaApertura from './icon/ComillaApertura.vue';
import ComillaCierre from './icon/ComillaCierre.vue';
export default {
    name: 'SectionMensaje',
    components: {
        ComillaApertura,
        ComillaCierre
    },
    data() {
        return {
            mensaje1:'Hoy comienza nuestra aventura juntos, uniendo nuestros corazones en un solo latido. Nos llena de alegría compartir este día tan especial rodeados del amor de nuestra familia y amigos.'
        }
    }
}
</script>
<template>
    <div class="mensaje_container">
        <div class="mensaje_content">
            <div class="mensaje comillas">
                <p class="mensaje__txt">{{ mensaje1 }}</p>
            </div>
            <ComillaApertura class="comilla1" />
            <ComillaCierre class="comilla2" /> 
        </div>
    </div>

</template>

<style>
.mensaje_container {
    width: 100%;
    height: 300px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.puntilla {
    width: 100%;
    height: 100%;
    position:relative;
}

.msj_content_text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position:relative;
    width: 100%;
    height: 100%;
}

.mensaje_content{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: absolute;
    width:70%;
    height: 300px;
}
.mensaje__txt{
    color:var(--color__font_primary);
    font-size: var(--font-size-12);
    font-family: Montserrat;
    text-align: center;
    margin: 0;
}
.mensaje comillas{
    position:relative;
    width: 100%;
    height:80%;
    border:1px solid blue;
}
.comilla1,
.comilla2{
    position: absolute;
    left: 50%;
}
.comilla1{
    margin-top: 3.5rem;
    top:0;
}
.comilla2{
    bottom:0;
    margin-bottom: 3.5rem;
}
@media (min-width: 768px) and (max-width: 991px) {
    .mensaje_container {
        width: 100%;
        height:450px;
        
    }
    .mensaje__txt{
        font-size: var(--font-size-24);
    }
    .mensaje_content{
        width:80%;
        height: 400px;
    }
    .comilla1{
        margin-bottom: 1rem;
    }
    .comilla2{
        margin-bottom: 3rem;
    }
}
@media (min-width: 1025px) {
    .mensaje_container {
        width: 90%;
        height: 40%;
    }
    .mensaje__txt{
        font-size: var(--font-size-28);
    }
    .mensaje_content{
        width:80%;
        height: 75%;
    }
    .comilla1{
        margin-top: 5rem;
    }
    .comilla2{
        margin-bottom:5rem;
    }
}
</style>