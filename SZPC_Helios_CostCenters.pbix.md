----

[Home](../home.md) > [SZPC_Helios_CostCenters.pbix](SZPC_Helios_CostCenters.pbix.md)

[Information](#information) | [Model information](#model-information) | [Model relationships](#model-relationships) | [Report sections](#report-sections) | [Business objects](#business-objects) | [Measures](#measures) | [Relationships](#relationships) | [Hierarchies](#hierarchies) | [Columns](#columns) | 

----

# Information

Documentation for file **SZPC_Helios_CostCenters.pbix**.

# Model information


| Param  | Value  |
|---|---|
| **Analyzed pbix file name** | `SZPC_Helios_CostCenters.pbix` | 
| **Catalog name** | `75199ab0-acc0-4584-aa76-de91c0758ee6` | 
| **Port** | `54816`|
| **Description** | `-NaN-` | 
| **Date modified** | `2023-11-30T16:03:44` | 
| **Compatibility level** | `1551` | 


[Up](#)
# Model relationships

```mermaid
graph LR;

id15(["vDimDatasource[DataSourceId]"]) --> id17(["vDimCenter[DataSourceId]"])
```



[Up](#)

# Report sections

## CostCenters

| Param  | Value  |
|---|---|
| **ID** | `405890500` |
| **Name** | `ReportSection` |
| **Display Name** | `CostCenters` |
| **Filters** | `[]` |
| **Ordinal** | `` |
| **Visual containers number** | `10` |

[Up](#)



### Container f7154c99568e683d92e8 

| Param  | Value  |
|---|---|
| **Name:** | `f7154c99568e683d92e8` |
| **Type:** | `card` |
| **Business objects:**  | `vDimCenter` | 
| **Attributes:**  | Aggregation: Min(vDimCenter.TECH_LOAD_DATE) | 

[Up](#)




### Container 31e024908e218d0998d0 

| Param  | Value  |
|---|---|
| **Name:** | `31e024908e218d0998d0` |
| **Type:** | `textbox` |
| **Business objects:**  | `n/a` | 
| **Attributes:**  | n/a | 

[Up](#)




### Container e10cb8ee180ad006e9082 

| Param  | Value  |
|---|---|
| **Name:** | `e10cb8ee180ad006e9082` |
| **Type:** | `textbox` |
| **Business objects:**  | `n/a` | 
| **Attributes:**  | n/a | 

[Up](#)




### Container c63e5e88967542e3d007 

| Param  | Value  |
|---|---|
| **Name:** | `c63e5e88967542e3d007` |
| **Type:** | `slicer` |
| **Business objects:**  | `vDimDatasource` | 
| **Attributes:**  | Column: vDimDatasource.Company | 

[Up](#)




### Container 2ca6c150071753011194 

| Param  | Value  |
|---|---|
| **Name:** | `2ca6c150071753011194` |
| **Type:** | `tableEx` |
| **Business objects:**  | `vDimCenter, vDimDatasource` | 
| **Attributes:**  | Column: vDimCenter.Alias<br/> Column: vDimCenter.AliasNumber<br/> Column: vDimCenter.Code<br/> Column: CountNonNull(vDimCenter.CenterTypeCode)<br/> Column: vDimCenter.CenterTypeName<br/> Column: vDimCenter.Name<br/> Column: vDimCenter.NameLevel01<br/> Column: vDimCenter.NameLevel02<br/> Column: vDimCenter.NameLevel03<br/> Column: vDimCenter.NameLevel04<br/> Column: vDimCenter.NameLevel05<br/> Column: vDimCenter.CodeLevel01<br/> Column: vDimCenter.CodeLevel02<br/> Column: vDimCenter.CodeLevel03<br/> Column: vDimCenter.CodeLevel04<br/> Column: vDimCenter.CodeLevel05<br/> Column: vDimCenter.DataSourceId<br/> Column: Sum(vDimCenter.DescLevel01)<br/> Column: Sum(vDimCenter.DescLevel02)<br/> Column: Sum(vDimCenter.DescLevel03)<br/> Column: Sum(vDimCenter.DescLevel04)<br/> Column: Sum(vDimCenter.DescLevel05)<br/> Column: Sum(vDimCenter.Description)<br/> Column: vDimDatasource.Company<br/> Column: vDimDatasource.SourceDbName | 

[Up](#)




### Container 88aaf3581616676de492 

| Param  | Value  |
|---|---|
| **Name:** | `88aaf3581616676de492` |
| **Type:** | `slicer` |
| **Business objects:**  | `vDimCenter` | 
| **Attributes:**  | Column: vDimCenter.Code | 

[Up](#)




### Container 60fe21330ec8e86b4d0e 

| Param  | Value  |
|---|---|
| **Name:** | `60fe21330ec8e86b4d0e` |
| **Type:** | `slicer` |
| **Business objects:**  | `vDimCenter` | 
| **Attributes:**  | Column: vDimCenter.Name | 

[Up](#)




### Container cfc0660647974ceb3010 

| Param  | Value  |
|---|---|
| **Name:** | `cfc0660647974ceb3010` |
| **Type:** | `slicer` |
| **Business objects:**  | `vDimCenter` | 
| **Attributes:**  | Column: vDimCenter.AliasNumber | 

[Up](#)




### Container efbfa8a7afc81cf00959 

| Param  | Value  |
|---|---|
| **Name:** | `efbfa8a7afc81cf00959` |
| **Type:** | `slicer` |
| **Business objects:**  | `vDimCenter` | 
| **Attributes:**  | Column: vDimCenter.Alias | 

[Up](#)






# Business objects

| ID | NAME | DESCRIPTION | 
|----|------|-------------|
| 14 | vDimDatasource | n/a |
| 17 | vDimCenter | n/a |



[Up](#)
# Measures


| ID | TABLE | NAME | DESCRIPTION | EXPRESSION | IS_HIDDEN | STATE |
|----|-------|------|-------------|------------|-----------|-------|


[Up](#)
# Relationships 


| ID | FROM_TABLE | TO_TABLE | FROM:TO CARDINALITY | NAME | IS_ACTIVE  |
|----|------------|----------|---------------------|------|------------|
| 1222 | vDimCenter[DataSourceId] | vDimDatasource[DataSourceId] | 2:1 | d9b6c365-73fe-4f82-9803-552ec3691052 | True |


[Up](#)
# Hierarchies 


There are no hierarchies information or we have insufficient permissions.


[Up](#)
# Columns 


| ID | TABLE | EXPLICIT_NAME | DESCRIPTION | IS_HIDDEN | EXPRESSION |
|----|-------|---------------|-------------|-----------|------------|
| 20 | vDimDatasource | Company | n/a | False | n/a |
| 21 | vDimDatasource | DataSourceId | n/a | False | n/a |
| 22 | vDimDatasource | Location | n/a | False | n/a |
| 23 | vDimDatasource | Name | n/a | False | n/a |
| 24 | vDimDatasource | Provider | n/a | False | n/a |
| 25 | vDimDatasource | SourceDbName | n/a | False | n/a |
| 26 | vDimDatasource | SparkDBName | n/a | False | n/a |
| 236414 | vDimDatasource | TECH_LOAD_DATE | n/a | False | n/a |
| 236422 | vDimDatasource | TECH_DATA_SOURCE_ID | n/a | False | n/a |
| 27 | vDimCenter | DimCenterId | n/a | False | n/a |
| 28 | vDimCenter | Alias | n/a | False | n/a |
| 29 | vDimCenter | AliasNumber | n/a | False | n/a |
| 30 | vDimCenter | CenterBk | n/a | False | n/a |
| 31 | vDimCenter | CenterTypeCode | n/a | False | n/a |
| 32 | vDimCenter | CenterTypeName | n/a | False | n/a |
| 33 | vDimCenter | Code | n/a | False | n/a |
| 34 | vDimCenter | CodeLevel01 | n/a | False | n/a |
| 35 | vDimCenter | CodeLevel02 | n/a | False | n/a |
| 36 | vDimCenter | CodeLevel03 | n/a | False | n/a |
| 37 | vDimCenter | CodeLevel04 | n/a | False | n/a |
| 38 | vDimCenter | CodeLevel05 | n/a | False | n/a |
| 39 | vDimCenter | DataSourceId | n/a | False | n/a |
| 40 | vDimCenter | DescLevel01 | n/a | False | n/a |
| 41 | vDimCenter | DescLevel02 | n/a | False | n/a |
| 42 | vDimCenter | DescLevel03 | n/a | False | n/a |
| 43 | vDimCenter | DescLevel04 | n/a | False | n/a |
| 44 | vDimCenter | DescLevel05 | n/a | False | n/a |
| 45 | vDimCenter | Description | n/a | False | n/a |
| 46 | vDimCenter | Name | n/a | False | n/a |
| 47 | vDimCenter | NameLevel01 | n/a | False | n/a |
| 48 | vDimCenter | NameLevel02 | n/a | False | n/a |
| 49 | vDimCenter | NameLevel03 | n/a | False | n/a |
| 50 | vDimCenter | NameLevel04 | n/a | False | n/a |
| 51 | vDimCenter | NameLevel05 | n/a | False | n/a |
| 236430 | vDimCenter | TECH_LOAD_DATE | n/a | False | n/a |
| 236438 | vDimCenter | TECH_DATA_SOURCE_ID | n/a | False | n/a |



----
<p align="center">
Generated at 01.12.2023 14:55:29 by <a href='https://github.com/dop12/pbix_doc'>PBIX DOC PROJECT</a> Git version: 31b4c38
</p>