# הכוח שבך — פריסה ל-Windows Server / IIS

האתר בשלב זה סטטי: HTML/CSS. אין צורך ב-Node.js, במסד נתונים או בשרת אפליקציה.

## הכנה
1. ב-IIS צור אתר נפרד בשם Hacoach (אין לשנות את האתר של טוהר).
2. הגדר Physical Path, למשל C:\\Sites\\Hacoach.
3. הגדר Application Pool ייעודי עם **No Managed Code**.
4. הגדר Binding לדומיין המיועד רק אחרי שה-DNS מכוון לשרת.
5. התקן אישור HTTPS מתאים, והוסף binding ל-443.

## פריסה
פתח PowerShell בשרת:

```powershell
git clone --branch develop/mobile-first-rebuild https://github.com/onoadir-cloud/hacoach-website.git C:\Sites\Hacoach
```

אם המאגר פרטי, השתמש באמצעי אימות מאובטח של Git ולא בסיסמה בקובץ.

לעדכון גרסה לאחר אישור:
```powershell
cd C:\Sites\Hacoach
git pull --ff-only
```

## בדיקות
- פתח את כתובת האתר דרך HTTPS בסלולר ובמחשב.
- ודא שהקישורים והניווט עובדים ושאין שגיאות 404.
- לפני פרסום: השלם תמונות, סיפורי מקרה, פרטי קשר ומדיניות פרטיות.
- לאחר אישור הגרסה, עבור לענף הראשי לפריסת production.

אין להגדיר כרגע הפניה אוטומטית לדומיין הפעיל או להחליף אתר קיים.
