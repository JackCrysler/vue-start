
v-bind
v-bind:属性名=属性值

v-on 简写方式 @
v-on:事件名=执行方法

在视图中输出值
{{ 变量名 }}

**一个实例就是由数据驱动的生命体**

    特征：
    el: 挂在元素，决定当前vue的控制范围
    data: 对象
    template: 模板
    computed: 计算属性
    methods: 方法的集合
    filters: 过滤器
    components: 局部组件
    watch: 监听数据变化

    生命周期：
    beforeCreate 创建之前
    created 创建完成 （关联数据，初始化事件）
    beforeMount  dom生成之前
    mount dom生成
    （beforeUpdate  updated） 如果数据更新了，则会触发update生命周期
    一般配合路由
    beforeDestroy
    destroyed


vue组件特征：
    基本同vue实例一样
    另外
        props:数组、对象 
        data:function(){ //函数
            return {

            }
        }




