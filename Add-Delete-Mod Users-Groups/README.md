<br>

# 👤 Add/Delete/Mod Users/Groups

### Create User (useradd/adduser)

useradd เป็นคำสั่ง Linux สำหรับสร้างผู้ใช้ใหม่ ต้องใช้ตัวเลือกต่าง ๆ เพื่อเพิ่มและตั้งค่าบัญชีผู้ใช้ที่ใช้งานอยู่ นอกจากนี้ คำสั่งอนุญาตให้เปลี่ยนค่าเริ่มต้นสำหรับกระบวนการสร้างผู้ใช้ด้วย

ป้อนคำสั่ง `useradd` เพื่อเพิ่มผู้ใช้ใหม่ :
		
	sudo useradd <username>
หลังจากป้อนรหัสผ่าน sudo คำสั่งจะสร้างผู้ใช้ใหม่ด้วยชื่อผู้ใช้ test_user และจะไม่มีการสร้างเอาต์พุตใด ๆ useradd จะใช้ตัวเลือกที่กำหนดค่าไว้ล่วงหน้าจากไฟล์ `/etc/useradd` โดยอัตโนมัติ อย่างไรก็ตาม ผู้ใช้จำเป็นต้องมีการตั้งค่าเพิ่มเติมด้วยคำสั่ง `passwd` เพื่อเป็นการใช้งานบัญชี

หากต้องการดูตัวเลือกทั้งหมดที่มี ให้ใช้แท็ก -h :
		
	useradd -h
หรือใช้คำสั่ง `man` เพื่อดูหน้าคู่มือฉบับสมบูรณ์

คำสั่ง adduser ทำหน้าที่สร้างผู้ใช้ใหม่บนระบบ Linux
 การรันคำสั่งจำเป็นต้องระบุ home directory และเพิ่มเชลล์เริ่มต้นให้เป็นแบบ Bash อย่างไรก็ตาม *ข้อเสีย*ของ adduser คือ มีตัวเลือกในการจัดการที่ค่อนข้างน้อย และ รองรับแค่กับระบบ Linux บางรุ่น
 
 - หากต้องการดูวิธีการทำงานของ adduser ให้รันคำสั่งต่อไปนี้ใน terminal:
 
		sudo adduser <username>

<table align="center">
	<tr>
		<th>Files</th>
		<th>Description </th>
	</tr>
	<tr>
		<td>/etc/passwd</td>
		<td>information regarding users’ accounts</td>
	</tr>
  <tr>
		<td>/etc/shadow</td>
		<td>user security-related information</td>
  </tr>
  <tr>
		<td>/etc/group</td>
		<td>information about groups</td>
  </tr>
  <tr>
		<td>/etc/gshadow</td>
		<td>group security-related information</td>
  </tr>
  <tr>
		<td>/etc/login.defs</td>
		<td>shadow password suite configuration</td>
  </tr>
<table>

<br><br>
### Modify Default User Settings (usermod)

usermod เป็นคำสั่งที่ผู้ดูแลระบบมีไว้เพื่อการจัดการผู้ใช้ เพื่อแก้ไขรายละเอียดบัญชีผู้ใช้ที่มีอยู่ เช่น ชื่อผู้ใช้ รหัสผ่าน ตำแหน่ง home directory เชลล์เริ่มต้น และอื่นๆ

ไวยากรณ์พื้นฐานสำหรับคำสั่ง `usermod` คือ :

	usermod [options] [username]

 <table align="center">
	<tr>
		<th>Files</th>
		<th>Description </th>
	</tr>
	<tr>
		<td>/etc/passwd</td>
		<td>information regarding users’ accounts</td>
	</tr>
  <tr>
		<td>/etc/shadow</td>
		<td>user security-related information</td>
  </tr>
  <tr>
		<td>/etc/group</td>
		<td>information about groups</td>
  </tr>
  <tr>
		<td>/etc/gshadow</td>
		<td>group security-related information</td>
  </tr>
  <tr>
		<td>/etc/login.defs</td>
		<td>shadow password suite configuration</td>
  </tr>
