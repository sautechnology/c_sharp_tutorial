# Operators in C#

## Types of Operators
C# มีชุดตัวดำเนินการที่สามารถจำแนกออกเป็นหมวดหมู่ต่างๆ ตามลักษณะการทำงาน โดยแบ่งออกเป็นประเภทดังต่อไปนี้:

- Arithmetic Operators
- Relational Operators
- Logical Operators
- Assignment Operators
- Increment and Decrement Operators
- Ternary Operator
- Null Coalescing Operator
  
### Arithmetic Operators
ตัวดำเนินการทางคณิตศาสตร์ (ตัวเลขกระทำกับตัวเลขได้ตัวเลข)
- Addition ( + )
- Subtraction ( - )
- Multiplication ( * )
- Division ( / )
- Modulus ( % )

ตัวอย่าง

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                int x = 20, y = 5;

                Console.WriteLine("Addition: " + (x + y));      //String Concatenation
                Console.WriteLine("Subtraction: {0}", x - y);   //Composite Formatting
                Console.WriteLine($"Multiplication: {x * y}");  //String Interpolation
                Console.WriteLine(string.Format("Division: {0}", x / y));   //string.Format
                Console.WriteLine(string.Format("Modulo: {0}", x % y));     //string.Format
            }
        }
    }

<kbd><img width="309" height="142" alt="Screenshot 2026-09-26 235836" src="https://github.com/user-attachments/assets/8ec09c6c-8bc8-4673-aca6-c1e5eb9b3348" /></kbd><br />


### Relational Operators
ตัวดำเนินการเปรียบเทียบ (ตัวเลขหรือตัวอักษรเปรียบเทียบกันผลลัพธ์ที่ได้มีแค่ true/false)

- Equal to ( == )
- Not equal to ( != )
- Less than ( < )
- Less than or equal to ( <= )
- greater than ( > )
- Greater than or equal to ( >= )

ตัวอย่าง

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                int num1 = 100, num2 = 200;
                char char1 = 'M', char2 = 'a';

                //show compare
                Console.WriteLine($"{num1} == {num2} is {num1 == num2}");
                Console.WriteLine($"{num1} != {num2} is {num1 != num2}");
                Console.WriteLine($"{num1} < {num2} is {num1 < num2}");
                Console.WriteLine($"{char1} > {char2} is {char1 > char2}");
                Console.WriteLine($"{char1} <= {char2} is {char1 <= char2}");
                Console.WriteLine($"{char1} >= {char2} is {char1 >= char2}");
            }
        }
    }

<kbd><img width="311" height="166" alt="Screenshot 2026-09-27 000617" src="https://github.com/user-attachments/assets/a5866ad7-eff7-4a66-b8da-341cd57b36fd" /></kbd><br />

### Logical Operators
ตัวดำเนินการตรรก (true/false กระทำกับ true/false ผลลัพธ์ที่ได้มีแค่  true/false)

- Logical AND (&&) : ให้ค่า true เมื่อทั้งสองฝั่งเป็น true อย่างอื่นเป็น false หมด
- Logical OR ( || ) : ให้ค่า false เมื่อทั้งสองฝั่งเป็น false อย่างอื่นเป็น true หมด
- Logical NOT ( ! ): ให้ค่าตรงข้าม !true ได้ false และ !false ได้ true

ตัวอย่าง

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                bool result;
                int num1 = 101, num2 = 202;

                result = (num1 == num2) && (num1 > 55);
                Console.WriteLine(result);
                Console.WriteLine(!result);

                result = (num1 == num2) || (num1 > 55);
                Console.WriteLine(result);
                Console.WriteLine(!result);
            }
        }
    }

<kbd><img width="338" height="131" alt="Screenshot 2026-09-27 001957" src="https://github.com/user-attachments/assets/12984860-3a74-40b2-baba-a5f45acf790a" /></kbd><br />

### Increment and Decrement Operators
ตัวดำเนินการเพิ่มค่า ลดค่า 
- ++ (Increments by 1 เพิ่มค่าตัวเองทีละ 1)
- -- (Decrements by 1 ลดค่าตัวเองทีละ 1)

ตัวอย่าง

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                int number = 10, result;

                ++number;
                Console.WriteLine(number);

                --number;
                Console.WriteLine(number);

                result = ++number;
                Console.WriteLine("++number = " + result);

                result = --number;
                Console.WriteLine("--number = " + result);
            }
        }
    }

<kbd><img width="323" height="130" alt="Screenshot 2026-09-27 002305" src="https://github.com/user-attachments/assets/1f50295d-fec0-483a-b116-7f352abc367e" /></kbd><br />

### Assignment Operators
ตัวดำเนินการกำหนดค่า

- =
- += (Add and assign.)
- -= (Subtract and assign.)
- *= (Multiply and assign.)
- /= (Divide and assign.)
- %= (Modulo and assign.)
  
ตัวอย่าง

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                int number = 10;

                number += 5;  // number = number + 5
                Console.WriteLine(number);

                number -= 3;  // number = number - 3
                Console.WriteLine(number);

                number *= 2;  // number = number * 2
                Console.WriteLine(number);

                number /= 3;  // number = number / 3
                Console.WriteLine(number);

                number %= 3;  // number = number % 3
                Console.WriteLine(number);
            }
        }
    }

<kbd><img width="331" height="148" alt="Screenshot 2026-09-27 002948" src="https://github.com/user-attachments/assets/e6d13c27-6c46-4ded-a976-86bdb5098311" /></kbd><br />

### Ternary Operator
ตัวดำเนินการเพื่อการตรวจสอบเงื่อนไข มี syntax ดังนี้

    Condition ? Expression1 : Expression2 ;

พิสูจน์ Condition กรณีผลเป็นจริงทำ Expression1 กรณีผลเป็นเท็จทำ Expression2

ตัวอย่าง

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                int number = 999;
                string result;

                result = (number % 2 == 0) ? "Even Number" : "Odd Number";
                Console.WriteLine("++++++++++++++++++++++++++");
                Console.WriteLine("{0} is {1}", number, result);
                Console.WriteLine("++++++++++++++++++++++++++");
            }
        }
    }

<kbd><img width="328" height="108" alt="Screenshot 2026-09-27 003108" src="https://github.com/user-attachments/assets/8d3b7190-d7ca-4c5d-8a6f-ab9c110c4db1" /></kbd><br />

### Null Coalescing Operator
ตัวดำเนินการเพื่อการตรวจสอบค่า Null มี syntax ดังนี้

    leftOperand ?? rightOperand

กรณี leftOperand เป็น Null จะได้ rightOperand 
กรณี leftOperand ไม่เป็น Null จะได้ leftOperand

ตัวอย่าง

    using System;

    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                string name = null;
                
                string result = name ?? "No name T_T";
                Console.WriteLine("++++++++++++++++++++++++++");
                Console.WriteLine(result);            

                name = "Sombat ^_^";
                result = name ?? "No name ^_^";
                Console.WriteLine("++++++++++++++++++++++++++");
                Console.WriteLine(result);

                Console.WriteLine("++++++++++++++++++++++++++");
            }
        }
    }

<kbd><img width="312" height="146" alt="Screenshot 2026-09-27 003834" src="https://github.com/user-attachments/assets/01ffa65a-4348-480e-ba7a-65bb288e6899" /></kbd><br /><br />



    
