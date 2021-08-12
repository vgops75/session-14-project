# Project -- Building generators on data from multiple separate files yielding data in the namedtuples format

Description:

Given 4 files containing information about persons.

The files are:
* `personal_info.csv` -   personal information such as name, gender, etc. (one row per person)
* `vehicles.csv` -   what vehicle people own (one row per person)
* `employment.csv` -   where a person is employed (one row per person)
* `update_status.csv` -   when the person's data was created and last updated

Each file contains a key, `SSN`, which **uniquely** identifies a person.

This key is present in **all** four files.

You are guaranteed that the same SSN value is present in **every** file, and that it only appears **once per file**.

In addition, the files are all sorted by SSN, i.e. the SSN values appear in the same order in each file.

#### Goal 1: Build generators for each of the datasets (assuming data is aligned across all the 4 files with respect to the field variable 'ssn')

#### Goal 2: Create a single iterable that combines all the columns from all the iterators.

#### Goal 3: Identify any stale records, where stale simply means the record has not been updated since 3/1/2017 (e.g. last update date < 3/1/2017). Create an iterator that only contains current records (i.e. not stale) based on the last_updated field from the status_update file.

#### Goal 4: Find the largest group of car makes for each gender.
