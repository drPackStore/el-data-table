search表单折叠并且设置部分总是可见

```vue
<template>
  <el-data-table v-bind="$data" ref="table" />
</template>
<script>
export default {
  data() {
    return {
      url: 'https://mockapi.eolinker.com/IeZWjzy87c204a1f7030b2a17b00f3776ce0a07a5030a1b/el-data-table?q=basic',
      columns: [
        {prop: 'date', label: '日期'},
        {prop: 'name', label: '姓名'},
        {prop: 'address', label: '地址'},
      ],
      searchForm: [
        {
          type: 'input',
          id: 'name',
          label: '',
          collapsible: false,
          el: {placeholder: '请输入用户名'}
        },
        {
          type: 'select',
          id: 'area',
          label: '',
          remote: {
            url: 'https://mockapi.eolinker.com/IeZWjzy87c204a1f7030b2a17b00f3776ce0a07a5030a1b/el-form-renderer?q=remote',
          }
        },
        {
          type: 'select',
          id: 'age',
          label: '',
          el: {
            placeholder: '请输入年龄'
          },
          options: [
            {
              value: 17
            },
            {
              value: 18
            }
          ]
        },
        {
          type: 'input',
          id: 'favorite',
          label: '',
        },
        {
          type: 'input',
          id: 'wishTravel',
          label: ''
        },
        {
          type: 'select',
          id: 'lived',
          label: '',
          options: [
            {
              label: '三番',
              value: 'San Francisco'
            }
          ]
        }
      ],
      canSearchCollapse: true
    }
  }
}
</script>
```
