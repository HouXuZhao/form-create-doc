# DatePicker 日期选择器

#### Maker
```js
$formCreate.maker.date('活动日期','section_day',['2018-02-20', new Date()]).props({
    "type": "datetimerange",
    "placeholder":"请选择活动日期"
})
```

#### JSON
```json
{
    type: "DatePicker",
    field: "section_day",
    title: "活动日期",
    value: ['2018-02-20', new Date()],
    props: {
        "type": "datetimerange",
        "format": "yyyy-MM-dd HH:mm:ss",
        "placeholder":"请选择活动日期",
    }
}
```

参考:[Element_DatePicker](http://element-cn.eleme.io/#/zh-CN/component/date-picker),[Element_DateTimePicker](http://element-cn.eleme.io/#/zh-CN/component/date-time-picker)

**value**: `String | Array`

### DatePicker

#### props

| 参数              | 说明                                           | 类型     | 可选值                                                       | 默认值               |
| ----------------- | ---------------------------------------------- | -------- | ------------------------------------------------------------ | -------------------- |
| readonly          | 完全只读                                       | boolean  | —                                                            | false                |
| disabled          | 禁用                                           | boolean  | —                                                            | false                |
| editable          | 文本框可输入                                   | boolean  | —                                                            | true                 |
| clearable         | 是否显示清除按钮                               | boolean  | —                                                            | true                 |
| size              | 输入框尺寸                                     | string   | large, small, mini                                           | —                    |
| placeholder       | 非范围选择时的占位内容                         | string   | —                                                            | —                    |
| startPlaceholder | 范围选择时开始日期的占位内容                   | string   | —                                                            | —                    |
| endPlaceholder   | 范围选择时结束日期的占位内容                   | string   | —                                                            | —                    |
| type              | 显示类型                                       | string   | year/month/date/dates/ week/datetime/datetimerange/daterange | date                 |
| format            | 显示在输入框中的格式                           | string   | 见[日期格式](http://element-cn.eleme.io/#/zh-CN/component/date-picker#ri-qi-ge-shi) | yyyy-MM-dd           |
| align             | 对齐方式                                       | string   | left, center, right                                          | left                 |
| popperClass      | DatePicker 下拉框的类名                        | string   | —                                                            | —                    |
| pickerOptions    | 当前时间日期选择器特有的选项参考下表           | object   | —                                                            | {}                   |
| rangeSeparator   | 选择范围时的分隔符                             | string   | —                                                            | '-'                  |
| defaultValue     | 可选，选择器打开时默认显示的时间               | Date     | 可被`new Date()`解析                                         | —                    |
| defaultTime      | 范围选择时选中日期所使用的当日内具体时刻       | string[] | 数组，长度为 2，每项值为字符串，形如`12:00:00`，第一项指定开始日期的时刻，第二项指定结束日期的时刻，不指定会使用时刻 `00:00:00` | —                    |
| valueFormat      | 可选，绑定值的格式。不指定则绑定值为 Date 对象 | string   | 见[日期格式](http://element-cn.eleme.io/#/zh-CN/component/date-picker#ri-qi-ge-shi) | —                    |
| name              | 原生属性                                       | string   | —                                                            | —                    |
| unlinkPanels     | 在范围选择器里取消两个日期面板之间的联动       | boolean  | —                                                            | false                |
| prefixIcon       | 自定义头部图标的类名                           | string   | —                                                            | el-icon-date         |
| clearIcon        | 自定义清空图标的类名                           | string   | —                                                            | el-icon-circle-close |
| validateEvent    | 输入时是否触发表单的校验                       | boolean  | -                                                            | true                 |

#### Picker Options

| 参数           | 说明                                                         | 类型                           | 可选值 | 默认值 |
| -------------- | ------------------------------------------------------------ | ------------------------------ | ------ | ------ |
| shortcuts      | 设置快捷选项，需要传入 { text, onClick } 对象用法参考 demo 或下表 | Object[]                       | —      | —      |
| disabledDate   | 设置禁用状态，参数为当前日期，要求返回 Boolean               | Function                       | —      | —      |
| firstDayOfWeek | 周起始日                                                     | Number                         | 1 到 7 | 7      |
| onPick         | 选中日期后会执行的回调，只有当 `daterange` 或 `datetimerange` 才生效 | Function({ maxDate, minDate }) | —      | —      |



#### on 事件

| 事件名称 | 说明                    | 回调参数                                              |
| -------- | ----------------------- | ----------------------------------------------------- |
| change   | 用户确认选定的值时触发  | 组件绑定值。格式与绑定值一致，可受 `value-format`控制 |
| blur     | 当 input 失去焦点时触发 | 组件实例                                              |
| focus    | 当 input 获得焦点时触发 | 组件实例                                              |



### DateTimePicker

#### props

| 参数               | 说明                                           | 类型                                        | 可选值                                                       | 默认值               |
| ------------------ | ---------------------------------------------- | ------------------------------------------- | ------------------------------------------------------------ | -------------------- |
| readonly           | 完全只读                                       | boolean                                     | —                                                            | false                |
| disabled           | 禁用                                           | boolean                                     | —                                                            | false                |
| editable           | 文本框可输入                                   | boolean                                     | —                                                            | true                 |
| clearable          | 是否显示清除按钮                               | boolean                                     | —                                                            | true                 |
| size               | 输入框尺寸                                     | string                                      | large, small, mini                                           | —                    |
| placeholder        | 非范围选择时的占位内容                         | string                                      | —                                                            | —                    |
| startPlaceholder  | 范围选择时开始日期的占位内容                   | string                                      | —                                                            | —                    |
| endPlaceholder    | 范围选择时结束日期的占位内容                   | string                                      | —                                                            | —                    |
| timeArrowControl | 是否使用箭头进行时间选择                       | boolean                                     | —                                                            | false                |
| type               | 显示类型                                       | string                                      | year/month/date/week/ datetime/datetimerange/daterange       | date                 |
| format             | 显示在输入框中的格式                           | string                                      | 见[日期格式](http://element-cn.eleme.io/#/zh-CN/component/date-picker#ri-qi-ge-shi) | yyyy-MM-dd           |
| align              | 对齐方式                                       | string                                      | left, center, right                                          | left                 |
| popperClass       | DateTimePicker 下拉框的类名                    | string                                      | —                                                            | —                    |
| pickerOptions     | 当前时间日期选择器特有的选项参考下表           | object                                      | —                                                            | {}                   |
| rangeSeparator    | 选择范围时的分隔符                             | string                                      | -                                                            | '-'                  |
| defaultValue      | 可选，选择器打开时默认显示的时间               | Date                                        | 可被`new Date()`解析                                         | —                    |
| defaultTime       | 选中日期后的默认具体时刻                       | 非范围选择时：string / 范围选择时：string[] | 非范围选择时：形如`12:00:00`的字符串；范围选择时：数组，长度为 2，每项值为字符串，形如`12:00:00`，第一项指定开始日期的时刻，第二项指定结束日期的时刻。不指定会使用时刻 `00:00:00` | —                    |
| valueFormat       | 可选，绑定值的格式。不指定则绑定值为 Date 对象 | string                                      | 见[日期格式](http://element-cn.eleme.io/#/zh-CN/component/date-picker#ri-qi-ge-shi) | —                    |
| name               | 原生属性                                       | string                                      | —                                                            | —                    |
| unlinkPanels      | 在范围选择器里取消两个日期面板之间的联动       | boolean                                     | —                                                            | false                |
| prefixIcon        | 自定义头部图标的类名                           | string                                      | —                                                            | el-icon-date         |
| clearIcon         | 自定义清空图标的类名                           | string                                      | —                                                            | el-icon-circle-close |

#### Picker Options

| 参数           | 说明                                                         | 类型     | 可选值 | 默认值 |
| -------------- | ------------------------------------------------------------ | -------- | ------ | ------ |
| shortcuts      | 设置快捷选项，需要传入 { text, onClick } 对象用法参考 demo 或下表 | Object[] | —      | —      |
| disabledDate   | 设置禁用状态，参数为当前日期，要求返回 Boolean               | Function | —      | —      |
| firstDayOfWeek | 周起始日                                                     | Number   | 1 到 7 | 7      |



#### on 事件

| 事件名称 | 说明                    | 回调参数                                               |
| -------- | ----------------------- | ------------------------------------------------------ |
| change   | 用户确认选定的值时触发  | 组件绑定值。格式与绑定值一致，可受 `value-format` 控制 |
| blur     | 当 input 失去焦点时触发 | 组件实例                                               |
| focus    | 当 input 获得焦点时触发 | 组件实例                                               |

