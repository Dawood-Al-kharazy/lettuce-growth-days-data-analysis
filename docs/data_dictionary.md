# **Data Dictionary: Lettuce Growth Days Dataset**

## **Overview**

This document defines the variables (columns) present in the lettuce\_dataset\_updated.csv file. It serves as the single source of truth for the data types, units of measurement, and descriptions of each feature to ensure accurate analysis.

## **Dataset Structure**

| Column Name | Data Type | Unit / Format | Description | Example Value |
| :---- | :---- | :---- | :---- | :---- |
| **Plant\_ID** | Integer | Numeric | A unique identifier assigned to an individual lettuce plant or batch. | 1, 70 |
| **Date** | Date String | MM/DD/YYYY | The specific date the measurements were recorded. | 8/3/2023 |
| **Temperature (°C)** | Float | Celsius (°C) | The ambient temperature of the growing environment measured in Celsius. | 33.4, 19.9 |
| **Humidity (%)** | Integer/Float | Percentage (1-100) | The relative humidity of the growing environment expressed as a whole number. | 53, 77 |
| **TDS Value (ppm)** | Integer | ppm (Parts Per Million) | Total Dissolved Solids in the water/nutrient solution. Indicates nutrient concentration. | 582, 479 |
| **pH Level** | Float | pH Scale (0-14) | The acidity or alkalinity of the water/nutrient solution. | 6.4, 6.1 |
| **Growth Days** | Integer | Days | The number of days the plant has been growing since planting/germination. | 1, 14 |

## **⚠️ Analyst Notes & Derived Columns**

*Note: The following columns are included in the raw dataset but are mathematical derivations of other primary columns. They should be used cautiously to avoid multicollinearity in predictive models.*

| Column Name | Data Type | Derivation Source | Description |
| :---- | :---- | :---- | :---- |
| **Temperature (F)** | Float | Temperature (°C) | The ambient temperature converted to Fahrenheit. Formula: (°C \* 9/5) \+ 32. |
| **Humidity** | Float | Humidity (%) | The relative humidity expressed as a decimal rather than a whole number. Formula: Humidity (%) / 100. |

