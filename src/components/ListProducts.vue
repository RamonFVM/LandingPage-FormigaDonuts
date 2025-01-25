<template>
  <div class="table-container">
    <table class="w-1/2 border-collapse shadow-md my-5">
      <thead>
        <tr>
          <th class="bg-[#ffffd0] p-2 text-left border border-gray-300">Massas</th>
          <th class="bg-[#ffffd0] p-2 text-left border border-gray-300">Cobertura</th>
          <th class="bg-[#ffffd0] p-2 text-left border border-gray-300">Recheio</th>
          <th class="bg-[#ffffd0] p-2 text-left border border-gray-300">Topping</th>
        </tr>
      </thead>
      <tbody>
        <tr class="hover:bg-gray-50">
          <td class="p-2">
            <ul class="list-none p-0 m-0 flex flex-col">
              <li v-for="(massa, index) in massas" :key="index" class="mb-1 text-sm leading-6">{{ massa }}</li>
            </ul>
          </td>
          <td class="p-2">
            <ul class="list-none p-0 m-0 flex flex-col">
              <li v-for="(cobertura, index) in coberturas" :key="index" class="mb-1 text-sm leading-6">{{ cobertura }}</li>
            </ul>
          </td>
          <td class="p-2">
            <ul class="list-none p-0 m-0 flex flex-col">
              <li v-for="(recheio, index) in recheios" :key="index" class="mb-1 text-sm leading-6">{{ recheio }}</li>
            </ul>
          </td>
          <td class="p-2">
            <ul class="list-none p-0 m-0 flex flex-col">
              <li v-for="(topping, index) in toppings" :key="index" class="mb-1 text-sm leading-6">{{ topping }}</li>
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
}

table {
  width: 38%; 
  border-collapse: collapse;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  margin: 20px 0;
  height: 30%;
}

th, td {
  padding: 8px;
  text-align: left;
  border: 1px solid #ddd;
}

tbody tr:hover {
  background-color: #f9f9f9;
}

ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
  height: 100%;
  display: flex;
  flex-direction: column;
}

li {
  margin-bottom: 5px;
  font-size: 0.9rem;
  line-height: 1.8;
}

th {
  text-align: center;
}

td {
  text-align: left;
}

th, td {
  vertical-align: top;
}
</style>