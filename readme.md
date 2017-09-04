
* v-bind 简写方式 ":"

    v-bind:属性名=属性值

* 在视图中输出值

    {{ 变量名 }}

* v-on 简写方式 @

    v-on:事件名=执行方法


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
    beforeUpdate
    updated (如果数据更新了，则会触发update生命周期一般配合路由)
    beforeDestroy
    destroyed

    这里面没有包含 keep-alive 时的两个生命周期，原因很简单：我们没有用到过。

**vue组件**

    特征：(基本同vue实例一样)
    props:数组、对象 
    data:function(){ //函数(组件和实例对于data的定义有区别)
        return {

        }
    }

    生命周期：（与vue实例相同，参考vue实例的生命周期）

**vuex**

    首先明白两个概念：视图容器和数据容器。

    视图容器：通过 new Vue() 所创建的实例以及通过 Vue.Component() 所定义的组件都是视图容器

    数据容器：通过 new Vuex() 所创建的store则是数据容器，这个store一旦注入到vue的实例，所有视图能够获取store的数据，无论这个数据是在哪一个组件中用，这就是所谓的时光旅行（time travel）。

    使用方法：

        store是一个数据容器，本质是一个JavaScript对象，有4个规定的属性：state、 mutations、 actions、 getters。

        1. 容器的数据都存放在state中。
        
        视图直接获取state的值使用 $store.[属性名]即可。如果想要对数据做一定的处理再返回使用getters，调用方式$store.getters.[getter名]即可。

        2. 无论通过哪种方式，要改变state的值最终必须通过mutations。 调用方式如：$store.commit('mutations-name',data)。

        mutations只能做同步的数据操作。

        3. actions用来做异步操作。
        
        actions通过分发一个mutations来达到修改state的目的，不可以直接修改state。调用方式如：$store.dispatch('actions-name',data)。

        总之：

                                              =>$store.[属性名]（获取数据）
        修改数据：actions =>mutations =>state--
                                              =>$store.getters.[getter名]（获取数据）



欢迎补充。


