
# interface
JDK8之前，interface之中可以定义变量和方法，变更必需是public static final ,方法必需是public abstract的。这也是默认的，所以可以不写。

JDK8及之后，接口可以定义static方法和default方法。
其中 静态方法只能通过接口名调用，不可以通过实现的类或者实现类的对象调用。
default方法，只能通过接口实现类的对象来调用。默认方法可以在实现类中覆盖默认方法，但是由于java支持一个类可以实现多个接口，如果多个接口中存在同样的static和default方法，如果是静态方法一样，并且一个类同时实现了两个接口，此时不会产生错误，只为只能通过接口调用接口中的静态方法，所以对编译器是可以区分的。但是如果是一样的默认方法，实现一个类同时实现了这两个接口，那么此方法必需重写，否则编译失败。
