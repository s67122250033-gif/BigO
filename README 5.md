1. แนวคิดของอัลกอริทึมRecursive / Iterative Partition: ใช้เทคนิค Hoare Partition หรือ Lomuto Partition สลับข้อมูลให้ค่า $\le k$ อยู่ฝั่งซ้าย และ $> k$ อยู่ฝั่งขวาSorting-Based Algorithm: เรียงลำดับอาร์เรย์ทั้งหมดก่อน ($\mathcal{O}(n \log n)$) ซึ่งผลลัพธ์จะแบ่งโซนโดยอัตโนมัติ
2. 4. ตัวอย่างข้อมูลนำเข้าและผลลัพธ์
Input: A = [12, 4, 7, 15, 3, 10, 8], k = 8

Partition Output: [4, 7, 3, 8, 15, 10, 12]

Sorting Output: [3, 4, 7, 8, 10, 12, 15]
5. การวิเคราะห์เชิงลึกTime Complexity:Recursive / Iterative Partition: $\mathcal{O}(n)$Sorting-Based: $\mathcal{O}(n \log n)$Space Complexity:Iterative Partition: $\mathcal{O}(1)$ (In-place)Recursive Partition: $\mathcal{O}(n)$Sorting-Based: $\mathcal{O}(\log n)$ ถึง $\mathcal{O}(n)$เหตุผลที่ Sorting ช้ากว่าที่จำเป็น: โจทย์ต้องการเพียงแค่ "แบ่งกลุ่ม" (Partition) ไม่ได้ต้องการให้ "เรียงลำดับสมาชิกทุกตัวในกลุ่ม" การเรียงลำดับจึงสร้าง Work Overhead ที่ไม่จำเป็นขึ้นมา ($\mathcal{O}(n \log n)$ แทนที่จะเป็น $\mathcal{O}(n)$)ความสัมพันธ์กับ Quick Sort: นี่คือขั้นตอนสำคัญ (Heart) ของอัลกอริทึม Quick Sort ซึ่งใช้ Partition เพื่อแบ่งปัญหาออกเป็น Sub-problems สองฝั่ง
