# Easy SQL problems

## Question-1

 - Show first name, last name, and gender of patients whose gender is 'M'

## Solution

```
Select first_name,last_name,gender
FROM patients
Where gender = 'M'
```

## Question-2

 - Show first name and last name of patients who does not have allergies. (null)

## Solution

```
select first_name,last_name
FROM patients
where allergies is null
```


## Question-3

 - Show first name of patients that start with the letter 'C'

## Solution

```
select first_name
FROM patients
where first_name like 'c%'
```

## Question-4

 - Show first name and last name of patients that weight within the range of 100 to 120 (inclusive)

## Solution

```
select first_name,last_name
FROM patients
where weight between 100 and 120
```

## Question-5

 - Update the patients table for the allergies column. If the patient's allergies is null then replace it with 'NKA'

## Solution

```
UPDATE patients
SET allergies = 'NKA'
WHERE allergies IS NULL;
```

## Question-6

 - Show first name and last name concatinated into one column to show their full name.

## Solution

```
select concat(first_name,' ',last_name) AS full_name
FROM patients

```
