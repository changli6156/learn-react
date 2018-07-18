# learn-react
1、     npm  install  create-react-app  -g 
2、      用create-react-app  创建项目   
Create-react-app    &lt;项目名> 
3、启动       |     npm  run  start       或者用   yarn start 
4、你所关心的只有一个：就是src里面的东西 **import语句需要放到整个文件的开头
…………………………………………………………………………………………
关于react样式问题:
1.直接引入              这是老师推荐的方式        import ‘./xxx.css’            &lt;h2 className=”red”>&lt;/h2> 
2. styled-components     
这种引入方式也很好 |    npm i styled-components –D      
进行安装 然后在index.js中进行引入:   import  styled from ‘styled-components’; 
|     const Title = styled.h2`font-size:20px; text-align:center;`
3.想使用less   
默认create-react-app不支持less     
必须自己修改它的配置文件  
如何修改creat-react-app配置：          
1).运行一个命令                 
|     npm run eject        
拷贝一份配置文件，覆盖掉node_modulesj里面的配置         
2).修改               
｜       config/webpack.config.dev.js                
|         config/webpack.config.prod.js             安装loader:                    
|       npm install less-loader less -D     
4.    css module           自动生成css的名字的唯一性             默认css-loader,没有开启，只要开启               
需要加上参数：{ |   modules:true }              |    import Button from’./button.css’             
Button.button …………………………………………………………………………………………………………………………        
|    css module还有一种办法：           
|        react-scripts-cssmodules:  |                         
1.  |   create-react-app&lt;项目名> --scripts-version react-scripts-cssmodule                      
2.定义模块的css                      
|       button.css    这就是普通css                
|         Button.module.css     这就是一个css module
……………………………………………………………………………………………………………
|     props      校验props类型：      1开发环境dev    ,校验，并且提示      
2生产环境      ，   项目都上线了，校验时就没有提示了。
