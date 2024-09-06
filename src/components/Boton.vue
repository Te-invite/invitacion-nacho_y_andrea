<script>
export default{
    name:'Boton',
    props: {
    label: {
      type: String,
      required: false 
    },
    customClass: {
      type: String,
      default: 'btn-mayor'
    }
  }

}
</script>
<template>
   <button type="button" :class="['btn', customClass, 'btn-lg']">
      {{ label }}
    </button>
</template>
<style>
.btn-mayor{
    width: 300px;
    background: transparent;
    color:var(--color_font_btn);
    border: 1px solid var(--line__buttom);
    font-family: Display-regular;
    font-size: var(--font-size-18);
    padding: .75rem 1rem;
}
.btn-mayor:hover{
    background:var(--color_font_btn);
    color:var(--font-light);
}
</style>