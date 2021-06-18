<template>
    <div class="text-center">
        <h3>Filtrar por continentes</h3>
        <div class="btn-group mb-3">
            <button class="btn btn-dark" @click="filtro('Americas')">AME</button>
            <button class="btn btn-dark" @click="filtro('Europe')">EUR</button>
            <button class="btn btn-dark" @click="filtro('Asia')">ASI</button>
            <button class="btn btn-dark" @click="filtro('Oceania')">OCE</button>
            <button class="btn btn-dark" @click="filtro('Africa')">AFR</button>
            <button class="btn btn-dark" @click="filtro('')">ALL</button>
        </div>
    </div>
</template>

<script>
import { useStore } from 'vuex'
export default {
    setup() {
        const store = useStore()
        
        const filtro = (region) => {
            store.dispatch('filtrarRegion',region)
        }

        return {
            filtro
        }
    }
}
</script>
