Angular-DotNet-SQL
מערכת ניהול משימות Full Stack באמצעות Angular, .NET Web API ו-SQL Server Stored Procedures

מערכת ניהול משימות
1. נושא הפרוייקט
מערכת לניהול משימות עם אפשרות ליצירה, עריכה, צפייה ומחיקה של משימות. מאפשרת ארגון משימות לפי סטטוס וקטגוריה, עם מעקב אחר תאריכי יצירה ויעד.

2. תיאור הטבלאות והקשרים
טבלאות:
משימות (טבלה ראשית)

ID - מזהה ייחודי (מפתח ראשי)
כותרת - כותרת המשימה
תיאור - תיאור המשימה
StatusId - מזהה סטטוס (מפתח זר ל-Statuses)
CategoryId - מזהה קטגוריה (מפתח זר ל-קטגוריות)
CreatedAt - תאריך יצירה
תאריך יעד - תאריך יעד
סטטוסים (טבלת סטטוסים)

ID - מזהה ייחודי (מפתח ראשי)
שם - הסטטוס (חדש, עונה, הושלם)
קטגוריות (טבלת קטגוריות)

ID - מזהה ייחודי (מפתח ראשי)
שם - שם הקטגוריה (עבודה, אישי, דחוף)
קשרים:
Tasks.StatusId → Statuses.Id (מפתח זר)
Tasks.CategoryId → Categories.Id (מפתח זר)
3. רשימת נהלים מאוחסנים
Tasks_Create - יצירת משימה חדשה
Tasks_Update - עדכון משימה קיימת
Tasks_GetById - שליפת משימה לפי מזהה (כולל JOIN לשמות מותרים)
Tasks_GetAll - שליפת כל המשימות (כולל JOIN)
משימות_מחק - מחיקת משימה
Statuses_GetAll - שליפת כל הסטטוסים
Categories_GetAll - שליפת כל הקטגוריות
4. הרצת הפרוייקט
מסעד נתונים:
פתח SQL Server Management Studio
התחבר לשרת:MININT-OUNN1FJ\SQLEXPRESS
הרץ את הסקריפט ליצירת מסד והטבלאות
הרץ את כל ה-Stored Procedures
הרץ את additional-procedures.sql להוספת נתוני דוגמה
צד שרת (.NET API):
פתח את הפרויקט ב-Visual Studio
ודא שמחרוזת החיבור ב-appsettings.json נכונה:
Server=MININT-OUNN1FJ\\SQLEXPRESS;Database=TaskManagement;Integrated Security=True;TrustServerCertificate=True;Encrypt=False;
הרץ את הפרויקט (F5)
ה-API ירוץ על: http://localhost:5258
צד לקוח (אנגולר):
לקוח פתח מסוף בתיקיית
הרץ: npm install(פעם ראשונה בלבד)
הרץ:ng serve
פתח דפדפן בכתובת: http://localhost:4200
מְשָׁכִים בְּמַעֲרָכָה
רשימת מסך (/משימות) - הצגת כל המשימות עם חיפוש ופתורי פעולה
מסך יצירה/עריכה (/tasks/new, /tasks/edit/:id) - טופס Reactive Forms
מסך פרטים (/tasks/:id) - הצגת כל פרטי המשימה
אוֹדוֹת
מערכת ניהול משימות Full Stack באמצעות Angular, .NET Web API ו-SQL Server Stored Procedures

אֶמְצָעִי
 קריאה
 פְּעִילוּת
כוכבים
 כוכב אחד
צופים
 0 צופים
מזלגות
 0 מזלגות
מאגר דוחות
מהדורות
לא פורסמו מהדורות
חבילות
לא פורסמו חבילות
תורמים
1
@רבקה-ניסאן
רבקה-ניסאן
שפות
טייפסקריפט
39.0%
 
HTML
21.1%
 
C#
14.7%
 
TSQL
13.5%
 
CSS
11.7%
כותרת תחתונה
יעל לימואי
