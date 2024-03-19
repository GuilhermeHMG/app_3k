<template>
  <div class="content">
    <div class="row">
      <div class="col back-circle">
          <a href="/inicio"><img src="../../assets/images/icons/back_circle.svg" /></a>
      </div>
      <div class="col-9">
        <h2>Produtos</h2>
      </div>
      <div class="col-2 button-add-prod d-grid">
        <button class="add-prod-button btn btn-light btn-sm" @click="goToEditor('new')"><i class="pi pi-user-plus relative-button"></i>Cadastrar Novo</button>
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
// import { StoreProducts } from '../../store/Products/StoreProducts';

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
          }
        ]
    };
  },
  methods: {
    async goToEditor(page){
      const novaRota = `${this.$router.currentRoute.value.path}/${page}`;

      // Navegando para a nova rota
      await this.$router.push({ path: novaRota });
    }
  }
};
</script>

<style scoped>
  .button-add-prod button {
    width: 100%;
    height: 80%;
    font-size: 16px;
    color: #414141;
    background-color: #FFFFFF;
    border-radius: 2px;
    border: 0.5px solid #CBCFDD;
  }

  .button-add-prod i {
    width: 1.5rem;
    margin-right: 5px;
    margin-bottom: 5px;
  }

  button.add-prod-button:hover {
    color: #FFF;
    background-color: #562873;
  }
</style>