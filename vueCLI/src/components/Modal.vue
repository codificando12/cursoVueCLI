<script setup>
    import { ref } from 'vue'
    
    const show = ref(false);

    function toggle(){
        show.value = !show.value  
    }


</script>

<template>

    <div>
        <button @click="toggle">
            Modal</button>
            <Teleport to="body">
            <div v-show="show" class="modal">
                <h1>Titulo</h1>
                <p>Lorem ipsum dolor</p>
                <button @click="toggle">Cerrar</button>
            </div>
        </Teleport>
        
    </div>

</template>