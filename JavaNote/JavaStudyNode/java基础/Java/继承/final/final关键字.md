**final的应用场景**
1. 不希望类被[继承],可以用final修饰
2. 不希望父类的某个方法被子类[覆盖]/重写,用final修饰 // 访问修饰符 final 返回类型 方法名
3. 不希望类的某个属性的值被修改,可以使用final修饰 // public final double N=0.5;
4. 不希望某个局部变量被修改 , 可以使用final修饰  // final double N = 0.3; 

**final使用注意事项和细节讨论**
1. final修饰的属性又叫常量, 一般用XX_XX_XX来命名
2. final修饰的属性在定义时,必须赋初始值,并且以后不能再修改 , 赋值方式在以下几种
     1.定义时   2.在构造器中  3.在代码块中
   3.如果final修饰的[属性是静态的],则初始化的位置只能   1.定义时初始化(因为确保能够使静态字段能够实例化)  2.[在静态代码块]
   4 .final类不能被继承, 但是可以实例化对象
   5 .如果类不是final类, 但是含有final方法, 则该方法虽然不能重写, 但是可以被继承 
   6.一般来说,如果一个类已经时final类了,就没有必要再将方法修饰成final方法
   7.final不能修饰[构造器]  (因为构造器是用于对象初始化的,final可以使不使对象初始化都能用)
   8.final和static往往搭配使用, 效率更高, 底层编译器做了优化处理,原因是不会导致类的加载  
   9.包装类(Integer,Double,Float,Boolean等都是final),String也是final类
   