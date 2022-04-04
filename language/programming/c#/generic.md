# 泛型（generic）
  ## 泛型：是指不确定的类型。
  ```
   void add(int num) 
   void add(double)
  ```
   * 一般情况下，定义变量或者参数都是声明必须确定类型，实现两个参数相加的方法只能对声明的参数类型进行操作，如果要处理其他类型，就必须定义其他的参数类型，导致重复率高，
     所以我们使用泛型来根据运行时确定参数的类型，这样一个方法就是处理多个参数类型。
   * 在尖括号里面放入占位符T来声明一个泛型,泛型可以修饰类、方法、和成员或者参数和接口等。
     ```
      <T> num //修饰成员或者变量
      class MyClass<T>{} //修饰类
      <T> add<T>(<T> num)
     ```
     * 占位符T的作用是在执行的时候替换明确的类型的类型。
     ```int add<int>(int num)```
   * 如果类继承的是泛型类或者是泛型接口，那该类也必须泛型。
     ``` interface Istudent<T>:Iteacher<T> ```

  ## 可空类型（nullable type）
     ```
      system.Nullable<int> nullableint;
     ```
   * 有时候我们需要值类型为空。可以使用System.Nullable<T>类型来使值类型为空。