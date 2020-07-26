<template>
  <div>
      <common-table :sortable="true" @filterHandler2="filterHandler2" :filterMultiple="false" style="width: 100%" :tableData="tableData" :cloumns="cloumns"/>
  </div>
</template>

<script>
import CommonTable from '@/components/table/index.vue'
export default {
  name: 'Index',
  components: {
    CommonTable,
  },
  data() {
    return {
        cloumns:[
            {
                prop:'name',
                label:'姓名',
                width:'100',
                id:'1',
                filters:[{text: '隐藏', value: '隐藏'}, {text: '前置', value: '前置'}, {text: '后置', value: '后置'}]
            },
            {
                prop:'date',
                label:'日期',
                width:'100',
                id:'2',
                filters:[{text: '隐藏', value: '隐藏'}, {text: '前置', value: '前置'}, {text: '后置', value: '后置'}]
            },
            {
                prop:'address',
                label:'地址',
                width:'100',
                id:'3',
                filters:[{text: '隐藏', value: '隐藏'}, {text: '前置', value: '前置'}, {text: '后置', value: '后置'}]
            },

        ],
      tableData: [{
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄',
          tag: '家'
        }, {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1517 弄',
          tag: '公司'
        }, {
          date: '2016-05-01',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1519 弄',
          tag: '家'
        }, {
          date: '2016-05-03',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1516 弄',
          tag: '公司'
        }]
    }
  },
  methods: {
      filterHandler2(value, row, column) {
          debugger;
          if(value === '0') {

          } else if(value === '1') {

          } else if(value === '2') {
              
          }
      }
  }
}
</script>

<style lang="scss" scoped>

</style>
