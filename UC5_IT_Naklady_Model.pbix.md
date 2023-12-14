----

[Home](../home.md) > [UC5_IT_Naklady_Model.pbix](UC5_IT_Naklady_Model.pbix.md)

[Information](#information) | [Model information](#model-information) | [Model relationships](#model-relationships) | [Report sections](#report-sections) | [Business objects](#business-objects) | [Measures](#measures) | [Relationships](#relationships) | [Hierarchies](#hierarchies) | [Columns](#columns) | 

----

# Information

Documentation for file **UC5_IT_Naklady_Model.pbix**.

# Model information


| Param  | Value  |
|---|---|
| **Analyzed pbix file name** | `UC5_IT_Naklady_Model.pbix` | 
| **Catalog name** | `10fc7aaf-87b1-4154-b3af-029030cbc5a4` | 
| **Port** | `59898`|
| **Description** | `-NaN-` | 
| **Date modified** | `2023-12-14T22:02:24` | 
| **Compatibility level** | `1567` | 


[Up](#)
# Model relationships

```mermaid
graph LR;

id780(["LocalDateTable_601d7..(51)[-NaN-]"]) --> id12(["Účty[EtlLoadTime]"])
id1375(["LocalDateTable_de5a9..(51)[-NaN-]"]) --> id15(["Strediská[EtlLoadTime]"])
id1800(["LocalDateTable_f8a05..(51)[-NaN-]"]) --> id18(["Zákazky[EtlLoadTime]"])
id2203(["LocalDateTable_da163..(51)[-NaN-]"]) --> id21(["Dátum[Date]"])
id2965(["LocalDateTable_9198a..(51)[-NaN-]"]) --> id27(["GLPCA Skutočnosť[EtlLoadTime]"])
id3463(["LocalDateTable_2b38b..(51)[-NaN-]"]) --> id30(["GLPCP Plán[EtlLoadTime]"])
id12(["Účty[DimAccountId]"]) --> id27(["GLPCA Skutočnosť[DimAccountId]"])
id12(["Účty[DimAccountId]"]) --> id30(["GLPCP Plán[DimAccountId]"])
id15(["Strediská[DimCenterId]"]) --> id27(["GLPCA Skutočnosť[DimCenterId]"])
id15(["Strediská[DimCenterId]"]) --> id30(["GLPCP Plán[DimCenterId]"])
id18(["Zákazky[DimContractId]"]) --> id27(["GLPCA Skutočnosť[DimContractId]"])
id18(["Zákazky[DimContractId]"]) --> id30(["GLPCP Plán[DimContractId]"])
id21(["Dátum[Date]"]) --> id27(["GLPCA Skutočnosť[Dátum]"])
id21(["Dátum[Date]"]) --> id30(["GLPCP Plán[Dátum]"])
```



[Up](#)

# Report sections

## Info

| Param  | Value  |
|---|---|
| **ID** | `168624009` |
| **Name** | `ReportSection` |
| **Display Name** | `Info` |
| **Filters** | `[]` |
| **Ordinal** | `` |
| **Visual containers number** | `1` |

[Up](#)



### Container 1e2eb5cb34ca8b4f4e23 

| Param  | Value  |
|---|---|
| **Name:** | `1e2eb5cb34ca8b4f4e23` |
| **Type:** | `textbox` |
| **Business objects:**  | `n/a` | 
| **Attributes:**  | n/a | 

[Up](#)






# Business objects

| ID | NAME | DESCRIPTION | 
|----|------|-------------|
| 12 | Účty | n/a |
| 15 | Strediská | n/a |
| 18 | Zákazky | n/a |
| 21 | Dátum | n/a |
| 24 | Čas | n/a |
| 27 | GLPCA Skutočnosť | n/a |
| 30 | GLPCP Plán | n/a |
| 8169 | Kalkulácia | n/a |



[Up](#)
# Measures


| ID | TABLE | NAME | DESCRIPTION | EXPRESSION | IS_HIDDEN | STATE |
|----|-------|------|-------------|------------|-----------|-------|
| 14247 | Účty |  | n/a | `
SWITCH (
    TRUE,
    LEFT ( 'Účty'[Číslo účtu], 1 ) = "5", "Náklad",
    LEFT ( 'Účty'[Číslo účtu], 1 ) = "6", "Výnos",
    "N/A"
)` | False |  1 |  
| 14690 | GLPCA Skutočnosť |  | n/a | `DATEVALUE ( "1/" & 'GLPCA Skutočnosť'[Mesiac] & "/" & 'GLPCA Skutočnosť'[Rok] )` | False |  1 |  
| 15189 | GLPCP Plán |  | n/a | `DATEVALUE ( "1/" & 'GLPCP Plán'[Mesiac] & "/" & 'GLPCP Plán'[Rok] )` | False |  1 |  
| 699 | DateTableTemplate_1b..(54) |  | n/a | `YEAR([Date])` | True |  1 |  
| 700 | DateTableTemplate_1b..(54) |  | n/a | `MONTH([Date])` | True |  1 |  
| 701 | DateTableTemplate_1b..(54) |  | n/a | `FORMAT([Date], "MMMM")` | True |  1 |  
| 702 | DateTableTemplate_1b..(54) |  | n/a | `INT(([ČMesiaca] + 2) / 3)` | True |  1 |  
| 703 | DateTableTemplate_1b..(54) |  | n/a | `"Štvrť " & [ČŠtvrťroka]` | True |  1 |  
| 704 | DateTableTemplate_1b..(54) |  | n/a | `DAY([Date])` | True |  1 |  
| 785 | LocalDateTable_601d7..(51) |  | n/a | `YEAR([Date])` | True |  1 |  
| 786 | LocalDateTable_601d7..(51) |  | n/a | `MONTH([Date])` | True |  1 |  
| 787 | LocalDateTable_601d7..(51) |  | n/a | `FORMAT([Date], "MMMM")` | True |  1 |  
| 788 | LocalDateTable_601d7..(51) |  | n/a | `INT(([ČMesiaca] + 2) / 3)` | True |  1 |  
| 789 | LocalDateTable_601d7..(51) |  | n/a | `"Štvrť " & [ČŠtvrťroka]` | True |  1 |  
| 790 | LocalDateTable_601d7..(51) |  | n/a | `DAY([Date])` | True |  1 |  
| 1380 | LocalDateTable_de5a9..(51) |  | n/a | `YEAR([Date])` | True |  1 |  
| 1381 | LocalDateTable_de5a9..(51) |  | n/a | `MONTH([Date])` | True |  1 |  
| 1382 | LocalDateTable_de5a9..(51) |  | n/a | `FORMAT([Date], "MMMM")` | True |  1 |  
| 1383 | LocalDateTable_de5a9..(51) |  | n/a | `INT(([ČMesiaca] + 2) / 3)` | True |  1 |  
| 1384 | LocalDateTable_de5a9..(51) |  | n/a | `"Štvrť " & [ČŠtvrťroka]` | True |  1 |  
| 1385 | LocalDateTable_de5a9..(51) |  | n/a | `DAY([Date])` | True |  1 |  
| 1805 | LocalDateTable_f8a05..(51) |  | n/a | `YEAR([Date])` | True |  1 |  
| 1806 | LocalDateTable_f8a05..(51) |  | n/a | `MONTH([Date])` | True |  1 |  
| 1807 | LocalDateTable_f8a05..(51) |  | n/a | `FORMAT([Date], "MMMM")` | True |  1 |  
| 1808 | LocalDateTable_f8a05..(51) |  | n/a | `INT(([ČMesiaca] + 2) / 3)` | True |  1 |  
| 1809 | LocalDateTable_f8a05..(51) |  | n/a | `"Štvrť " & [ČŠtvrťroka]` | True |  1 |  
| 1810 | LocalDateTable_f8a05..(51) |  | n/a | `DAY([Date])` | True |  1 |  
| 2208 | LocalDateTable_da163..(51) |  | n/a | `YEAR([Date])` | True |  1 |  
| 2209 | LocalDateTable_da163..(51) |  | n/a | `MONTH([Date])` | True |  1 |  
| 2210 | LocalDateTable_da163..(51) |  | n/a | `FORMAT([Date], "MMMM")` | True |  1 |  
| 2211 | LocalDateTable_da163..(51) |  | n/a | `INT(([ČMesiaca] + 2) / 3)` | True |  1 |  
| 2212 | LocalDateTable_da163..(51) |  | n/a | `"Štvrť " & [ČŠtvrťroka]` | True |  1 |  
| 2213 | LocalDateTable_da163..(51) |  | n/a | `DAY([Date])` | True |  1 |  
| 2970 | LocalDateTable_9198a..(51) |  | n/a | `YEAR([Date])` | True |  1 |  
| 2971 | LocalDateTable_9198a..(51) |  | n/a | `MONTH([Date])` | True |  1 |  
| 2972 | LocalDateTable_9198a..(51) |  | n/a | `FORMAT([Date], "MMMM")` | True |  1 |  
| 2973 | LocalDateTable_9198a..(51) |  | n/a | `INT(([ČMesiaca] + 2) / 3)` | True |  1 |  
| 2974 | LocalDateTable_9198a..(51) |  | n/a | `"Štvrť " & [ČŠtvrťroka]` | True |  1 |  
| 2975 | LocalDateTable_9198a..(51) |  | n/a | `DAY([Date])` | True |  1 |  
| 3468 | LocalDateTable_2b38b..(51) |  | n/a | `YEAR([Date])` | True |  1 |  
| 3469 | LocalDateTable_2b38b..(51) |  | n/a | `MONTH([Date])` | True |  1 |  
| 3470 | LocalDateTable_2b38b..(51) |  | n/a | `FORMAT([Date], "MMMM")` | True |  1 |  
| 3471 | LocalDateTable_2b38b..(51) |  | n/a | `INT(([ČMesiaca] + 2) / 3)` | True |  1 |  
| 3472 | LocalDateTable_2b38b..(51) |  | n/a | `"Štvrť " & [ČŠtvrťroka]` | True |  1 |  
| 3473 | LocalDateTable_2b38b..(51) |  | n/a | `DAY([Date])` | True |  1 |  


[Up](#)
# Relationships 


| ID | FROM_TABLE | TO_TABLE | FROM:TO CARDINALITY | NAME | IS_ACTIVE  |
|----|------------|----------|---------------------|------|------------|
| 783 | Účty[EtlLoadTime] | LocalDateTable_601d7..(51)[-NaN-] | 2:1 | acdc2ff4-b747-4492-8859-9384d702c64a | True |
| 1378 | Strediská[EtlLoadTime] | LocalDateTable_de5a9..(51)[-NaN-] | 2:1 | 672b9fc5-1163-4194-ab75-62d2cd168868 | True |
| 1803 | Zákazky[EtlLoadTime] | LocalDateTable_f8a05..(51)[-NaN-] | 2:1 | c115dfbe-a6c7-4e57-aebd-bbc11b49b6d1 | True |
| 2206 | Dátum[Date] | LocalDateTable_da163..(51)[-NaN-] | 2:1 | 71ad4d58-3914-486b-bc14-b632cd7ec09d | True |
| 2968 | GLPCA Skutočnosť[EtlLoadTime] | LocalDateTable_9198a..(51)[-NaN-] | 2:1 | 95168930-5c7a-4fda-ab42-f2fd9b4261d5 | True |
| 3466 | GLPCP Plán[EtlLoadTime] | LocalDateTable_2b38b..(51)[-NaN-] | 2:1 | 11a09650-a371-4998-91ec-58e61ef2dec3 | True |
| 7982 | GLPCA Skutočnosť[DimAccountId] | Účty[DimAccountId] | 2:1 | c09263aa-f69f-4502-973b-0754342d9d6f | True |
| 7999 | GLPCP Plán[DimAccountId] | Účty[DimAccountId] | 2:1 | 8222ce8b-9b9d-427e-9228-33c0e9e6fba4 | True |
| 8016 | GLPCA Skutočnosť[DimCenterId] | Strediská[DimCenterId] | 2:1 | 52da7bce-7199-4346-ab6d-bb10e203eafb | True |
| 8033 | GLPCP Plán[DimCenterId] | Strediská[DimCenterId] | 2:1 | 4eff9349-fe74-4c46-ab28-6e529adf7c6b | True |
| 8050 | GLPCA Skutočnosť[DimContractId] | Zákazky[DimContractId] | 2:1 | b5f72491-c8b9-44b3-b8f1-dd96be76a309 | True |
| 8067 | GLPCP Plán[DimContractId] | Zákazky[DimContractId] | 2:1 | 4761789d-34ca-4d70-a15a-76239bf28f41 | True |
| 15555 | GLPCA Skutočnosť[Dátum] | Dátum[Date] | 2:1 | 8ef49162-4aa2-4cbf-aa16-fd7b3c6fbf3e | True |
| 15572 | GLPCP Plán[Dátum] | Dátum[Date] | 2:1 | ce9fc0ce-8816-4d2c-930e-bcb97dabc93e | True |


[Up](#)
# Hierarchies 



| ID | TABLE | NAME | DESCRIPTION  | IS_HIDDEN | 
|----|----------|------|--------------|-----------|
| 706 |DateTableTemplate_1b..(54) | Hierarchia dátumov | n/a | False | 
| 792 |LocalDateTable_601d7..(51) | Hierarchia dátumov | n/a | False | 
| 1387 |LocalDateTable_de5a9..(51) | Hierarchia dátumov | n/a | False | 
| 1812 |LocalDateTable_f8a05..(51) | Hierarchia dátumov | n/a | False | 
| 2215 |LocalDateTable_da163..(51) | Hierarchia dátumov | n/a | False | 
| 2977 |LocalDateTable_9198a..(51) | Hierarchia dátumov | n/a | False | 
| 3475 |LocalDateTable_2b38b..(51) | Hierarchia dátumov | n/a | False | 


[Up](#)
# Columns 


| ID | TABLE | EXPLICIT_NAME | DESCRIPTION | IS_HIDDEN | EXPRESSION |
|----|-------|---------------|-------------|-----------|------------|
| 34 | Účty | Číslo účtu | n/a | False | n/a |
| 35 | Účty | Názov účtu | n/a | False | n/a |
| 36 | Účty | Hierarchia | n/a | False | n/a |
| 14247 | Účty | Trieda účtu | n/a | False | 
SWITCH (
    TRUE,
    LEFT ( 'Účty'[Číslo účtu], 1 ) = "5", "Náklad",
    LEFT ( 'Účty'[Číslo účtu], 1 ) = "6", "Výnos",
    "N/A"
) |
| 40 | Strediská | Číslo strediska | n/a | False | n/a |
| 41 | Strediská | Stredisko | n/a | False | n/a |
| 42 | Strediská | Hierarchia | n/a | False | n/a |
| 46 | Zákazky | Zákazka | n/a | False | n/a |
| 47 | Zákazky | Názov | n/a | False | n/a |
| 50 | Dátum | Date | n/a | False | n/a |
| 51 | Dátum | DimDateId | n/a | False | n/a |
| 52 | Dátum | Rok | n/a | False | n/a |
| 53 | Dátum | MonthId | n/a | False | n/a |
| 54 | Dátum | MonthYear | n/a | False | n/a |
| 55 | Dátum | MonthNameYear | n/a | False | n/a |
| 56 | Dátum | Číslo mesiaca | n/a | False | n/a |
| 57 | Dátum | Month | n/a | False | n/a |
| 58 | Dátum | MonthShort | n/a | False | n/a |
| 59 | Dátum | Day | n/a | False | n/a |
| 60 | Dátum | DayOfWeekName | n/a | False | n/a |
| 61 | Dátum | DayOfWeekNameShort | n/a | False | n/a |
| 62 | Dátum | DayOfWeek | n/a | False | n/a |
| 63 | Dátum | Quarter | n/a | False | n/a |
| 64 | Dátum | YearQuarter | n/a | False | n/a |
| 65 | Dátum | IsoWeek | n/a | False | n/a |
| 66 | Dátum | IsoWeekBusiness | n/a | False | n/a |
| 67 | Čas | DimTimeId | n/a | False | n/a |
| 68 | Čas | hours | n/a | False | n/a |
| 69 | Čas | minutes | n/a | False | n/a |
| 70 | Čas | seconds | n/a | False | n/a |
| 74 | GLPCA Skutočnosť | Mesiac | n/a | False | n/a |
| 75 | GLPCA Skutočnosť | Rok | n/a | False | n/a |
| 76 | GLPCA Skutočnosť | Suma | n/a | False | n/a |
| 77 | GLPCA Skutočnosť | Mena | n/a | False | n/a |
| 14690 | GLPCA Skutočnosť | Dátum | n/a | False | DATEVALUE ( "1/" & 'GLPCA Skutočnosť'[Mesiac] & "/" & 'GLPCA Skutočnosť'[Rok] ) |
| 83 | GLPCP Plán | Mesiac | n/a | False | n/a |
| 84 | GLPCP Plán | Rok | n/a | False | n/a |
| 85 | GLPCP Plán | Suma | n/a | False | n/a |
| 86 | GLPCP Plán | Mena | n/a | False | n/a |
| 15189 | GLPCP Plán | Dátum | n/a | False | DATEVALUE ( "1/" & 'GLPCP Plán'[Mesiac] & "/" & 'GLPCP Plán'[Rok] ) |



----
<p align="center">
Generated at 14.12.2023 23:29:19 by <a href='https://github.com/dop12/pbix_doc'>PBIX DOC PROJECT</a> Git version: 46272be
</p>