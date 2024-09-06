<script>
import PopupAsistencia from './PopupAsistencia.vue';
import PopupLocalizacion from './PopupLocalizacion.vue';
import IconFiesta from './icon/IconFiesta.vue';
import Boton from './Boton.vue';
export default{
    name:'SectionAsistencia',
    data(){
        return{
            title:'Fiesta',
            text:'Los esperamos en el Salón del Club. A. Agrario a las 21:30 hs.',
            popup:false,
            popup_:false
            
        }
    },
    components:{
        IconFiesta ,
        Boton,
        PopupAsistencia,
        PopupLocalizacion
    },
    methods: {
        togglePopUp(){
            this.popup = !this.popup
        },
        togglePopUp2(){
            this.popup_ = !this.popup_
        }         
    }
}
</script>
<template>
    <div id="asistencia" class="asistencia__conteiner container">
        <div class="asistencia_content">
            <IconFiesta />
            <h1 class="title_section_asistencia">{{ title }}</h1>
        </div>
        <div class="asistencia_description">
            <p class="detalle_asistencia">{{ text }}</p>
        </div>
        <div class="container__button">
            <PopupAsistencia v-show="popup" @close="togglePopUp()"/>
            <Boton label="CONFIRMAR ASISTENCIA" customClass="btn-mayor" @click="togglePopUp()"/>
        </div>
        <div class="container__button2">
            <PopupLocalizacion v-show="popup_" @close="togglePopUp2()"/>
            <Boton label="¿COMO LLEGAR?" customClass="btn-mayor" @click="togglePopUp()"/>
        </div>      
        
    </div>
</template>
<style>
.asistencia__conteiner{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width:100%;
    margin-bottom: 2rem;
}
.asistencia_content{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.title_section_asistencia{
    font-family: var(--family__font_primary);
    color:var(--color__font_primary);
    font-size: var(--font-size-32);
    font-weight: 700;
    margin-bottom: 1rem;
}
.detalle_asistencia{
    font-family: PlayfairDisplay-Italic;
    color:var(--color__font_sencondary);
    font-size: var(--font-size-18);
    text-align: center;
    font-weight: 100;
}
.asistencia_description{
    width:80%;
    height:100%;
}
.container__button{
    margin-bottom: 1rem;
}
@media (min-width: 768px) and (max-width: 991px) {
    .title_section_asistencia{
        font-size: var(--font-size-42);
    }
    .detalle_asistencia{
        font-size: var(--font-size-24);
    }
    .detalle_asistencia3{
    font-size: var(--font-size-18);
    }

}
@media (min-width: 1025px) {
    .title_section_asistencia{
        font-size: var(--font-size-64);
    }
    .detalle_asistencia{
        font-size: var(--font-size-24);
    }
    .detalle_asistencia3{
    font-size: var(--font-size-16);
    }
}
</style>