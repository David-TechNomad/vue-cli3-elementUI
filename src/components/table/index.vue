<template>
  <el-table
    ref="filterTable"
    :data="tableData"
    style="width: 100%">
    <template v-for="item in cloumns">
        <el-table-column
        :prop="item.prop"
        :label="item.label"
        :sortable="sortable"
        :filters='item.filters'
        :filter-method="filterHandler"
        :filter-multiple='filterMultiple'
        :filter-change="filterChange"
        >
        </el-table-column>
    </template>
  </el-table>
</template>

<script>
  export default {
    name: 'CommonTable',
    props: {
        tableData: {
            type: Array,
        },
        sortable:Boolean,
        filterMultiple:Boolean,
        cloumns:{
            type: Array,
        },
    },
    methods: {
      filterHandler(value, row, column) {
          debugger;
          let columnId = column.id.split('_');
          if(value === '隐藏') {
              this.cloumns.forEach((item,index)=> {
                  if(item.id === columnId[columnId.length - 1]) {
                      this.cloumns.splice(index,1);
                  }
              })
           }
        //   this.$emit('filterHandler2',value, row, column)
      },
      filterChange(value, row, column) {
          debugger;
      }
    }
  }
</script>
