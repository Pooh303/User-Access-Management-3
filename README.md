# 🧑🏽‍💻 User Access Management

กระบวนการในการจัดการผู้ใช้และสิทธิ์ในการเข้าถึงระบบและทรัพยากรต่างๆ ซึ่งเป็นสิ่งสำคัญสำหรับการรักษาความปลอดภัยของระบบ การป้องกันการเข้าถึงโดยไม่ได้รับอนุญาต และการกำนหดควบคุมว่าใครสามารถทำอะไรได้บ้าง

มีองค์ประกอบหลักหลายอย่างที่ทำงานร่วมกัน ช่วยให้มั่นใจได้ว่าบุคลใดๆสามารถเข้าถึงทรัพยากรได้ในเวลาที่ถูกต้องและเหมาะสม  อีกทั้งป้องกันไม่ให้บุคคลใดๆที่ไม่ได้รับอนุญาตมีสิทธิ์ที่จะเข้าถึงทรัพยากรเหล่านั้นได้


## Subcomponents_Overview 🔍

**ภาพรวมขององค์ประกอบต่างๆ**

1. [Add/Delete/Mod Users/Groups](https://github.com/Pooh303/User-Access-Management-3/tree/main/Add-Delete-Mod%20Users-Groups) ฟังก์ชั่นพื้นฐานสำหรับการจัดการผู้ใช้และการเข้าถึงในระบบคอมพิวเตอร์ ซึ่งมีความสำคัญต่อการรักษาความปลอดภัยและควบคุมการเข้าถึงข้อมูลและทรัพยากรของระบบ

2. [User Policy และ Password Policy](https://github.com/Pooh303/User-Access-Management-3/tree/main/User%20Policy%2C%20Password%20Policy) เครื่องมือสำคัญในการรักษาความปลอดภัยของระบบคอมพิวเตอร์ โดยการกำหนดกฎเกณฑ์สำหรับบัญชีผู้ใช้และรหัสผ่าน ช่วยให้ผู้ดูแลระบบสามารถควบคุมการเข้าถึงข้อมูลและทรัพยากรของระบบและป้องกันการใช้งานโดยไม่ได้รับอนุญาต

3. [Authentication/IDM/SSO](https://github.com/Pooh303/User-Access-Management-3/tree/main/Authentication-IDM-SSO) เทคโนโลยีที่สำคัญในการรักษาความปลอดภัยของระบบคอมพิวเตอร์ โดยช่วยให้ผู้ดูแลระบบสามารถควบคุมการเข้าถึงระบบ ข้อมูล และทรัพยากรต่างๆ ได้อย่างมีประสิทธิภาพ

4. [Authorization](https://github.com/Pooh303/User-Access-Management-3/tree/main/Authorization) ระบบการรักษาความปลอดภัยที่กำหนดระดับสิทธิ์การเข้าถึงของผู้ใช้ผ่านตัวตนที่ได้มีการยืนยันไว้แล้ว

5. [Access Control, Firewall](https://github.com/Pooh303/User-Access-Management-3/tree/main/Access%20Control%2C%20Firewall) เทคโนโลยีที่ใช้ควบคุมการเข้าถึง และกรองรับส่งข้อมูลระหว่างเครือข่าย Access Control ใช้ในการควบคุมและจำกัดการเข้าถึงทรัพยากรในระบบคอมพิวเตอร์ ในขณะที่ Firewall เป็นระบบป้องกันการบุกรุกที่ใช้เพื่อกรองและควบคุมการไหลของข้อมูลในเครือข่าย


## นำเสนอ
<img style="height:10vh" src="https://media.discordapp.net/attachments/699878120421064796/1205217109290918028/Sumet.png">

**ผู้ช่วยศาสตราจารย์ ดร. สุเมธ ประภาวัต**

  - อาจารย์ประจำคณะเทคโนโลยีสารสนเทศ สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง

## Collaborator ✨
<table>
  <tr>
    <th>Student ID</th>
    <th>Name</th>
    <th>Duty</th>
    <th>Profile</th>
  </tr>
  <tr>
    <td>65070091</td>
    <td>นาย ธนดล  กองสุข</td>
    <td align="center">User Policy, Password Policy</td>
    <td><img style="height:200px" src="https://cdn.discordapp.com/attachments/1205566248105017374/1205575895012876319/gun.jpg?ex=65d8df0b&is=65c66a0b&hm=bc57821b2f1b85c7f7c06f405ccecf2402fb6af5bdae47b4d818578517919edc&"></td>
  </tr>
  <tr>
    <td>65070178</td>
    <td>นาย ภูมิไชย  อุดมศิลป์</td>
    <td align="center">Authentication/SSO</td>
    <td><img style="height:200px" src="https://cdn.discordapp.com/attachments/1205566248105017374/1205575896002465873/poom.jpg?ex=65d8df0c&is=65c66a0c&hm=6b868c72497dd21f8eafda860157e7c7ea855b7a59d09556d536c09c2967c216&"></td>
  </tr>
  <tr>
    <td>6070180</td>
    <td>นาย ภูรินท์  ดวงมาลย์</td>
    <td align="center">Authorization</td>
    <td><img style="height:200px;"
src="https://cdn.discordapp.com/attachments/1205566248105017374/1205575891736854610/AJ.jpg?ex=65d8df0b&is=65c66a0b&hm=2c2dea0367ca2dd4bf156574a4a038cf15369c82d0384faf1d896780d7669a13&"></td>
  </tr>
  <tr>
    <td>65070182</td>
    <td>นาย ภูวดล  ศรีพันนา</td>
    <td align="center">GitHub / Overview</td>
    <td><img style="height:200px;"
src="https://cdn.discordapp.com/attachments/1205566248105017374/1205575893813170176/dream.jpg?ex=65d8df0b&is=65c66a0b&hm=510384a677159a463662cc77a66e8fb306b5b2bbb90a51772220549ed51869ae&"></td>
  </tr>
  <tr>
    <td>65070199</td>
    <td>นางสาว รุ่งนภา  แช่มชื่น</td>
    <td align="center">Add/Delete/Mod Users/Groups</td>
    <td><img style="height:200px"
src="https://media.discordapp.net/attachments/1205566248105017374/1205575892433375302/areyou.jpg?"></td>
  </tr>
  <tr>
    <td>65070220</td>
    <td>นาย ศิวกร  สมจิตร์</td>
    <td align="center">User/Access Management</td>
    <td><img style="height:200px;"
src="https://cdn.discordapp.com/attachments/1205566248105017374/1205575893083365507/com.jpg?ex=65d8df0b&is=65c66a0b&hm=2dd85599816388bd582c6bc505acb9c4d215754bb31d061b22f5e5cce5f7dcfa&"></td>
  </tr>
  <tr>
    <td>65070248</td>
    <td>นาย อนุวัติพงษ์  พลสำราญ</td>
    <td align="center">Access Control, Firewall</td>
    <td><img style="height:200px;" src="https://media.discordapp.net/attachments/1205566248105017374/1205575895520247818/meen.jpg"></td>
  </tr>
</table>

<br>

## Sources
#### User/Access Management
  https://phoenixnap.com/kb/user-management-linux

* ##### Add/Delete/Mod Users/Groups
  
  https://www.redhat.com/sysadmin/linux-groups
  
  https://www.geeksforgeeks.org/userdel-command-in-linux-with-examples/?ref=lbp
  
  https://www.geeksforgeeks.org/groupadd-command-in-linux-with-examples/?ref=lbp
  
  https://www.geeksforgeeks.org/groupmod-command-in-linux-with-examples/?ref=lbp
  
  https://www.geeksforgeeks.org/groupdel-command-in-linux-with-examples/?ref=lbp
  
  https://phoenixnap.com/kb/useradd-vs-adduser
  
  https://phoenixnap.com/kb/usermod-linux#usermod-linux-syntax
  
  https://phoenixnap.com/kb/user-management-linux#ftoc-heading-6
  
  https://phoenixnap.com/kb/add-user-to-linux-group
  
* ##### User Policy, Password Policy
  https://en.wikipedia.org/wiki/Password_policy
  
  https://ubuntu.com/server/docs/security-users

  - User Policy

  https://ubuntu.com/server/docs/security-users

  - Password Policy
  
  https://www.baeldung.com/linux/password-complexity

  https://askubuntu.com/questions/244115/how-do-i-enforce-a-password-complexity-policy
 
  https://www.server-world.info/en/note?os=Ubuntu_20.04&p=password

  https://www.nokhosting.com/info/command-line-linux
  
* ##### Authentication/IDM/SSO
  https://en.wikipedia.org/wiki/Single_sign-on
  
  https://en.wikipedia.org/wiki/Identity_management
  
  https://en.wikipedia.org/wiki/Authentication

  https://linuxhint.com/linux-authentication-systems/

  https://www.debian.org/doc/manuals/debian-reference/ch04.en.html#_normal_unix_authentication

  https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/identity_management_guide/introduction

  https://www.cloudflare.com/learning/access-management/what-is-sso/
  
* ##### Authorization

  https://monsterconnect.co.th/authentication-vs-authorization/

  https://www.hostinger.com/tutorials/sudo-and-the-sudoers-file/

  https://saixiii.com/chown-linux-command/

  https://saixiii.com/chmod-linux-command/

  https://saixiii.com/chgrp-linux-command/

  https://www.ibm.com/docs/en/zos/2.2.0?topic=scd-getfacl-display-owner-group-access-control-list-acl-entries

  https://www.ibm.com/docs/en/zos/3.1.0?topic=scd-setfacl-set-remove-change-access-control-lists-acls#sfacl__title__3
  
* ##### Access Control, Firewall

  https://www.pdpaplus.com/Article/Detail/138148/Firewall

  https://www.vulcan-tec.com/access-control
  
  https://www.xylem.com/siteassets/about-xylem/cybersecurity/advisories/xpsa---apache---log4j-v3.0-.pdf
  
  https://www.cisa.gov/news-events/news/apache-log4j-vulnerability-guidance
  
  https://firewalld.org/documentation/
