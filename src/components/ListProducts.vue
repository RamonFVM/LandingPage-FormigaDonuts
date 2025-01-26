<template>
  <div class="table-container relative rounded-2xl">
    <table class="w-full sm:w-3/4 border-collapse shadow-md my-5 relative z-10">
      <thead>
        <tr>
          <th class="bg-[#ffffd0] p-4 sm:p-6 text-left border font-sans text-xl sm:text-3xl border-gray-300">Massas</th>
          <th class="bg-[#ffffd0] p-4 sm:p-6 text-left border font-sans text-xl sm:text-3xl border-gray-300">Cobertura</th>
          <th class="bg-[#ffffd0] p-4 sm:p-6 text-left border font-sans text-xl sm:text-3xl border-gray-300">Recheio</th>
          <th class="bg-[#ffffd0] p-4 sm:p-6 text-left border font-sans text-xl sm:text-3xl border-gray-300">Topping</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="p-2">
            <ul class="list-none p-0 m-0 flex flex-col">
              <li v-for="(massa, index) in massas" :key="index" class="mb-2 text-sm sm:text-lg leading-6">
                <div class="flex items-center">
                  <img :src="require('@/assets/donuts.png')" class="rotating-image" alt="Mini Donut" />
                  <span class="ml-2">{{ massa }}</span>
                </div>
              </li>
            </ul>
          </td>
          <td class="p-2">
            <ul class="list-none p-0 m-0 flex flex-col">
              <li v-for="(cobertura, index) in coberturas" :key="index" class="mb-2 text-sm sm:text-lg leading-6">
                <div class="flex items-center">
                  <img :src="require('@/assets/donuts.png')" class="rotating-image" alt="Mini Donut" />
                  <span class="ml-2">{{ cobertura }}</span>
                </div>
              </li>
            </ul>
          </td>
          <td class="p-2">
            <ul class="list-none p-0 m-0 flex flex-col">
              <li v-for="(recheio, index) in recheios" :key="index" class="mb-2 text-sm sm:text-lg leading-6">
                <div class="flex items-center">
                  <img :src="require('@/assets/donuts.png')" class="rotating-image" alt="Mini Donut" />
                  <span class="ml-2">{{ recheio }}</span>
                </div>
              </li>
            </ul>
          </td>
          <td class="p-2">
            <ul class="list-none p-0 m-0 flex flex-col">
              <li v-for="(topping, index) in toppings" :key="index" class="mb-2 text-sm sm:text-lg leading-6">
                <div class="flex items-center">
                  <img :src="require('@/assets/donuts.png')" class="rotating-image" alt="Mini Donut" />
                  <span class="ml-2">{{ topping }}</span>
                </div>
              </li>
            </ul>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      massas: ["Baunilha", "Chocolate"],
      coberturas: ["Chocolate ao leite", "Chocolate branco"],
      recheios: [
        "Brigadeiro 50%",
        "Brigadeiro branco",
        "Brigadeiro de leite em pó",
        "Doce de leite",
        "Nutella"
      ],
      toppings: [
        "Granulado duo",
        "Granulado colorido",
        "Amendoim triturado",
        "Nutella",
        "Confete",
        "Chocoball"
      ]
    };
  }
};
</script>

<style scoped>
.table-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  position: relative;
}

table {
  width: 50%; 
  border-collapse: collapse;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  margin: 20px 0;
  z-index: 10;
}

th,
td {
  padding: 8px;
  text-align: left;
  border: 1px solid #ddd;
}

ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
}

li {
  margin-bottom: 5px;
  font-size: 1.5rem;
  line-height: 1.8;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

th {
  text-align: center;
}

td {
  text-align: left;
}

th,
td {
  vertical-align: top;
}

@keyframes rotate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

.rotating-image {
  width: 30px;
  height: 30px;
  animation: rotate 5s infinite linear;
}

.ml-2 {
  margin-left: 8px;
}


@media (max-width: 768px) {
  th,
  td {
    padding: 4px;
  }

  .rotating-image {
    width: 25px;
    height: 25px;
  }

  .text-sm {
    font-size: 1rem; 
  }

  .text-lg {
    font-size: 1.2rem; 
  }

  .w-full {
    width: 100%; 
  }
}

@media (max-width: 480px) {
  th,
  td {
    padding: 2px; 
  }

  .text-sm {
    font-size: 0.9rem;
  }

  .text-lg {
    font-size: 1.1rem;
  }
}
</style>