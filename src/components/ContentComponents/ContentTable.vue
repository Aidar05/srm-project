<template>
  <table>
    <!-- Названия колон таблицы -->
    <tr class="row">
      <th v-for="(header, index) in tableData[0]" :key="index" class="column-names">
        {{ header }}
      </th>
    </tr>

    <!-- Элементы таблицы -->
    <tr v-for="(row, index) in tableData.slice(1)" :key="index" class="row">
      <td v-for="(value, key) in Object.entries(row).slice(0, -1)" :key="key" class="row-element">
        {{ value[1] }}
      </td>
    </tr>
  </table>
</template>

<script>
export default{
  name: "ContentTable",
  props: {
    tableData: Array
  }
}
</script>