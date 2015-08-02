#Design patterns in yuml

##Abstract Factory

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/abstractFactory.png)

```
[＜＜interface＞＞;AbstractFactory|+createProduct();]^-.-[ConcreteFactory|+createProduct();],
[＜＜interface＞＞;AbstractProduct]^-.-[ConcreteProduct]
```

##Builder

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/builder.png)

```
[Director|+build();]++-[Builder|+buildPart();], [Builder]^-.-[ConcreteBuilder|+buildPart();+getResult():Product;]
```

##FactoryMethod

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/factoryMethod.png)

```
[Creator|+factoryMethod():Product;]^-[ConcreteCreator|+factoryMethod():Product;]
```

Prototype

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/prototype.png)

```
[＜＜interface＞＞;Prototype|+clone():Prototype;]^-.-[ConcretePrototypeB|+clone():Prototype;],
[＜＜interface＞＞;Prototype|+clone():Prototype;]^-.-[ConcretePrototypeA|+clone():Prototype;]
```

##Singleton

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/singleton.png)

```
[Singleton|-instance:Singleton = null|-Singleton();+getInstance():Singleton;]
```

##Adapter

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/adapter.png)

```
[＜＜interface＞＞;Target|+request();]^-.-[Adapter|+request();],
[Adapter]-^[Adaptee|+specificRequest();]
```

##Bridge

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/bridge.png)

```
[Abstraction|-impl:Implementor;+function()]^-[RefinedAbstraction |+refinedFunction();],
[Abstraction]<>-[Implementor|+implementation();],
[Implementor]^-[ConceteImplementor|+implementation();]
```

##Composite

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/composite.png)

```
[Component|+opertation()]^-[Leaf|+operation();],
[Component]^-[Composite|+operation();+add();+remove();+getChild()],
[Component]0..*-<>1[Composite]
```




