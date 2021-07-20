# Patika.dev.sql

## Ödev 1

#### Film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.
```
--1. Soru
SELECT title, description
FROM film;
```

#### Film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.
```
--2. Soru
SELECT *
FROM film
WHERE length > 60 AND length < 75;
```

#### Film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.
```
--3. Soru
SELECT *
FROM film
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);
```

#### Customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?
```
--4. Soru(Smith)
SELECT last_name
FROM customer
WHERE first_name = 'Mary'
```

#### Film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.
```
--5. Soru
SELECT *
FROM film
WHERE NOT (length > 50 OR rental_rate = 2.99 OR rental_rate = 4.99 );
```
