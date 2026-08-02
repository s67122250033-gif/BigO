1. แนวคิดของอัลกอริทึม
Pre-processing (เงื่อนไขเพิ่มเติม): แปลงสตริงให้เป็นตัวพิมพ์เล็กทั้งหมด และกรองเฉพาะตัวอักษร/ตัวเลข (Character.isLetterOrDigit)

Reverse and Compare: นำสตริงที่กรองแล้วมากลับลำดับด้วย Iterative จากข้อ 1 แล้วนำมาเปรียบเทียบกับสตริงเดิมด้วย .equals()

Recursive Two-Pointer: เทียบตัวอักษรตำแหน่ง left และ right หากไม่ตรงกันตอบ false ทันที หากตรงกันให้เรียกเวียนเกิดโดยเขยิบ left + 1 และ right - 1
4. ตัวอย่างข้อมูลนำเข้าและผลลัพธ์
Input: "A man, a plan, a canal: Panama"

Output: true
5. การวิเคราะห์ Time ComplexityReverse and Compare:Best/Worst Case: $\mathcal{O}(n)$ — ต้องกลับลำดับสตริงทั้งเส้นเสร็จก่อนเสมอ จึงจะเริ่มเปรียบเทียบได้Recursive Two-Pointer:Best Case: $\mathcal{O}(1)$ — ตัวอักษรคู่แรกสุดไม่ตรงกัน โปรแกรมหยุดทำงานทันที (Early Exit)Worst Case: $\mathcal{O}(n)$ — สตริงเป็น Palindrome ต้องเทียบครบ $n/2$ คู่
6. การวิเคราะห์ Space ComplexityReverse and Compare: $\mathcal{O}(n)$ — สำหรับเก็บ Reverse String ใหม่Recursive Two-Pointer: $\mathcal{O}(n)$ — สำหรับ Call Stack สูงสุด $n/2$ ชั้น
7. การเปรียบเทียบข้อดีและข้อจำกัด
Reverse and Compare: เขียนง่ายแต่ประมวลผลเปลืองโดยไม่จำเป็น หากสตริงยาวมากๆ แล้วตัวแรกไม่เท่ากัน ก็ยังต้องสร้าง String กลับลำดับจนเสร็จ

Recursive Two-Pointer: มีคุณสมบัติ Early Exit ช่วยประหยัดเวลาอย่างมากในกรณีที่ไม่เป็น Palindrome
8. สรุปอัลกอริทึมที่เหมาะสม
Recursive Two-Pointer เหมาะสมกว่าเนื่องจากหยุดทำงานได้ทันทีเมื่อพบตัวอักษรที่ไม่เข้าคู่กัน (ประหยัดทั้งเวลาและพลังงานประมวลผล)