<table>

<br><br>**`usermod` Command Examples**

- Set User’s Home Directory

หากผู้ใช้ต้องการเปลี่ยนตำแหน่ง home directory ให้ใช้ตัวเลือก -d :

	sudo usermod -d [directory-location] [username]

> แต่เนื่องด้วยตัวเลือก -d จะไม่ย้ายเนื้อหาของ home directory ไปยังตำแหน่งใหม่ หากผู้ใช้เคยใช้ home directory เพื่อจัดเก็บไฟล์ ให้เพิ่มตัวเลือก -m เพื่อย้ายเนื้อหา home directory ของผู้ใช้ :

	sudo usermod -d [location] -m [username]

- Change Password for a User

หากผู้ใช้ต้องการเปลี่ยนรหัสผ่าน ให้ป้อนคำสั่ง `passwd` :

	sudo passwd <username>

- Change User’s Primary Group

หากผู้ใช้ต้องการเปลี่ยน primary group ให้ใช้ตัวเลือก -g :

	sudo usermod -g [group] [username]

> นอกเหนือจาก primary group แล้ว ผู้ใช้ยังสามารถเป็นสมาชิกของ supplementary group จำนวนเท่าใดก็ได้ โดยตัวเลือก -G จะเพิ่มผู้ใช้ใน supplementary group :

	sudo usermod -G [group] [username]

หากต้องการอ่านวิธีใช้ usermod ให้ใช้ argument `–help` :

	usermod --help

หรือถ้าต้องการดูรายการตัวเลือกและฟังก์ชันแบบละเอียด ให้ป้อนคำสั่ง `man`

<br><br>
### Delete User (userdel)

userdel เป็นคำสั่งที่ใช้สำหรับการลบผู้ใช้ (user) ออกจากระบบ

**Options ที่มีอยู่ในคำสั่ง `userdel`**

<table align="center">
	<tr>
		<th>Option</th>
		<th>Description </th>
	</tr>
	<tr>
		<td>-f</td>
		<td>Force removal of the user account, including home directory and mail spool, even if the user is logged in.</td>
	</tr>
  <tr>
		<td>-r</td>
		<td>Remove the user’s home directory along with the account. Useful for a complete cleanup.</td>
  </tr>
  <tr>
		<td>-h</td>
		<td>Display a help message and exit, providing information on command syntax and available options.</td>
  </tr>
  <tr>
		<td>-R</td>
		<td>Apply changes in the specified CHROOT_DIR, useful for user deletion operations within a chroot environment.</td>
  </tr>
  <tr>
		<td>-Z</td>
		<td>Remove SELinux user mapping for the user’s login, applicable in SELinux-enabled systems.</td>
  </tr>
  <tr>
		<td>-help</td>
		<td>Display a help message with the general syntax and available options for the userdel command.</td>
  </tr>
<table>

<br><br>ไวยากรณ์พื้นฐานสำหรับคำสั่ง `userdel` คือ :

	userdel [options] <username>

 > หากผู้ใช้ต้องการลบ home directory ให้ใช้ตัวเลือก -r :

	sudo userdel -r <username>

 ***Note : การดำเนินการนี้ไม่สามารถย้อนกลับได้ โดยเฉพาะเมื่อใช้ตัวเลือก -r  ดังนั้นควรดำเนินการด้วยความระมัดระวัง***

 <br><br>
### Linux User Group Management Commands

ใน Linux ผู้ใช้จะมีบทบาทหรือความรับผิดชอบที่แตกต่างกัน ผู้ใช้บางคนอาจถูกจำกัดไม่ให้เข้าถึงไฟล์และโฟลเดอร์เฉพาะ
Groups จึงหมายถึงกลุ่มของผู้ใช้ที่มีสิทธิ์และการเข้าถึงตามการกำหนดสิทธิ์และการอนุญาตของระบบ โดยผู้ใช้ที่เป็นสมาชิกของกลุ่มเดียวกันสามารถแบ่งปันแฟ้มและทรัพยากรอื่น ๆ ในระบบได้

