<template>
  <div class="card mb-4 border border-info">
      <div class="card-body bg-info">
          <h5 class="text-center h3">{{pais.name}}</h5>
          <p class="text-center">
              <img :src="pais.flag" class="img-fluid w-25" :alt="`bandera de ${pais.name}`">
          </p>
          <p class="card-text">
              <span class="badge badge-dark d-block mb-1">Native Name: {{pais.nativeName}}</span>
              <span class="badge badge-dark d-block mb-1">Capital: {{pais.capital}}</span>
              <span class="badge badge-dark d-block mb-1">Region: {{pais.region}}</span>
              <span class="badge badge-info p-3 d-block mb-1">Population: {{numeroFormateado(pais.population)}}</span>
          </p>
      </div>
  </div>
</template>

<script>
export default {
    props: ['pais'],
    setup() {
        const numeroFormateado = (n) =>  new Intl.NumberFormat("de-DE").format(n)
        return {
            numeroFormateado
        }
    }
}
</script>
