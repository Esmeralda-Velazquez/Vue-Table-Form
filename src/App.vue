<template>
  <link rel="stylesheet" href="https://unpkg.com/primitive-ui/dist/css/main.css" />
  <div id="app" class="small-container">
    <h1>Form</h1>
    <!-- Pasar el arreglo de empleados como prop a EmployeeForm -->
    <employee-form :employees="employees" />
    <h1>Employees</h1>
    <!-- Pasar el arreglo de empleados como prop a EmployeeTable -->
    <employee-table :employees="employees" />
  </div>
</template>

<script>
import EmployeeTable from '@/components/EmployeeTable.vue';
import EmployeeForm from '@/components/EmployeeForm.vue';

export default {
  name: 'HelloWorld',
  components:{
    EmployeeTable,
    EmployeeForm
  },
  data() {
    return {
      employees: [ 
        { name: 'Richard Hendricks', email: 'richard@piedpiper.com' },
        { name: 'Bertram Gilfoyle', email: 'gilfoyle@piedpiper.com' },
        { name: 'Dinesh Chugtai', email: 'dinesh@piedpiper.com' }
      ]
    };
  },
  methods: {
    editEmployee(rowData) {
      console.log('Editar empleado:', rowData);
    },
    deleteEmployee(rowData) {
      console.log('Eliminar empleado:', rowData);
    }
  }
}
</script>

<style></style>
