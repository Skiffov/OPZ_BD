# OPZ_BD
Курсова робота (База данних)"Облік програмного забезпечення"

Курсову роботу виконує Герман Олександр Сергійович ІПЗ-21

![image](https://github.com/Skiffov/OPZ_BD/assets/51057115/11b75e13-7dab-4f42-8565-d0f8a88dc8f1)

   1. Отримання інформації про програмне забезпечення та відповідний постачальник:

SELECT s.Name AS SoftwareName, s.Version, s.Cost, sup.Name AS SupplierName
FROM Software s
JOIN Suppliers sup ON s.SupplierID = sup.SupplierID;

 Результат: 

 ![Uploading Screenshot_20231206_121642.png…]()
