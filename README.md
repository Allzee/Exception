# Exception
//how to handle exceptions
public class Example_01{
  private int num=1;                           //成员变量
public int getNum(){                           //成员方法
  return num;                                  //返回成员变量的值
}
public void setNum(int num){                   //成员方法
  this.num=num;                                //设置成员变量的值
}
public Example_01(){                           //类的构造方法 
  try{
      Class.forName("com.mingrisoft.Test");    //装载com.mingrisoft包中的Test类
  }catch(ClassNotFoundException e){
        e.printStackTrace();
  }
  System.out.println("测试！");                 //在控制台输出“测试！”
}
public static void main(String[] args){
    Example_01 exam=new Example_01();          //创建类的实例
    exam.setNum(12);                           //调用setNum()设置成员变量num的值为12
    System.out.println(exam.getNum());         //调用getNum()输出成员变量的值为12
}

}
