# Create C# Project

1. เลือก Create a new project

   <br/><kbd><img width="400" alt="Screenshot 2026-09-26 173758" src="https://github.com/user-attachments/assets/f9819d57-0d24-4fce-93ef-7aabb49ba998" /></kbd><br /><br />

2. เลือก language: C# -> platform: Window -> project type: Console ดังนี้

   <kbd><img width="400"  alt="Screenshot 2026-09-26 175226" src="https://github.com/user-attachments/assets/2cef3a48-6370-4bd4-bc4b-2ef14db9c761" /></kbd><br /><br />

3. ตั้งชื่อโปรเจ็กต์ (Project name) และเลือกตำแหน่งที่จะเก็บโปรเจ็กต์ (Location)

    - แนะนำตั้งชื่อโปรเจ็กต์แบบ Pascal Case เช่น MyProject, LoanProject, ApartmentProject เป็นต้น ณ โปรเจ็กต์นี้ตั้งชื่อเป็น SAUConsoleApp1

    - ส่วนของ Solution name เบื้องต้นแนะนำเป็นชื่อเดียวกับชื่อโปรเจ็กต์ ทั้งนี้ Solution name เปรียบเสมือนเป็นระบบใหญ่ที่ครอบคลุมได้หลายโปรเจ็กต์

   <br/><kbd><img width="400"  alt="Screenshot 2026-09-26 175406" src="https://github.com/user-attachments/assets/49661187-bc50-492f-8760-109bba020ad2" /></kbd><br /><br />

   <kbd><img width="600"  alt="Screenshot 2026-09-26 175447" src="https://github.com/user-attachments/assets/8123b06e-d69f-4066-93c8-59c142b42962" /></kbd><br /><br />

4. แก้ไขโค้ด ดังนี้

   ```
   using System;
   
   namespace SAUConsoleApp1
   {
       internal class Program
       {
           static void Main(string[] args)
           {
               Console.WriteLine("+++++++++++++++++++++++++");
               Console.WriteLine("Hello....");
               Console.Write("Hi....");
               Console.WriteLine("Hey....");
               Console.WriteLine("Hum....");
               Console.WriteLine("+++++++++++++++++++++++++");
           }
       }
   }
   ```

5. Run โปรเจ็กต์ โดยคลิกที่ปุ่ม Start หรือ เลือกเมนู Debug->Start Debugging หรือ **กดปุ่ม F5 ซึ่งแนะนำ** 

   <br /><kbd><img width="450"  alt="Screenshot 2026-09-26 185239" src="https://github.com/user-attachments/assets/9d8dd017-d68f-4afc-98c1-c906935f1986" /></kbd><br /><br />

   <kbd><img width="450"  alt="Screenshot 2026-09-26 185314" src="https://github.com/user-attachments/assets/a411ac16-21a8-40dd-918c-2928ff8bc585" /></kbd><br /><br />

6. หน้าจอการ Run โปรเจ็กต์ประเภท Console แสดง ดังนี้

   <br /><kbd><img width="673" height="324" alt="Screenshot 2026-09-26 175702" src="https://github.com/user-attachments/assets/d685dfdb-2ba0-4403-a2bd-1273ab01444e" /></kbd><br /><br />

## C# Program Structure 

```
using System;   // 1. Namespace declaration

namespace SAUConsoleApp1    // 2. Namespace ของโปรแกรม
{
    internal class Program      // 3. Class declaration
    {
        static void Main(string[] args)     // 4. Main method
        {
            // 5. Statement
            Console.WriteLine("+++++++++++++++++++++++++");
            Console.WriteLine("Hello....");
            Console.Write("Hi....");
            Console.WriteLine("Hey....");
            Console.WriteLine("Hum....");
            Console.WriteLine("+++++++++++++++++++++++++");
        }
    }
}
```

**ส่วนประกอบหลักของโปรแกรม C#**

1. using System;
    - คืออะไร: เป็นการประกาศว่าเราจะใช้ namespace ที่ชื่อว่า System
    - ทำไมต้องมี: เพราะ Console.WriteLine() อยู่ใน System namespace ถ้าไม่ใส่ เราจะเรียกใช้ไม่ได้
    - เปรียบเทียบง่าย ๆ: เหมือนการบอกว่า “ขอยืมเครื่องมือจากกล่อง System มาใช้หน่อย”
