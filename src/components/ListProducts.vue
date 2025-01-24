<template>
    <div>
      <table>
        <thead>
          <tr>
            <th>Massas</th>
            <th>Cobertura</th>
            <th>Recheio</th>
            <th>Topping</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>
              <ul>
                <li v-for="(massa, index) in massas" :key="index">{{ massa }}</li>
              </ul>
            </td>
            <td>
              <ul>
                <li v-for="(cobertura, index) in coberturas" :key="index">{{ cobertura }}</li>
              </ul>
            </td>
            <td>
              <ul>
                <li v-for="(recheio, index) in recheios" :key="index">{{ recheio }}</li>
              </ul>
            </td>
            <td>
              <ul>
                <li v-for="(topping, index) in toppings" :key="index">{{ topping }}</li>
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
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 20px 0;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  th,
  td {
    padding: 12px;
    text-align: left;
    border: 1px solid #ddd;
  }
  
  th {
    background-color: #f4f4f4;
  }
  
  tbody tr:hover {
    background-color: #f9f9f9;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    margin-bottom: 5px;
  }
  </style>