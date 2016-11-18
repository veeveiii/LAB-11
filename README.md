#ใบงานที่ 11
##การเขียนโปรแกรมกราฟฟิกส์ด้วย GDI+ (3)
## กล่าวนำ
ใบงานนี้ มีวัตถุประสงค์ เพื่อให้นักศึกษา ได้รู้จักกับ GDI+ ซึ่งจะช่วยให้นักษาสามารถ

* วาดรูปร่างต่างๆ โดยใช้ GDI+ ได้

## การใช้งานแปรงระบายสี (Brush)
แปรงระบายสี ช่วยให้เราสามารถระบายสีแบบต่างๆ ให้กับรูปร่างต่างๆ ได้ตามต้องการ ใน GDI+ มีแปรงระบายสีอยู่ 5 รูปแบบด้วยกัน ประกอบด้วย ```SolidBrush```, ```HatchBrush```, ```TextureBrush```, ```LinearGradientBrush``` และ ```PathGradientBrush``` ซึ่งทั้งหมดจะอยู่ในคลาส ```Brush``` 

### การระบายสีด้วย SolidBrush
* แก้ไข code ต่อไปนี้ในฟังก์ชัน ```private void Form1_Paint(object sender, PaintEventArgs e)```
<p align = "center">
<img src= "https://github.com/Desktop-Programming-Lab-2559/LAB-11/blob/master/imgs/lab11-1.png">
</p>
 ###ผลการทดลอง
 ![](https://scontent.fbkk2-3.fna.fbcdn.net/v/t34.0-12/15151540_1142160405904209_1648822479_n.png?oh=53253b10ddbe6bcb3569205630c00d9f&oe=58304E7A)
<hr>
### การระบายสีด้วย HatchBrush
* แก้ไข code ต่อไปนี้ในฟังก์ชัน ```private void Form1_Paint(object sender, PaintEventArgs e)```
 <p align = "center">
<img src= "https://github.com/Desktop-Programming-Lab-2559/LAB-11/blob/master/imgs/lab11-2.png">
</p>
###ผลการทดลอง
 ![](https://scontent.fbkk2-3.fna.fbcdn.net/v/t34.0-12/15050396_1142160422570874_324611034_n.png?oh=c47b872bf1eba7f47dbc4c0daacc4d8c&oe=58318085)
<hr>
 
### การระบายสีด้วย TextureBrush
* แก้ไข code ต่อไปนี้ในฟังก์ชัน ```private void Form1_Paint(object sender, PaintEventArgs e)```
  <p align = "center">
<img src= "https://github.com/Desktop-Programming-Lab-2559/LAB-11/blob/master/imgs/lab11-3.png">
</p>
**หมายเหตุ** ชื่อรูปในบรรทัดที่ 22 ให้เปลี่ยนเป็นที่ตั้งจริงของรูปที่นักศึกษาใช้
###ผลการทดลอง
 ![](https://scontent.fbkk2-3.fna.fbcdn.net/v/t34.0-12/15139393_1142160415904208_1816170851_n.png?oh=70ea83097cad1d026b519eb7017f4efb&oe=58311489)
<hr>
### การระบายสีด้วย TextureBrush
* ให้วางคอนโทรล Panel จำนวน 2 ตัวลงบน Form โดยมีชื่อว่า panel1 และ panel2 ตามลำดับ
 * เพิ่ม paint event ให้กับ panel ทั้งสองตัว
  <p align = "center">
<img src= "https://github.com/Desktop-Programming-Lab-2559/LAB-11/blob/master/imgs/lab11-4.png">
</p>
* แก้ไข code ต่อไปนี้ในฟังก์ชัน ```private void palen1_Paint(object sender, PaintEventArgs e)```
  <p align = "center">
<img src= "https://github.com/Desktop-Programming-Lab-2559/LAB-11/blob/master/imgs/lab11-5.png">
</p> 

* แก้ไข code ต่อไปนี้ในฟังก์ชัน ```private void palen2_Paint(object sender, PaintEventArgs e)```
   <p align = "center">
<img src= "https://github.com/Desktop-Programming-Lab-2559/LAB-11/blob/master/imgs/lab11-6.png">
</p>

###ผลการทดลอง
 ![](https://scontent.fbkk2-3.fna.fbcdn.net/v/t34.0-12/15128553_1142160409237542_989325675_n.png?oh=baf41c7ec7daf183e0fda37707552332&oe=583051FE)
<hr>


### การระบายสีด้วย Path Gradient Brush

การระบายสีด้วย Path Gradient Brush เป็นการไล่เฉดสีตาม path ที่กำหนด ในโปรแกรมตัวอย่างนี้จะวาดวงรีและไล่เฉดสีจากด้านในออกสู่ด้านนอก
* การทดลอง 
 * ให้ลดขนาด panel1 และ panel2 ลง แล้วเพิ่ม panel3 เข้าไปใน form1 ดังรูป
    <p align = "center">
<img src= "https://github.com/Desktop-Programming-Lab-2559/LAB-11/blob/master/imgs/lab11-7.png">
</p>

 * เพิ่ม Paint event ให้กับ Panel3
* แก้ไข code ต่อไปนี้ในฟังก์ชัน ```private void palen3_Paint(object sender, PaintEventArgs e)```
<p align = "center">
<img src= "https://github.com/Desktop-Programming-Lab-2559/LAB-11/blob/master/imgs/lab11-8.png">
</p>

###ผลการทดลอง
 ![](https://scontent.fbkk2-3.fna.fbcdn.net/v/t34.0-12/15134357_1142160419237541_809384272_n.png?oh=61aa9e9e37040afcf59dabef039ba3fb&oe=583112BC)
<hr>

###แบบทดสอบ 
ให้เลื่อนจุดศูนย์กลางและปรับเปลี่ยนสี ให้ได้รูปดังนี้
<p align = "center">
<img src= "https://github.com/Desktop-Programming-Lab-2559/LAB-11/blob/master/imgs/lab11-9.png">
</p>

###ผลการทดลอง
 ![](https://scontent.fbkk2-3.fna.fbcdn.net/v/t34.0-12/15135483_1142160412570875_325279909_n.png?oh=57a4b43e2e9bf307849226c9a35612b3&oe=58311D53)
<hr>
<hr>
Ailada Samingkaew 57030249
<hr>
<hr>