2. namespace HelloWorld
    - คืออะไร: Namespace คือพื้นที่จัดเก็บโค้ด เพื่อไม่ให้ชื่อซ้ำกัน
    - ทำไมต้องมี: ถ้าโปรเจกต์ใหญ่ มีหลาย class และ library การใช้ namespace จะช่วยจัดระเบียบ
    - ตัวอย่าง:
        - namespace School อาจเก็บ class เกี่ยวกับนักเรียน ครู
        - namespace Hospital อาจเก็บ class เกี่ยวกับหมอ คนไข้
3. class Program
    - คืออะไร: Class คือโครงสร้างหลักที่เก็บ method และ data/field
    - ทำไมต้องมี: C# เป็นภาษาเชิงวัตถุ (OOP) ทุกโค้ดต้องอยู่ใน class หรือ struct
    - ตัวอย่าง:
        - class Student อาจมีข้อมูลชื่อ, อายุ, เกรด
        - class Car อาจมีข้อมูลยี่ห้อ, รุ่น, ความเร็ว
4. static void Main(string[] args)
    - คืออะไร: จุดเริ่มต้นของโปรแกรม C# ทุกตัว (entry point)
    - รายละเอียด:
        - static → ไม่ต้องสร้าง object ก็เรียกใช้ได้
        - void → ไม่คืนค่าอะไรกลับมา
        - Main → ชื่อ method หลัก
    (string[] args) → ใช้รับค่าจาก command line (ถ้ามี)
5. Console.WriteLine() และ Console.Write( )
    - คืออะไร: Statement หรือคำสั่งที่ให้โปรแกรมทำงาน
    - การทำงานในที่นี้เพื่อบอกให้โปรแกรมแสดงข้อมูลใดๆ ออกมาทางหน้าจอ โดยข้อมูลที่แสดงเป็นได้ทั้งข้อความ(String) ตัวเลข(Number) ตัวอักษร(Character) นิพจน์(Expression: ส่งที่สร้างผลลัพธ์และให้ค่าคืนกลับมา เช่น การคำนวณ ตัวแปร เป็นต้น)
    - Console.WriteLine() แสดงข้อมูลเสร็จแล้วขึ้นบรรทัดใหม่
    - Console.Write() แสดงข้อมูลเสร็จแล้วไม่ขึ้นบรรทัดใหม่
    - ตัวอย่าง:
        - Console.WriteLine("Welcome SAU Student!");
        - Console.Write(5 + 3); → จะแสดงผลเป็น 8

**ข้อควรรู้เบื้องต้น**
    
   - ทุก statement ต้องลงท้ายด้วย **;** (semi-colon)
   - ขอบเขตการทำงานของกลุ่มคำสั่งต่างๆ ต้องเขียนอยู่ภายใต **{ ..... }** (curly brackets)
   - Comment ตัวอักษร ข้อความ ตัวเลข ที่ไม่มีผลต่อการทำงาน โดยสามารถเขียนได้ 2 แบบเบื้องต้น ดังนี้
     - Single line comment เขียนอยู่หลังเครื่องหมาย //
     - Multiline comment เขียนอยู่ระหว่างเครื่องหมาย /*    */

        ```
        using System;

        namespace SAUConsoleApp1
        {
            internal class Program
            {
                static void Main(string[] args)
                {
                    /*
                        Output statement
                        Console.WriteLine()
                        แสดงผลเสร็จแล้วขึ้นบรรทัดใหม่
                    */
                    Console.WriteLine("+++++++++++++++++++++++++");
                    Console.WriteLine("AAA");
                    //Console.WriteLine("BBB");
                    Console.WriteLine("CCC");
                    //Console.WriteLine("DDD");
                    Console.WriteLine("EEE");
                    Console.WriteLine("+++++++++++++++++++++++++");
                }
            }
        }
        ```
        <kbd><img width="300" alt="Screenshot 2026-09-26 195039" src="https://github.com/user-attachments/assets/f680245a-c4c7-474e-8839-ebdfca828574" /></kbd><br /><br />
        สังเกตุว่าส่วนที่เป็น Comment จะไม่มีผลใดๆ ต่อการทำงาน


