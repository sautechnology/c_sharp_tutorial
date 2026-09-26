# Identifiers and Keywords
## Identifiers

**Identifiers** คือ ชื่อใดที่นักพัฒนาใช้ตั้งให้กับสิ่งต่าง ๆ ในโปรแกรม ได้แก่
- ชื่อ namespace
- ชื่อ variable 
- ชื่อ constant 
- ชื่อ class 
- ชื่อ object 
- ชื่อ method 
- ชื่อ data/field 
- ชื่อ interface

**กฎการตั้งชื่อ Identifiers ใน C#**
1. ต้องขึ้นต้นด้วย ตัวอักษร (A–Z, a–z) หรือ เครื่องหมายขีดล่าง _
2. ห้ามขึ้นต้นด้วยตัวเลข
3. ห้ามมีช่องว่างหรือสัญลักษณ์พิเศษ เช่น @, #, %, !
4. C# แยกตัวพิมพ์เล็ก–ใหญ่ เช่น Name ≠ name
5. ห้ามใช้ คำสงวน (keywords) 

## Keywords

**Keywords** (คำสงวน) คือ คำที่ C# ใช้สำหรับโครงสร้างของภาษาเอง เช่น การประกาศตัวแปร การควบคุมการทำงาน หรือการกำหนดชนิดข้อมูล หากนำคำสงวนไปตั้งเป็นชื่อใดๆ (identifiers) ก็จะ error โดย keywords มี ดังนี้

    abstract, as, base, bool, break, byte, case, catch, char, checked, class, const, 
    continue, decimal, default, delegate, do, double, else, enum, event, explicit, extern, 
    false, finally, fixed, float, for, foreach, goto, if, implicit, in, int, interface,
    internal, is, lock, long, namespace, new, null, object, operator, out, override, 
    params, private, protected, public, readonly, ref, return, sbyte, sealed, short, 
    sizeof, stackalloc, static, string, struct, switch, this, throw, true, try, typeof, 
    uint, ulong, unchecked, unsafe, ushort, using, virtual, void, volatile, while

ทั้งนี้ หากต้องการนำไปตั้งชื่อจริงๆ ก็ทำได้ โดยการใส่เครื่องหมาย @ ไว้ข้างหน้า (แต่ไม่แนะนำให้ทำ)

    using System;
    
    namespace SAUConsoleApp1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                int @class = 20;
                int @bool = 50;
                int @if = @class + @bool;
                Console.WriteLine("+++++++++++++++++++++++++++");
                Console.WriteLine("@class is " + @class);
                Console.WriteLine("@bool is " + @bool);
                Console.WriteLine($"{@class} + {@bool} = {@if}");
                Console.WriteLine("+++++++++++++++++++++++++++"); ;
            }
        }
    }

<kbd><img width="320" alt="Screenshot 2026-09-26 212326" src="https://github.com/user-attachments/assets/99388db7-1e67-4c0f-9e15-6b59a05e7c8a" /></kbd><br />


## Naming Conventions

ธรรมเนียมปฏิบัติในการตั้งชื่อใน C#

| Code Element | Casing Style| Prefix / Suffix | Example |
| --- | --- | --- | --- |
Classes & Structs | PascalCase| None| CustomerAccount |
| Interfaces | PascalCase | I prefix | IUserRepository |
| Methods | PascalCase | None | CalculateTotal() |
| Properties | PascalCase | None | IsActive |
| Public Fields | PascalCase | None | TotalCount |
| Constants (const) | PascalCase | None | MaxItemsPerPage |
| Private Fields | camelCase | _ prefix | _databaseConnection |
| Local Variables | camelCase | None | invoiceAmount |
| Method Parameters | camelCase | None | userId |

