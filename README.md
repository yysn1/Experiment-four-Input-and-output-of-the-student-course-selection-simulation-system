# 实验4学生选课模拟系统之文件输入输出

#实验目的

    掌握文件输入输出；
    了解对象序列化方法。

#业务要求

    在实验三（学生选课模拟系统）的基础上，利用文件保存选课结果，实现方法以下
    3.对象序列化
      1)采用对象序列化的writeObject方法把选课结果存到硬盘文件系统中；
      2)采用对象序列化的readObject方法从文件中恢复对象，并操作学生的选课课表，实现退课操作。
      3)打印课程对象信息，采用覆盖定义toString（）方法的方式。

#关键代码

  1导入编程时所需要的的库。
  
      import java.io.*;


  2.创建一个 选课结果.txt 文件，并将 System.out.println内容存储到文件中。

      public static void main(String[] args) throws IOException {
        PrintStream out = new PrintStream("选课结果.txt");
        System.setOut(out);
        Student me = new Student(2021310899, "马天硕", "男");
        System.out.println("学生信息");
        System.out.println(me);
        Teacher b = new Teacher(100, "师老师", "女", "线代");
        System.out.println("教师信息");
        System.out.println(b);
        Course c = new Course("现代", 006, "教室", 90f);
        System.out.println("课程信息");
        System.out.println(c);

  3.创建一个处理结果.txt.文件，并将 System.out.println内容存储到文件中。

      PrintStream Out = new PrintStream("处理结果.txt");
        System.setOut(Out);
        System.out.println("当前信息为："+"\n");
        File file = new File("\"E:\\java\\experiment_four\"");
        Reader r=new FileReader(file);
        BufferedReader br=new BufferedReader(r);
        String str="";
        while((str=br.readLine())!=null){
            System.out.println(str);
        }

#运行结果截图

  ![image](https://github.com/yysn1/Experiment-four-Input-and-output-of-the-student-course-selection-simulation-system/assets/124029692/8cbe705d-7084-4e07-a182-1936ef09b214)

#实验感受

    掌握了文件输入输出；
    了解了对象序列化方法。
    更深入了解了语言思路。
