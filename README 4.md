1. แนวคิดของอัลกอริทึม
Recursive Two-Pointer: ใช้ตัวชี้ left และ right หาก a[left] คู่ ขยับขวา, หาก a[right] คี่ ขยับซ้าย, หากซ้ายคี่-ขวาคู่ ให้ Swap แล้วเรียกเวียนเกิด

Iterative Two-Pointer: ใช้แนวคิดเดียวกับวิธีแรก แต่ใช้ลูป while (left < right)

Extra Array: วนลูปอ่าน 2 รอบ รอบแรกคัดเฉพาะเลขคู่ใส่ Array ใหม่ รอบสองคัดเลขคี่ใส่ต่อท้าย
4. ตัวอย่างข้อมูลนำเข้าและผลลัพธ์
Input: [5, 2, 7, 4, 9, 6]

Iterative/Recursive Output: [6, 2, 4, 7, 9, 5] (ไม่คงลำดับเดิม - Unstable)

Extra Array Output: [2, 4, 6, 5, 7, 9] (คงลำดับเดิม - Stable)
5. การวิเคราะห์เปรียบเทียบคุณสมบัติRecursive Two-PointerIterative Two-PointerExtra ArrayTime Complexity$\mathcal{O}(n)$$\mathcal{O}(n)$$\mathcal{O}(n)$Space Complexity$\mathcal{O}(n)$ (Stack)$\mathcal{O}(1)$ (In-place)$\mathcal{O}(n)$ (Extra Array)Swaps Countน้อยที่สุด ($\le n/2$)น้อยที่สุด ($\le n/2$)0 (ใช้ Copy แทน)StabilityUnstableUnstableStable
6. สรุปอัลกอริทึมที่เหมาะสม
หากเน้น Memory Efficient (In-place): ใช้ Iterative Two-Pointer

หากเน้น การรักษาลำดับเดิม (Stable): ต้องใช้ Extra Array
