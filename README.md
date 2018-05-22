### 命令行启动项目

    java -jar target/girl-0.0.1-SNAPSHOT.jar --spring.profiles.active=dev
    
    java -jar target/girl-0.0.1-SNAPSHOT.jar --spring.profiles.active=prod
    
#### 注解

    @RestController  新的
    
    ===  @Controller @ResponseBody
    
    @RequestMapping(value="", method=)   // 配置路由映射
    
    
路由映射嵌套

    在整个Controller外层加  @RequestMapping("/父路由")
    在 Controller 中每个方法前加  @RequestMapping(value="/子路由", method= RequestMethod.GET)
    如不指定method，get post 请求均可以获取结果，但不推荐这种做法
    
处理 url 参数

    @PathVariable   获取url中的参数     params类  /id/xx/xx
    @RequestParam   获取请求参数的值     querystring  参数  ?id=xxx
    
    非必选参数，并设置默认什
    @RequestParam(value="id", required="false", defaultValue="0")
    
    @GetMapping     组合注解  对上面 @RequestMapping的简写