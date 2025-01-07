

#### بداية التعامل مع استعلامات SQL الأساسية

![image](https://github.com/user-attachments/assets/ef271a87-906b-4da4-8546-895f9ec28145)

**المهمة 1: التعرف على قواعد البيانات الموجودة في النظام.**

- **الاستعلام:**  
  ```sql
  show databases;
  ```

ده بيعرض قواعد البيانات الموجودة على النظام.

---



![image](https://github.com/user-attachments/assets/c30fa214-1fc8-41fd-b366-4762e4d096b4)


> Query: use wpdatabase;


```
## استخدام قاعدة البيانات `wpdatabase`

الاستعلام `use wpdatabase;` بيستخدم لتحديد قاعدة البيانات اللي هتتعامل معاها في الجلسة الحالية. في المثال ده، بنحدد قاعدة بيانات اسمها `wpdatabase`.
```


---

## عرض الجداول في قاعدة البيانات

![image](https://github.com/user-attachments/assets/ef076e71-b893-4a16-b59f-e152b92567ac)

الاستعلام `show tables;` بيعرض جميع الجداول الموجودة في قاعدة البيانات الحالية اللي شغال عليها.

---

## استرجاع البيانات من جدول `wp_users`

![image](https://github.com/user-attachments/assets/967b9575-f42b-4a35-8b65-cb43ac69c4fb)

الاستعلام `select * from wp_users;` بيجيب كل البيانات الموجودة في جدول `wp_users`. يعني بيعرض جميع الأعمدة والصفوف من الجدول ده.

---


## استرجاع بيانات من أعمدة معينة في جدول `wp_users`

![image](https://github.com/user-attachments/assets/557d8468-e5b0-46ba-92a7-8d2dedc4b486)

الاستعلام `select user_login, user_pass from wp_users;` بيجيب بيانات عمودين فقط من جدول `wp_users`: عمود `user_login` (اسم المستخدم) وعمود `user_pass` (كلمة المرور).
---


## استرجاع البيانات من جدول باستخدام اسم قاعدة البيانات

![image](https://github.com/user-attachments/assets/5ae3ae87-b41f-4db3-8c8c-144c263c3811)
![image](https://github.com/user-attachments/assets/6334fa9f-635c-43ec-bf35-4cc47b79b740)


الاستعلام `select * from wpdatabase.wp_posts;` بيجيب كل البيانات من جدول `wp_posts` في قاعدة البيانات `wpdatabase`. 


---
## الصورة بتوريك لما تدخل '; بيطلع ايرور وبالتالي بتتوقع ان الموقع مصاب ب sQLi  لان الامر بيتم معالجته بواسطة database 

![image](https://github.com/user-attachments/assets/edcbc697-feb2-4237-a5d9-cce9e65f06a0)

---

### طريقة الاستغلال في موقع حقيقي شبه الquery الي في الصورة ونتيجته بيجبلك كل البيانات الي في الجدول باستخدام  or true=true لانه هنا بيشوف لو الامر الاول غلط نفذ الامر الي بعد ال or 

![image](https://github.com/user-attachments/assets/1473e53a-9982-4fae-b70c-1e0574b5525e)

---
