<template>
  <div>
    <DataTable />
    <AddUser />
  </div>
</template>

<script>
import DataTable from './components/DataTable.vue';
import AddUser from './components/AddUser.vue';

export default {
  name: 'App',

  components: {
    DataTable,
    AddUser,
  },

  data: () => ({
    //
  }),
};
</script>
