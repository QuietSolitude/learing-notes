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
      System.Nullable<int> nullableInt; 
      nullableInt = null;  
    ```
   * 有时候我们需要值类型为空。可以使用System.Nullable<T>类型来使值类型为空。
     * 可以是使用类型+？来替代上面的System.Nullable
      ```int? nullableInt```
    

  ## 运算符
    * 对了可空的基本类型与基本类型进行运算符处理都是没有区别的，但是要注意的是如果对可空基本类型与基本类型进行运算，就要强制把可空基本类型转换成基本类型。
    ```
      int? number = 5;
      int numberInt = (int)number * 8;
    ```
     
    * 空接合运算符(null coalescing operator)
     ```
       int? number = null;
       int nValue = number ?? 3; //nVaule的值是3。

       int? number2 = number * 3 ?? 3 // number2的值是3。
     ```
    * ？？是二元运算符，可以给可空变量提供默认的值（可以为任意类型提供），如 果第一个值不是null那么就将第一个值赋给nValue，否则就第二个值赋给nValue，？？运算符会自动处理转换。
    如果两个值是null，那么会报错。
       ？？可以在处理可空变量提供默认值的一种快捷方式，不需要在使用if或者三元运算符。
     
    * ?.(可控条件符)，有助于避免繁杂的空值检查造成的代码歧义,也可用于触发事件。
     ```
       int? number = Cost.orders?.Count(); //这样如果这个方法返回的是null不会抛出异常，会将Count设为null。
 ## List<T> 
    * T类型对象的集合