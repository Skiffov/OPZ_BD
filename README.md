# OPZ_BD
Курсова робота (База данних)"Облік програмного забезпечення"

Курсову роботу виконує Герман Олександр Сергійович ІПЗ-21

# Схема

![image](https://github.com/Skiffov/OPZ_BD/assets/51057115/11b75e13-7dab-4f42-8565-d0f8a88dc8f1)
[`Код бази`](BD.mysql)
# Тести

   1. Отримання інформації про програмне забезпечення та відповідний постачальник:

SELECT s.Name AS SoftwareName, s.Version, s.Cost, sup.Name AS SupplierName  
FROM Software s  
JOIN Suppliers sup ON s.SupplierID = sup.SupplierID;

 Результат: 

![Screenshot_20231206_121642](https://github.com/Skiffov/OPZ_BD/assets/51057115/b76cee66-69df-4fa8-82ab-dfec2a44f485)

   2. Перегляд інформації про оновлення програмного забезпечення:

SELECT su.UpdateID, su.SoftwareID, su.UpdateDate, su.Description,  
s.Name AS SoftwareName, s.Version  
FROM SoftwareUpdates su  
JOIN Software s ON su.SoftwareID = s.SoftwareID;

Результат: 

![Screenshot_20231206_121642](https://github.com/Skiffov/OPZ_BD/assets/51057115/62cb6d5f-f0e4-4a50-955e-6ab7e09f1bae)

   3. Вибірка користувачів та відповідних відомостей про програмне забезпечення:

   SELECT u.UserID, u.UserName, u.DepartmentID,  
   s.Name AS SoftwareName, s.Version, s.LicenseType,  
   lk.LicenseKey, lk.SerialNumber, lk.ExpiryDate  
   FROM Users u  
   JOIN Software s ON u.SoftwareID = s.SoftwareI  
   LEFT JOIN LicenseKeys lk ON u.LicenseKeyID = lk.LicenseKeyID;

Результат: 

![Screenshot_20231206_122857](https://github.com/Skiffov/OPZ_BD/assets/51057115/b58e383d-f3c0-4aa2-b5a9-57980d6dbdad)

