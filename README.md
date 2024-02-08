# Yandex_scoter_api_test_13
Задание №1

Задание 1.

SELECT c.login, COUNT (o."courierId")
FROM "Couriers"
AS c JOIN "Orders"
AS o ON c id = o. "courierId"
WHERE O. "inDelivery" = true
GROUP BY c.login;

Приходят задвоенные данные!

Задание №2

SELECT
 track,
 CASE
   WHEN finished = true THEN 2
   WHEN cancelled = true THEN -1
   WHEN "inDelivery" = true THEN 1
   ELSE 0
 END AS status
FROM "Orders"
AS o;