**แบ่งออกเป็น 2 ประเภท**

- Primary Group

เมื่อทำการสร้างผู้ใช้ Primary Group ที่มีชื่อเดียวกันกับผู้ใช้จะถูกสร้างขึ้น โดยที่ผู้ใช้สามารถอยู่ใน Primary Group ได้ครั้งละหนึ่งกลุ่มเท่านั้น

- Secondary Groups

ผู้ใช้สามารถอยู่ใน Secondary Groups จำนวนเท่าใดก็ได้ (หรือไม่อยู่เลยก็ได้) Secondary Groups ถูกสร้างขึ้นเพื่อจัดการไฟล์และแอปพลิเคชันซอฟต์แวร์แต่ละไฟล์ สมาชิกของกลุ่มสามารถสืบทอดสิทธิ์การอ่าน เขียน และดำเนินการสำหรับกลุ่มนั้น

<br><br>
### **Create Group**

ป้อนคำสั่ง `groupadd` เพื่อสร้างกลุ่มผู้ใช้ใหม่ :

	sudo groupadd <groupname>

 **Options ที่มีอยู่ในคำสั่ง `groupadd`**

 <table align="center">
	<tr>
		<th>Option</th>
		<th>Description </th>
	</tr>
	<tr>
		<td>-f, –force</td>
		<td>This option forces the command to silently abort if the group with the given name already exists. If used with the -g or –gid option and the specified group id already exists, the command forcefully ignores the given group id and assigns a new and unique group id.</td>
	</tr>
  <tr>
		<td>-g GID, –gid GID</td>
		<td>This option assigns a specific numeric group id to the newly created group.
The group id (GID) should be non-negative and unique, unless explicitly created to be non-unique using the -o or –non-unique option.
If not specified, the command assigns a default group id greater than any existing group id.
</td>
  </tr>
  <tr>
		<td>-h, –help</td>
		<td>Displays a help message, providing information about the groupadd command and its available options.
Useful for quickly accessing command documentation.
</td>
  </tr>
  <tr>
		<td>-K KEY=VALUE, –key KEY=VALUE</td>
		<td>Overrides the default values set in the /etc/login.defs file.
Multiple -K options can be specified.
Parameters like GID_MIN and GID_MAX, defined in /etc/login.defs, can be modified using this option.
</td>
  </tr>
  <tr>
		<td>-o, –non-unique</td>
		<td>Permits adding a group with a non-unique group id (GID).
Useful when you want to create groups with duplicate GIDs.
</td>
  </tr>
  <tr>
		<td>-p PASSWORD, –password PASSWORD</td>
		<td>Sets an encrypted password for the group.
The password, returned by crypt(3), is visible to users and is stored in the /etc/gshadow file. By default, the password is disabled, and it is crucial to ensure it adheres to the system’s password policy.
</td>
  </tr>
</tr>
  <tr>
		<td>-r, –system</td>
		<td>Creates a system group. System groups have numeric identifiers chosen within the SYS_GID_MIN-SYS_GID_MAX range, as defined in the /etc/login.defs file, instead of GID_MIN and GID_MAX.</td>
  </tr>
<tr>
		<td>-R CHROOT_DIR, –root CHROOT_DIR</td>
		<td>Applies changes in the specified CHROOT_DIR directory and uses the configuration files from that directory.
Useful when managing groups within a chroot environment. </td>
  </tr>
<table>

<br><br>
### **Modify a Group**

groupmod มีหน้าที่เพื่อแก้ไขหรือเปลี่ยนแปลงกลุ่มที่มีอยู่ในระบบ Linux สามารถจัดการได้โดยผู้ใช้ระดับสูงหรือผู้ใช้รูท

