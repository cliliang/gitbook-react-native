1、[react-navigation](https://reactnavigation.org/)官方主页。

2、react-navigation库的安装：
`yarn add react-navigation`，
在项目中导入:
```js
import {
    StackNavigator
} from 'react-navigation'
```

3、StackNavigator的定义
```js
const App = StackNavigator({
    //定义RouteConfigs
    Home:{
        screen:HomePage,
        path:'people/:name',
        navigationOptions:{
            //如果在此处定义了统一的navigationOptions，会覆盖页面内定义的
        }
    },
    Chat:{
        screen:ChatPage
        ...other Route Configs
    }
},{
    //NavigatorConfigs
    //Stack栈中默认的界面，必须是已经配置的Router中的一个
    initialRouterName:'Home',
    //初始化的参数
    initialRouterParams:{},
    //会覆盖在RouterConfigs内的path
    paths:'',
    //新界面出现的模式，只在IOS中才会作用。"card:页面左右出现", "modal:页面从下方出现"
    mode:'card',
    //导航头部的模式，"float:透明，只在IOS才会有作用" "screen:不透明的，也是Android默认的样式" "none:不会出现"
    headerMode:'float',
    //定义此Style，页面的样式会被重写
    cardStyle:{
        backgroundColor:'#305',
    },
    //方法，在页面跳转时会被调用
    onTransitionStart:()=>{},
    //方法，在页面跳转后会被调用
    onTransitionEnd:()=>{},
    //默认的Navigator样子
    navigationOptions:{
        title:'Homi',
        //返回一个组件或方法，如果定义了此header，以下的headerTitle、headerRight等都不起作用了，这是一个可以完
        //成自定义Natigator的。__null__，就不会显示header
        header{
            <View style={{
                height:45,
                backgroundColor:'#fff',
                justifyContent:'space-between',
                alignItem:'center'
            }}>
            ...<View>...
            </View>
        },
        //以前起作用，都是在没有定义header的前提下
        headerStyle:{
            height:45,
            backgroundColor:''
        },
        headerTitle:'defaultTitle',
        headerTitleStyle:{}
        //返回一个组件，出现在Header的左边
        headerLeft:<View style={{}}>,
        headerRight:<View style={{}}>,
        //在IOS中，是否允许右滑关闭界面
        gesturesEnable:true
    }
    
});
```