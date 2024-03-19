<template>
    <div class="content">
      <div class="row">
        <div class="col back-circle">
            <a href="/inicio"><img src="../../assets/images/icons/back_circle.svg" /></a>
        </div>
        <div class="col-9">
          <h2>Cadastro de Produto</h2>
        </div>
      </div>
      <div class="row">
        <div class="col back-circle">
        </div>
        <div class="col-12">
          <Breadcrumb :home="home" :model="items" />
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import { useRouter } from 'vue-router';
  
  // Importa os Stores
//   import { StoreProducts } from '../../store/Products/StoreProducts';
  
  export default {
    setup(){
          const router = useRouter()
      },
    data() {
        return {
            items: [
                {
                  label: 'Início',
                  command: () => {
                    this.$router.push('/inicio');
                  }
                },
                {
                  label: 'Produtos',
                  command: () => {
                    this.$router.push('/products');
                  }
                },    
                {
                  label: 'Cadastro de Produto',
                  command: () => {
                    this.$router.push('/products/new');
                  }
                }
            ]
        };
    },
    methods: {}
  };
  </script>
  <style scoped>
  
    
  </style>