ไวยากรณ์พื้นฐานสำหรับคำสั่ง `groupmod` คือ :

	groupmod [options] <groupname>

**Files** : คำสั่ง `groupmod` มีไฟล์ดังต่อไปนี้

 <table align="center">
	<tr>
		<th>Files</th>
		<th>Description </th>
	</tr>
	<tr>
		<td>/etc/passwd</td>
		<td>information regarding users’ accounts</td>
	</tr>
  <tr>
		<td>/etc/group</td>
		<td>information about groups</td>
  </tr>
  <tr>
		<td>/etc/gshadow</td>
		<td>group security-related information</td>
  </tr>
  <tr>
		<td>/etc/login.defs</td>
		<td>shadow password suite configuration</td>
  </tr>
<table>

<br><br>
**Options** : มีตัวเลือกต่อไปนี้ในคำสั่ง `groupmod`

<table align="center">
	<tr>
		<th>Option</th>
		<th>Description </th>
	</tr>
  <tr>
		<td>-g GID, –gid GID</td>
		<td>The group ID of the given GROUP will be changed to GID.</td>
  </tr>
<tr>
		<td>-n, –new-name NEW_GROUP</td>
		<td>The name of group will change into newname.</td>
  </tr>
  <tr>
		<td>-h, –help</td>
		<td>This option display help message and exist.
</td>
  </tr>
  <tr>
		<td>-K KEY=VALUE, –key KEY=VALUE</td>
		<td>Overrides the default values set in the /etc/login.defs file.
Multiple -K options can be specified.
Parameters like GID_MIN and GID_MAX, defined in /etc/login.defs, can be modified using this option.
</td>
  </tr>
  <tr>
		<td>-o, –non-unique</td>
		<td>This option used with the -g option that allow to change the group GID to a non-unique value.
</td>
  </tr>
  <tr>
		<td>-p , –password PASSWORD</td>
		<td>This gives the encrypted password
</td>
  </tr>
</tr>
  <tr>
		<td>-r, –system</td>
		<td>Creates a system group. System groups have numeric identifiers chosen within the SYS_GID_MIN-SYS_GID_MAX range, as defined in the /etc/login.defs file, instead of GID_MIN and GID_MAX.</td>
  </tr>
<tr>
		<td>-R , –root CHROOT_DIR</td>
		<td>Apply changes in the CHROOT_DIR directory and use the configuration files from the CHROOT_DIR directory.</td>
  </tr>
<table>

<br><br>
### **Delete a Group**

ไวยากรณ์พื้นฐานสำหรับคำสั่ง `groupdel` คือ :

	groupdel [options] <groupname>

**Files** : คำสั่ง `groupdel` มีไฟล์ดังต่อไปนี้

<table align="center">
	<tr>
		<th>Files</th>
		<th>Description </th>
	</tr>
  <tr>
		<td>/etc/group</td>
		<td>It contains the account information of the Group.</td>
  </tr>
<tr>
		<td>/etc/gshadow</td>
		<td>It contains the secure group account information.</td>
  </tr>
<table>

<br><br>

**Options** : มีตัวเลือกต่อไปนี้ในคำสั่ง `groupdel`

<table align="center">
	<tr>
		<th>Option</th>
		<th>Description </th>
	</tr>
  <tr>
		<td>-h, –help</td>
		<td>Displays the help message and exits.</td>
  </tr>
<tr>
		<td>-f, –force</td>
		<td>This option forces the deletion of the group, even if it is still in use.</td>
  </tr>
  <tr>
		<td>-R, –root</td>
		<td>It apply the changes in the CHROOT_DIR directory. Also, it uses the configuration files from the CHROOT_DIR directory.</td>
  </tr>
  <tr>
		<td>-r, –remove</td>
		<td>Removes the group along with its associated files.</td>
<table>

<br>

**- บทถัดไป [User Policy และ Password Policy](https://github.com/Pooh303/User-Access-Management-3/tree/main/User%20Policy%2C%20Password%20Policy)**
