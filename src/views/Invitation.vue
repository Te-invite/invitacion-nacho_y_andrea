<script>
import SectionPortada from '@/components/Sesiones/SectionPortada.vue';
import Cuadrante from '@/components/timer/Cuadrante.vue';
import IconFlorRight1 from '@/components/icon/IconFlorRight1.vue';
import IconFlor2 from '@/components/icon/IconFlor2.vue';
import IconFlorBottom from '@/components/icon/IconFlorBottom.vue';
import IconFlorLeft from '@/components/icon/IconFlorLeft.vue';
import SectionMensaje from '@/components/Sesiones/SectionMensaje.vue';
import SectionAsistencia from '@/components/Sesiones/SectionAsistencia.vue';
import SectionLugarVue from '@/components/Sesiones/SectionLugar.vue.vue';
import SectionDress from '@/components/Sesiones/SectionDress.vue';
import SectionGift from '@/components/Sesiones/SectionGift.vue';
import SectionMusic from '@/components/Sesiones/SectionMusic.vue';
import Carrousel from '@/components/Carrousel.vue';
import SectionRedes from '@/components/Sesiones/SectionRedes.vue';
import SectionFooter from '@/components/Sesiones/SectionFooter.vue';
import SectionTarjeta from '@/components/Sesiones/SectionTarjeta.vue';
import IconFlorTop from '@/components/icon/IconFlorTop.vue';

export default {
    name: 'Invitation',
    components: {
        SectionPortada,
        Cuadrante,
        IconFlorRight1,
        IconFlor2,
        IconFlorBottom,
        IconFlorLeft,
        SectionMensaje,
        SectionAsistencia,
        SectionLugarVue,
        SectionDress,
        SectionGift,
        SectionMusic,
        Carrousel,
        SectionRedes,
        SectionFooter,
        SectionTarjeta,
        IconFlorTop 
    }

}
</script>
<template>
    <div class="container__invitacion container">
        <div class="content_invitacion">
            <div class="box1">
                <SectionPortada class="portada"/>
                <IconFlorRight1 class="flower_right1"/>
            </div>
            <!----------------------------------------------->
            <div class="box2">
                <Cuadrante />
                <IconFlor2  class="flower_right2"/>
            </div>
        </div>
        <!----------------------------------------------->
        <div class="box3">
            <SectionMensaje />
            <IconFlorLeft class="flower_left1"/>
        </div>
        <!----------------------------------------------->
        <div class="box4">
            <SectionLugarVue />
        </div>
        <!----------------------------------------------->
        <div class="box5">
            <SectionAsistencia />
        </div>
        <!----------------------------------------------->
        <div class="box_carousel">
            <Carrousel />
            <IconFlorBottom class="flower_bottom"/>
        </div>
        <!----------------------------------------------->
        <div class="box6">
            <SectionTarjeta />
        </div>
        <!----------------------------------------------->
        <div class="box7">
            <IconFlorTop class="flower_top"/>
            <SectionDress />
        </div>
        <!----------------------------------------------->
        <div class="box8">
            <SectionGift />
        </div>
        <!----------------------------------------------->
        <div class="box9">
            <SectionMusic />
        </div>
        <!----------------------------------------------->
        <div class="box11">
            <SectionRedes/>
        </div>
        <!----------------------------------------------->
        <div class="box_section">
                <a href="#asistencia" class="opcion_menu">Confirmar Asistencia</a>
                <a href="#lugar" class="opcion_menu">¿Como llegar?</a>
                <a href="#hospedaje" class="opcion_menu">Hospedaje</a>
                <a href="#dress" class="opcion_menu">Dress</a>
                <a href="#regalo" class="opcion_menu">Regalo</a>
                <a href="#musica" class="opcion_menu">Sugerir Canción</a>
            </div>
        <div class="box12">
            <SectionFooter/>
        </div>
    </div>
</template>
<style>
.container__invitacion {
    min-width: 100%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}


.content_invitacion {
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.box1,
.box2,
.box3,
.box4,
.box5,
.box6,
.box7,
.box8,
.box10,
.box11,
.box12 {
    width: 100%;
    display: flex;
    justify-content: center;

}

.box10 {
    height: 50%;
}

.box3,
.box4,
.box5,
.box6,
.box7,
.box8,
.box9,
.box_carousel {
    margin-top: 1rem
}

.box1,
.box2,
.box3,
.box_carousel,
.box7{
    position: relative;
}

.flower_right1,
.flower_right2,
.flower_left1,
.flower_bottom,
.flower_top {
    position: absolute;
    z-index: 2;
}

.flower_right1{
    right: -90px;
    top:8px;
    width: 100%;
    height: 100px;
}
.flower_right2{
    right: -20px;
    bottom:-100px;
    width: auto;
    height: 100%;
}
.flower_left1{
    left: -20px;
    bottom:-100px;
    width: auto;
    height: 100%;
}
.flower_bottom{
    right: 0px;
    bottom:-130px;
    width: auto;
    height: 100%;
}
.flower_top{
    left: -20px;
    top:-75px;
    width: 100%;
    height: auto;
}
.box_carousel {
    position: relative;
}

.box12{
    margin-top:1rem;
}
.box_section{
    display:flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}
.box_section{
    font-size:.5rem;
}
.opcion_menu{
    margin-left:.3rem;
    font-family: var( --family__font_secondary);
    color:var(--color__font_primary);
    text-decoration: none;
}
@media (min-width: 768px) and (max-width: 991px) {
    .content_invitacion {
        width: 100vw;
        padding: 0;
    }

    .box1 {
        width: 100%;
    }

    .curv_right {
        right: 0;
    }

}

@media (min-width: 1025px) {
    .content_invitacion {
        width: 100vw;
    }

    .curv_right {
        right: 0;
    }
    .box_section{
        font-size:1rem;
    }
    .box12{
        margin-top:.5rem;
    }
    .opcion_menu{
        margin-right:1rem;
    }
}
</style>