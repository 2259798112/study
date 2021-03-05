1. IOC 字面意思 控制反正，是Spring 框架的一种设计思想。
对象资源的管理交付给Spring 容器。

https://www.cnblogs.com/xdyixia/p/9347911.html

IoC和DI是Spring的两个核心概念，很多人都把它们视为相同的东西，但事实并非如此。

IoC(Inversion of Control)：控制反转。

DI(Dependency Injection)：依赖注入。
  
控制反转是目的，依赖注入是实现控制反转的手段。
控制反转是一种面向对象的思想，它是一种宽泛的概念，只要一个类将对它内部状态的控制权交由其他机制去完成即为『控制反转』。控制反转是为了降低类与类之间的耦合度。
而Spring采用依赖注入这一具体的手段来达到控制反转的目的。

当我们需要使用某个 Bean 时，容器会自动帮我们创建，并在适当时销毁。还有一种情况，当某个 Bean 中需创建另一个 Bean 时，也就是 Bean 之间有依赖关系，这种依赖的 Bean 也是由容器自动创建。在外界有一个标准的名词，前者称呼为 IOC，也就是控制反转，后者称呼为 DI，也就是依赖注入。

### 注入类型
- byName
- byType重复配置会错

@Qualifier(“ID”)会根据bean的id为father装配。

`<bean class="com.Hi"  primary="true"></bean>`
```
    @Autowired
    @Qualifier("father")
    private Father father;
```
- constructor
- default
- no

### FactoryBean BeanFactory BeanDefinition
FactoryBean 是一个Bean 
BeanFactory 是一个Factory
BeanDefinition

https://segmentfault.com/a/1190000021628751