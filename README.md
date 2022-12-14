# Excel Test

## Preparation 
Before starting, you will need: 
- Git - Github/Bitbucket/Gitlab account 
- Your own dev set up 

Please use following technologies: 
- Laravel

Create an api to validate excel file format and its data. For this test, you will have to validate two type of excel file `Type_A` and `Type_B`.

## General Rules

1. Column name that starts with `#` should not contain any space
2. Column name that ends with `*` is a required column, means it must have a value
3. For each file type, it should validate the header columns name and the amount of columns it has
    - For example, `Type_A`  file should only contains 5 columns and the header column name should be and follows the following order;
      1. Field_A* 
      2. #Field_B 
      3. Field_C 
      4. Field_D* 
      5. Field_E*
4. The package should be able to validate both `.xls` and `.xlsx` file
5. You may use third party library to parse the excel file

Two sample file is provided namely `Type_A.xlsx` and `Type_B.xlsx`

Sample Output when validating `Type_A.xlsx`

| Row | Error |
| --- | --- |
| 3 | Missing value in Field_A, Field_B should not contain any space, Missing value in Field_D |
| 4 | Missing value in Field_A,Missing value in Field_E |

Sample Output when validating `Type_B.xlsx`

| Row | Error |
| --- | --- |
| 3 | Missing value in Field_A, Field_B should not contain any space |

## Bonus

It will be nice if new file type(`Type_C`) can be integrated by just adding `Type_C.js`

## Coding Recommendation

1. Follow DRY principle
2. Write simple but meaningful code
3. Incorporate design patterns in your code

### Enjoy your test!
