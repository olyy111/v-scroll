# v-scroll
基于`better-scroll`滚动指令

## 安装
```
npm install v-scroll --save

```

## 立即使用
```javscript
import Vue from 'vue'
import vscroll from 'v-scroll'
Vue.use(vscroll)
```
```html
<div id="app" v-scroll>
    <div id="inner">
      //.....
    </div>
</div>
```
## 选项
- method: 指令创建时的钩子函数
- opts: 选项对象

```html
<div id="app" v-scroll="{method:appScroll, opts:appScrollOpts ">
    <div id="inner">
      
    </div>
</div>
```

```javscript
new Vue({
    data(){
        return {

            //这里设置选项对象
            appScrollOpts: {
                click: true,
                probeType: 3
            }
        }
    },
    methods: {
        appScroll(scroll){

            //滚动对象实例
            console.log(scroll)
        }
    }
}).$mount("#app")
```

选项对象参见[这里](https://github.com/ustbhuangyi/better-scroll/tree/master)