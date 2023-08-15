<template>
    <div class="weird-header">
        <template v-for="item in headers" :key="item">
            <div class="weird-header__item">
                {{ item }}
            </div>
        </template>
    </div>
    <WeirdTable :datas="datas" >
        <template
        #item="{
          id,name,age
        }"
      >
      <WeirdRow :data="{ id,name,age }" />  
    </template>
    </WeirdTable>
</template>
    
<script setup lang="ts">
import WeirdTable from './WeirdTable.vue';
import WeirdRow from './WeirdRow.vue';
const headers = [
    'Id',
    'Name',
    'Age',
    'Actions'
]
const datas = [
    {
        'id': 1,
        'name': 'Nassim',
        'age': 8
    },
    {
        'id': 2,
        'name': 'Nassim',
        'age': 18

    },
    {
        'id': 3,
        'name': 'Nassim',
        'age': 25
    }
]


</script>
    
<style scoped>
.weird-table {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding-top: 1rem;

}
.weird-header {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    text-align: left;
    justify-content: space-between;
    align-items: center;
    background-color: #f5f5f5;
    color: black;
    border-radius: 5px;
    font-weight: bold;
    padding: 1rem;

}

.weird-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    text-align: left;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    background-color: #f5f5f5;
    color: black;
    border-radius: 5px;

    
}
</style>
    