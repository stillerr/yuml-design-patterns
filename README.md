# Design patterns in yUML

> Design patterns written down using [yUML](https://github.com/jaime-olivares/yuml-diagram/wiki)

## Abstract Factory

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/abstractFactory.png)

```yuml
[＜＜interface＞＞;AbstractFactory|+createProduct();]^-.-[ConcreteFactory|+createProduct();],
[＜＜interface＞＞;AbstractProduct]^-.-[ConcreteProduct]
```

## Builder

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/builder.png)

```yuml
[Director|+build();]++-[Builder|+buildPart();], [Builder]^-.-[ConcreteBuilder|+buildPart();+getResult():Product;]
```

## FactoryMethod

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/factoryMethod.png)

```yuml
[Creator|+factoryMethod():Product;]^-[ConcreteCreator|+factoryMethod():Product;]
```

## Prototype

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/prototype.png)

```yuml
[＜＜interface＞＞;Prototype|+clone():Prototype;]^-.-[ConcretePrototypeB|+clone():Prototype;],
[＜＜interface＞＞;Prototype|+clone():Prototype;]^-.-[ConcretePrototypeA|+clone():Prototype;]
```

## Singleton

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/singleton.png)

```yuml
[Singleton|-instance:Singleton = null|-Singleton();+getInstance():Singleton;]
```

## Adapter

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/adapter.png)

```yuml
[＜＜interface＞＞;Target|+request();]^-.-[Adapter|+request();],
[Adapter]-^[Adaptee|+specificRequest();]
```

## Bridge

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/bridge.png)

```yuml
[Abstraction|-impl:Implementor;+function()]^-[RefinedAbstraction |+refinedFunction();],
[Abstraction]<>-[Implementor|+implementation();],
[Implementor]^-[ConceteImplementor|+implementation();]
```

## Composite

![alt tag](https://raw.githubusercontent.com/stillerr/yuml-design-patterns/master/composite.png)

```yuml
[Component|+opertation()]^-[Leaf|+operation();],
[Component]^-[Composite|+operation();+add();+remove();+getChild()],
[Component]0..*-<>1[Composite]
```
