# Patika.dev.sql

## Ödev 1

#### 1.Film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.
```
--1.1 Soru
SELECT title, description
FROM film;
```

#### 2.Film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.
```
--1.2 Soru
SELECT *
FROM film
WHERE length > 60 AND length < 75;
```

#### 3.Film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.
```
--1.3 Soru
SELECT *
FROM film
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);
```

#### 4.Customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?
```
--1.4 Soru(Smith)
SELECT last_name
FROM customer
WHERE first_name = 'Mary'
```

#### 5.Film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.
```
--1.5 Soru
SELECT *
FROM film
WHERE NOT (length > 50 OR rental_rate = 2.99 OR rental_rate = 4.99 );
```

## Ödev 2

#### 1.Film tablosunda bulunan tüm sütunlardaki verileri replacement cost değeri 12.99 dan büyük eşit ve 16.99 küçük olma koşuluyla
```
--2.1 Soru
SELECT * 
FROM film 
WHERE replacement_cost Between 12.99 AND 16.99;
```

#### 2. Actor tablosunda bulunan first_name ve last_name sütunlardaki verileri first_name 'Penelope' veya 'Nick' veya 'Ed' değerleri olması
```
--2.2 Soru
SELECT first_name, last_name
FROM actor 
WHERE first_name IN('Penelope', 'Ed', 'Nick');
```

#### 3. film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99, 2.99, 4.99 VE replacement_cost 12.99, 15.99, 28.99 olma koşullarıyla sıralayınız.
```
--2.3 Soru
SELECT *
FROM film
WHERE (rental_rate IN(0.99,2.99,4.99)) AND (replacement_cost IN(12.99,15.99,28.99))
```

## Ödev 3

#### 1.Country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.
```
--3.1 Soru
SELECT country
FROM country
WHERE country LIKE 'A%a';
```
#### 2.Country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.
```
--3.2 Soru
SELECT country
FROM country
WHERE country LIKE '%_____n';
```
#### 3.Film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren
```
--3.3 Soru
SELECT  title
FROM film
WHERE title ILIKE '%T%T%T%T%';
```
#### 4.Film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız.
```
--3.4 Soru
SELECT *
FROM film
WHERE title ILIKE 'C%' AND length > 90 AND rental_rate = 2.99;
```


