## Question-11

 - Show the total number of admissions

## Solution

```
SELECT COUNT(*) AS total_admissions
FROM admissions;

```
## Question-12

 - Show all the columns from admissions where the patient was admitted and discharged on the same day.

## Solution

```
SELECT *
FROM admissions
WHERE admission_date = discharge_date;

```

## Question-13

 - Show the patient id and the total number of admissions for patient_id 579.

## Solution

```
SELECT
  patient_id,
  COUNT(*) AS total_admissions
FROM admissions
WHERE patient_id = 579;

```

## Question-14

 - Show the patient id and the total number of admissions for patient_id 579.

## Solution

```
SELECT
  patient_id,
  COUNT(*) AS total_admissions
FROM admissions
WHERE patient_id = 579;

```

## Question-15

 - Based on the cities that our patients live in, show unique cities that are in province_id 'NS'.

## Solution

```
SELECT DISTINCT(city) AS unique_cities
FROM patients
WHERE province_id = 'NS';

```


## Question-16

 - Write a query to find the first_name, last name and birth date of patients who has height greater than 160 and weight greater than 70

## Solution

```
select first_name,last_name,birth_date
from patients
where height > 160 and weight > 70

```

## Question-17

 - Write a query to find list of patients first_name, last_name, and allergies where allergies are not null and are from the city of 'Hamilton'

## Solution

```
SELECT
  first_name,
  last_name,
  allergies
FROM patients
WHERE
  city = 'Hamilton'
  and allergies is not null

```
