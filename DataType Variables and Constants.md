# DataType Variables and Constants

## Data Types

**Data Types** (ชนิดข้อมูล) ใช้กับการประกาศตัวแปร และการกำหนดชนิดข้อมูลที่ส่งกลับของเมธอด 

## Variables

**Variables** (ตัวแปร) คือ สิ่งที่ใช้เก็บข้อมูลที่เกิดขึ้นในโปรแกรม เป็น identifiers ชื่อที่พัฒนาตั้งขึ้นเอง และการจะนำตัวแปรไปเก็บข้อมูลใดๆ ได้ต้องทำการประกาศตัวแปร (variable declaration) ก่อนโดยมีรูปแบบคือ

    data_type  variable_name ;
    data_type  variable_name = init_value ;

**🌟Integral Data Types🌟**

ชนิดข้อมูลเลขจำนวนเต็ม
| Data ype | Size | Range |
| --- | --- | --- |
| byte	| 1 byte	| 0 to 255 |
| sbyte	| 1 byte	| -128 to 127 |
| short	| 2 bytes	| -32,768 to 32,767 |
| ushort	| 2 bytes	| 0 to 65,535 |
| int	| 4 bytes	| -2,147,483,648 to 2,147,483,647 |
| uint	| 4 bytes	| 0 to 4,294,967,295 |
| long	| 8 bytes	| -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| ulong	| 8 bytes	| 0 to 18,446,744,073,709,551,615 |

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                byte empExperience = 10;
                short empYearBorn = 2026;
                int empId = 190084985;
                long empBankDeposits = 9008498798798L; 
                
                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine("Employee experience is " + empExperience);
                Console.WriteLine("Employee year born is " + empYearBorn);
                Console.WriteLine("Employee ID is " + empId);
                Console.WriteLine("Employee bank deposits is " + empBankDeposits);
                Console.WriteLine("+++++++++++++++++++++++++++"); ;
            }
        }
    }

**🌟Floating-Point Data Types🌟**

ชนิดข้อมูลเลขจำนวนจริง (ทศนิยม)

| Data Type	| Size	| Precision | 
| --- | --- | --- |
| float	| 4 bytes	| 6-7 decimal places | 
| double	| 8 bytes	| 15-16 decimal places | 
| decimal	| 16 bytes	| 28-29 decimal places|  

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                float gpa = 3.48f;
                double widths = 4597.459814;
                decimal distance = 18799780.06506548999m;
                
                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine($"GPA is {gpa}");
                Console.WriteLine($"Widths is {widths}" );
                Console.WriteLine($"Distance is {distance}");
                Console.WriteLine("+++++++++++++++++++++++++++"); ;
            }
        }
    }


**🌟Character and Boolean Data Types🌟**

Data Type	| Size	| Description | 
| --- | --- | --- |
| char	| 2 bytes	| ตัวอักษร 1 ตัว | 
| bool	| 1 byte	| true หรือ false | 

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                char studentGrade = 'B';
                bool isComplete = true;

                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine("Student grade is {0}", studentGrade);
                Console.WriteLine("Complete is {0}", isComplete);
                Console.WriteLine("+++++++++++++++++++++++++++"); ;
            }
        }
    }

**🌟String Types🌟**
ชนิดข้อมูลข้อความ (ตัวอักษรตั้งแต่ 0 ตัวขึ้นไป เขียนอยู่ภายใต้ "???")

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {

            static void Main(string[] args)
            {
                string firstName = "Somsak";
                string lastName = "Deemak";

                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine("Full Name: {0} {1}", firstName, lastName);
                Console.WriteLine("+++++++++++++++++++++++++++"); ;
            }
        }
    }


**🌟Enumerations (enum) Types🌟**

ใช้สำหรับกำหนด ค่าคงที่ (constant values) ที่มีชื่อกำกับ เพื่อให้อ่านง่ายและเข้าใจความหมายมากกว่าตัวเลขดิบ

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            enum Day {
                Sunday,    // ค่าเริ่มต้น = 0
                Monday,    // 1
                Tuesday,   // 2
                Wednesday, // 3
                Thursday,  // 4
                Friday,    // 5
                Saturday   // 6
            };

            static void Main(string[] args)
            {
                Day today = Day.Wednesday;

                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine(string.Format("Today is {0}", today));
                Console.WriteLine(string.Format("Number of today is {0}", (int)today));
                Console.WriteLine("+++++++++++++++++++++++++++"); ;
            }
        }
    }

**🌟Struct Types🌟**

ใช้สำหรับสร้างกลุ่มข้อมูลที่เกี่ยวข้องกัน เก็บข้อมูลเป็นชุด

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            struct Student
            {
                public int Id;
                public string Name;
                public double Score;
            }

            static void Main(string[] args)
            {
                Student s1;
                s1.Id = 101;
                s1.Name = "Sombat Jaidee";
                s1.Score = 95.5;            

                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine($"ID: {s1.Id}, Name: {s1.Name}, Score: {s1.Score}");
                Console.WriteLine("+++++++++++++++++++++++++++"); ;
            }
        }
    }

**🌟Array Types🌟**

 คือชนิดข้อมูลที่ใช้เก็บ หลายค่า ที่มีชนิดเดียวกันไว้ในตัวแปรเดียว แต่ละค่าจะถูกเก็บใน ตำแหน่ง (index) โดยเริ่มจาก 0 เหมาะสำหรับเก็บข้อมูลที่เป็นชุด

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {

            static void Main(string[] args)
            {
                string[] foods = { "KFC", "Pizza", "Teenoi", "Oishi", "Yayoi" };

                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine("        FOOD LIST");
                Console.WriteLine("+++++++++++++++++++++++++++");
                foreach (string food in foods) {
                    Console.WriteLine(food);
                }
                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine();

                int[] scores = new int[3];
                scores[0] = 10;
                scores[1] = 20;
                scores[2] = 30;

                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine("        SCORE LIST");
                Console.WriteLine("+++++++++++++++++++++++++++");
                foreach (int score in scores)
                {
                    Console.WriteLine(score);
                }
                Console.WriteLine("+++++++++++++++++++++++++++");

            }
        }
    }
