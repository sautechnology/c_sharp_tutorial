# DataType Variables and Constants

## Data Types

**Data Types** (ชนิดข้อมูล) ใช้กับการประกาศตัวแปร และการกำหนดชนิดข้อมูลที่ส่งกลับของเมธอด 

## Variables

**Variables** (ตัวแปร) คือ สิ่งที่ใช้เก็บข้อมูลที่เกิดขึ้นในโปรแกรม เป็น identifiers ชื่อที่พัฒนาตั้งขึ้นเอง และการจะนำตัวแปรไปเก็บข้อมูลใดๆ ได้ต้องทำการประกาศตัวแปรก่อน (variable declaration) มีรูปแบบ ดังนี้

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

<kbd><img width="376" height="170" alt="Screenshot 2026-09-26 214714" src="https://github.com/user-attachments/assets/684f5b73-2b9e-43bd-9f08-97506700f193" /></kbd><br />


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


<kbd><img width="352" height="153" alt="Screenshot 2026-09-26 225543" src="https://github.com/user-attachments/assets/aaddfda0-d4fd-4c35-9d86-094d1461b88c" /></kbd><br />



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

<kbd><img width="327" height="135" alt="Screenshot 2026-09-26 221126" src="https://github.com/user-attachments/assets/d822a2ae-439a-481d-b719-cff8ec6f5181" /></kbd><br />

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

<kbd><img width="344" height="111" alt="Screenshot 2026-09-26 223613" src="https://github.com/user-attachments/assets/7b84df37-818b-40dd-b456-1860b4083e7d" /></kbd><br />


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

<kbd><img width="343" height="134" alt="Screenshot 2026-09-26 221549" src="https://github.com/user-attachments/assets/922a12bd-bf24-44e1-bb4a-3d19afa3f25f" /></kbd><br />

**🌟Struct Types🌟**

เป็น Value Type ในภาษา C# ใช้สำหรับสร้างกลุ่มข้อมูลที่เกี่ยวข้องกัน เก็บข้อมูลเป็นชุด

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

<kbd><img width="394" height="108" alt="Screenshot 2026-09-26 223133" src="https://github.com/user-attachments/assets/ca18e87a-8e6c-4f43-a65e-1ea6221feb3c" /></kbd><br />

**🌟Array Types🌟**

 คือ ชนิดข้อมูลที่ใช้เก็บ หลายค่า ที่มีชนิดเดียวกันไว้ในตัวแปรเดียว แต่ละค่าจะถูกเก็บใน ตำแหน่ง (index) โดยเริ่มจาก 0 เหมาะสำหรับเก็บข้อมูลที่เป็นชุด

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

<kbd><img width="350" height="377" alt="Screenshot 2026-09-26 224604" src="https://github.com/user-attachments/assets/451f017c-351b-4882-a799-0a0a1dcaab89" /></kbd><br />

## Constants

คือ ค่าที่ถูกกำหนดไว้แล้วและ ไม่สามารถเปลี่ยนแปลงได้ ตลอดการทำงานของโปรแกรม ใช้คำสั่ง const ในการประกาศ เหมาะสำหรับค่าที่แน่นอน มีรูปแบบ ดังนี้

    const data_type constant_name = value; 

**ข้อควรระวัง**
- สำหรับ Constants ต้องมีการกำหนดค่าตั้งแต่ตอนประกาศ ไม่เช่นนั้นจะ error
- ค่าของ Constants ห้ามเปลี่ยน ไม่เช่นนั้นจะ error

ตัวอย่าง

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                const int DataA = 100;
                //const int DataB;      error
                //DataA = 200;          error

                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine(DataA);
                Console.WriteLine("+++++++++++++++++++++++++++");
            }
        }
    }


<kbd><img width="305" height="111" alt="Screenshot 2026-09-26 230738" src="https://github.com/user-attachments/assets/bd33daaa-f4b6-4c9a-814b-21e3d9a05220" /></kbd><br /><br />
    
