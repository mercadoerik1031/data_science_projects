# Project 1: World Development Statistics

# Background

The global population has experienced a colossal expansion over the last century, multiplying several folds in number. This growth is a testament to various factors, including advancements in medical science, increased agricultural productivity, and overall improvements in living standards. The burgeoning population has diverse implications for economies and societies worldwide. A larger population can signify a more substantial workforce, driving economic growth and innovation. However, if this growth outpaces the availability of resources or job opportunities, it could result in challenges such as unemployment, resource depletion, and infrastructural strain. Understanding these dynamics is crucial for policy-makers and stakeholders, as they navigate the delicate balance between fostering population growth and ensuring sustainable development to maintain economic vitality and quality of life across the globe.

# Problem Statement
This study delves into a century's worth of global demographic shifts, life expectancy, and economic changes, aiming to unravel:
- The dynamics of population growth from 1924 to 2024.
- The interplay between life expectancy and population numbers.
- The tripartite relationship among life expectancy, population, and Gross National Income (GNI).
- The performance of countries regarding GNI and life expectancy.

# Data Dictionary

### Population by Country (`population.csv`)
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| country | String | The name of the country. |
| 1800 - 2100 | String | Population estimates from the year 1800 to 2100. Values are in a compact format with 'k' representing thousands (e.g., '10k' for 10,000) and 'M' for millions (e.g., '1M' for 1,000,000). |

### Life Expectancy by Country (`life_expectancy.csv`)
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| country | String | The name of the country. |
| 1800 - 2100 | Float | Life expectancy at birth from the year 1800 to 2100, measured in years. |

### Gross National Income (GNI) per Capita in Current US Dollars (`gni_per_cap_atlas_method_con2021.csv`)
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| country | String | The name of the country. |
| 1800 - 2050 | String | GNI per capita from the year 1800 to 2050, expressed in current US dollars. Values are in a compact format with 'k' representing thousands (e.g., '10k' for 10,000) and simple numerical values for amounts below $1,000. |

### Merged Data (`merged_data.csv`)
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| country | String | The name of the country. |
| continent | String | The continent on which the country is located. |
| 1924_gni - 2024_gni | Float | Gross National Income (GNI) per capita from 1924 to 2024 in current US dollars. |
| 1924_life_expectancy - 2024_life_expectancy | Float | Life expectancy at birth from 1924 to 2024, measured in years. (Assuming its presence based on initial request) |
| 1924_population - 2024_population | Float | Population numbers from 1924 to 2024. Values are absolute and represent the total population. |



# Executive Summary

### Key Findings
- Population has quintupled globally from 1924 to 2024.
- Life expectancy has risen significantly despite population growth.
- Higher GNI correlates with greater life expectancy.
- Economic growth and health improvements are unevenly distributed worldwide.

### Conclusions and Recommendations
The study underscores the need for sustainable and inclusive development policies. The findings advocate for balanced economic growth, enhanced healthcare systems, and focused developmental aid to ensure improved quality of life across different regions.

### Next Steps
Further research could explore:
- The impact of technological advancements on economic and health indicators.
- Longitudinal studies on the quality of life in rapidly growing economies.
- Policy effectiveness in bridging the health and economic divide between nations.

**For inquiries or further information, please feel free to reach out.**