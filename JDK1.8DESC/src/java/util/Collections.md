集合类  源码解析   
先看看两大接口 
Map 接口 和 Collection接口
Map接口和Collection接口的关系：（之间没有实际继承关系，只是）
1、虽然总是将Map和List 以及Set 一起说，但实际上Map和List 以及Set并不是同级关系。List 和Set是Collection的子接口；Map并不是，Map并不属于Collection接口系列。 
2、Map和Collection的关系在于Map的实现上。因为Map的所有key实际是一个Set对象，Map的所有value也是一个Collection接口对象。（可看Map接口源码） 
Map集合:是一种键和值的映射关系(双列集合)        
        Collection集合:单列集合,只能存储一种类型的元素



     间接关系:HashSet依赖于Map接口的子实现类HashMap的
           TreeSet依赖于Map接口的子实现类TreeMap的

3、其他，并没有太多关系。

1.所有集合类都位于java.util包下。Java的集合类主要由两个接口派生而出：Collection和Map，Collection和Map是Java集合框架的根接口，这两个接口又包含了一些子接口或实现类。
2. 集合接口：6个接口（短虚线表示），表示不同集合类型，是集合框架的基础。
3. 抽象类：5个抽象类（长虚线表示），对集合接口的部分实现。可扩展为自定义集合类。
4. 实现类：8个实现类（实线表示），对接口的具体实现。
5. Collection 接口是一组允许重复的对象。
6. Set 接口继承 Collection，集合元素不重复。
7. List 接口继承 Collection，允许重复，维护元素插入顺序。
8. Map接口是键－值对象，与Collection接口没有什么关系。