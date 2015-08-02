#Design patterns in yuml

##Abstract Factory

```
[＜＜interface＞＞;AbstractFactory|+createProduct();]^-.-[ConcreteFactory|+createProduct();],
[＜＜interface＞＞;AbstractProduct]^-.-[ConcreteProduct]
```

##Builder

```
[Director|+build();]++-[Builder|+buildPart();], [Builder]^-.-[ConcreteBuilder|+buildPart();+getResult():Product;]
```

##FactoryMethod

```
[Creator|+factoryMethod():Product;]^-[ConcreteCreator|+factoryMethod():Product;]
```

Prototype

```
[＜＜interface＞＞;Prototype|+clone():Prototype;]^-.-[ConcretePrototypeB|+clone():Prototype;],
[＜＜interface＞＞;Prototype|+clone():Prototype;]^-.-[ConcretePrototypeA|+clone():Prototype;]
```

##Singleton

```
[Singleton|-instance:Singleton = null|-Singleton();+getInstance():Singleton;]
```

##Adapter

```
[＜＜interface＞＞;Target|+request();]^-.-[Adapter|+request();],
[Adapter]-^[Adaptee|+specificRequest();]
```

##Bridge

```
[Abstraction|-impl:Implementor;+function()]^-[RefinedAbstraction |+refinedFunction();],
[Abstraction]<>-[Implementor|+implementation();],
[Implementor]^-[ConceteImplementor|+implementation();]
```

##Composite

```
[Component|+opertation()]^-[Leaf|+operation();],
[Component]^-[Composite|+operation();+add();+remove();+getChild()],
[Component]0..*-<>1[Composite]
```




