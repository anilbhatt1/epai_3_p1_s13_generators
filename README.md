# Generators

## Assignment
- Assignment is as below.
- **Goal 1** 
    - Create a lazy iterator that will return a named tuple of the data in each row. 
    - The data types should be appropriate - i.e. if the column is a date, you should be storing dates in the named tuple, if the field is an integer, then it should be stored as an integer, etc.
- **Goal 2** 
    - Calculate the number of violations by car make.
- Note: Try to use lazy evaluation as much as possible - it may not always be possible though! That's OK, as long as it's kept to a minimum.

## Assignment Solution

- File that holds required functions: Generators_Assignment.py
- Github Location : https://github.com/anilbhatt1/epai_3_p1_s13_generators/blob/master/Generators_Assignment.py
- Following functions are implemented:
- **cast(type_, data)**
    - This will cast the 'data' based on data-type passed via 'type_'
- **cast_row(data_type, data_row)**
    - Calls 'cast' as a list comprehension from 'car_tickets' function
- **car_tickets(file_path)**
    - Accepts file_path that holds 'nyc_parking_tickets_extract-1.csv' file.
    - It then returns a generator that can cast and yield records one by one from csv file.
- **ctr_dict(vehicle_make)**
    - This is a counter
    - This will update a dictionary 'ticket_dict' that holds the violations per car make.

- Draft Jupyter version where assignment was initially tried out can be found below:
https://github.com/anilbhatt1/epai_3_p1_s13_generators/blob/master/Generators_Assignment_Draft.ipynb

## Testing
- All the above functions are tested using pytest.
- Testcase file : **test_Generators_Assignment.py** (Please note that that 'test_' need to be prefixed for Pytest to automatically identify that it is a testcase file).
- Github Location : https://github.com/anilbhatt1/epai_3_p1_s13_generators/blob/master/test_Generators_Assignment.py
- Test snapshot results as below:
![Test_Pass](https://github.com/anilbhatt1/epai_3_p1_s13_generators/blob/master/Test_Passed_Snapshot.png)
