<template>
  <app-layout>
    <template #header>
      <h2 v-if="dadosEditar" class="font-semibold text-xl text-gray-800 leading-tight">
        Editar
      </h2>
       <h2 v-else class="font-semibold text-xl text-gray-800 leading-tight">
        Cadastrar Projeto
      </h2>
      
      
    </template>
      <template #body>
           <div class="py-12">
        <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
         
          <div class="bg-white overflow-hidden shadow-xl sm:rounded-sm ajustePadding">
              <FormularioProjeto :autoPreencher = "dadosEditar" />
              
          </div>
        </div>
      </div>
         
      </template>
  </app-layout>
</template>
<style>

</style>


<script>
import AppLayout from "@/Layouts/AppLayout";
import FormularioProjeto from "@/Pages/components/FormularioProjeto";
export default {
  components: {
    AppLayout,
    FormularioProjeto

  },
  props:{
    dadosEditar: Object
  }
}
</script>