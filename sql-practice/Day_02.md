## Question-7

 - Show first name, last name, and the full province name of each patient.

Example: 'Ontario' instead of 'ON'

## Solution

```
SELECT p.first_name,p.last_name,pn.province_name
FROM patients p 
inner join province_names pn
on p.province_id = pn.province_id

```

## Question-8

 - Show how many patients have a birth_date with 2010 as the birth year.

## Solution

```
SELECT COUNT(*) AS total_patients
FROM patients
WHERE YEAR(birth_date) = 2010;

```

## Question-9

 - Show the first_name, last_name, and height of the patient with the greatest height.

## Solution

```
SELECT
  first_name,
  last_name,
  height
FROM patients
WHERE height = (
    SELECT max(height)
    FROM patients
  )

```

## Question-10

 - Show all columns for patients who have one of the following patient_ids:
1,45,534,879,1000

## Solution

```
SELECT *
FROM patients
WHERE
  patient_id IN (1, 45, 534, 879, 1000);

```
