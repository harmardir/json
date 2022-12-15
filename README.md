# json
Python codes to process json data

https://www.geeksforgeeks.org/convert-nested-json-to-csv-in-python/


# Approach

- The first step is to read the JSON file as a python dict object. This will help us to make use of python dict methods to perform some operations. The read_json() function is used for the task, which taken the file path along with the extension as a parameter and returns the contents of the JSON file as a python dict object.
- We have iterated for each JSON object present in the details array. In each iteration we first normalized the JSON and created a temporary dataframe. This dataframe was then appended to the output dataframe.
- Once done, the column name was renamed for better visibility. If we see the console output, the “major” column was named as “education.graduation.major” before renaming. This is because the “json_normalize()” method uses the keys in the complete nest for generating the column name to avoid duplicate column issue. So, “education” is the first level, “graduation” is second and “major” is third level in the JSON nesting. Therefore, the column “education.graduation.major” was simply renamed to “graduation”.
- After renaming the columns, the to_csv() method saves the pandas dataframe object as CSV to the provided file location.
