# Sales & Profitability Analysis - Results Summary

- Raw file: **10,800** rows = **9,994** order lines + **4** managers + **800** return records

## Data cleaning

- Missing postal codes: **11** (all Burlington, Vermont, filled with 05401)
- Other missing values: **0**
- Duplicate order lines removed: **1** (leaves **9,993** order lines)
- Orders shipped before they were placed: **0**
- Return records: **800**, unique returned orders: **296** (some orders had several returned products)
- Date range: **03 Jan 2015** to **30 Dec 2018**

## SQL findings

**Kpis**

|   total_sales |   total_profit |   profit_margin_pct |   orders |   customers |   avg_order_value |
|--------------:|---------------:|--------------------:|---------:|------------:|------------------:|
|       2296919 |         286409 |                12.5 |     5009 |         793 |               459 |

**Yearly Growth**

|   year |   sales |   profit |   margin_pct | sales_growth_pct   |
|-------:|--------:|---------:|-------------:|:-------------------|
|   2015 |  483966 |    49556 |         10.2 | -                  |
|   2016 |  470533 |    61619 |         13.1 | -2.8               |
|   2017 |  609206 |    81795 |         13.4 | 29.5               |
|   2018 |  733215 |    93439 |         12.7 | 20.4               |

**Category Performance**

| category        |   sales |   profit |   margin_pct |
|:----------------|--------:|---------:|-------------:|
| Technology      |  836154 |   145455 |         17.4 |
| Office Supplies |  719047 |   122491 |         17   |
| Furniture       |  741718 |    18463 |          2.5 |

**Loss Making Subcategories**

| sub_category   |   sales |   profit |   margin_pct |
|:---------------|--------:|---------:|-------------:|
| Tables         |  206966 |   -17725 |         -8.6 |
| Bookcases      |  114880 |    -3473 |         -3   |
| Supplies       |   46674 |    -1189 |         -2.5 |

**Subcategory Profit**

| sub_category   |   sales |   profit |   margin_pct |
|:---------------|--------:|---------:|-------------:|
| Copiers        |  149528 |    55618 |         37.2 |
| Phones         |  330007 |    44516 |         13.5 |
| Accessories    |  167380 |    41937 |         25.1 |
| Paper          |   78479 |    34054 |         43.4 |
| Binders        |  203413 |    30222 |         14.9 |
| Chairs         |  328168 |    26602 |          8.1 |
| Storage        |  223844 |    21279 |          9.5 |
| Appliances     |  107532 |    18138 |         16.9 |
| Furnishings    |   91705 |    13059 |         14.2 |
| Envelopes      |   16476 |     6964 |         42.3 |
| Art            |   27119 |     6528 |         24.1 |
| Labels         |   12486 |     5546 |         44.4 |
| Machines       |  189239 |     3385 |          1.8 |
| Fasteners      |    3024 |      950 |         31.4 |
| Supplies       |   46674 |    -1189 |         -2.5 |
| Bookcases      |  114880 |    -3473 |         -3   |
| Tables         |  206966 |   -17725 |         -8.6 |

**Discount Impact**

| discount_band   |   order_lines |   sales |   profit |   margin_pct |
|:----------------|--------------:|--------:|---------:|-------------:|
| 1) No discount  |          4798 | 1087908 |   320988 |         29.5 |
| 2) 1-20%        |          3803 |  846522 |   100785 |         11.9 |
| 3) 21-40%       |           459 |  233857 |   -35805 |        -15.3 |
| 4) Over 40%     |           933 |  128632 |   -99559 |        -77.4 |

**Region And Manager**

| manager           | region   |   sales |   profit |   margin_pct |
|:------------------|:---------|--------:|---------:|-------------:|
| Anna Andreadi     | West     |  725458 |   108418 |         14.9 |
| Chuck Magee       | East     |  678500 |    91535 |         13.5 |
| Cassandra Brandow | South    |  391722 |    46749 |         11.9 |
| Kelly Williams    | Central  |  501240 |    39706 |          7.9 |

**Return Rate By Category**

| category        |   orders |   returned_orders |   return_rate_pct |
|:----------------|---------:|------------------:|------------------:|
| Technology      |     1544 |               123 |               8   |
| Furniture       |     1764 |               136 |               7.7 |
| Office Supplies |     3742 |               234 |               6.3 |

**Discount By Region**

| region   |   avg_discount_pct |   pct_lines_over_20pct_discount |   margin_pct |
|:---------|-------------------:|--------------------------------:|-------------:|
| Central  |               24   |                            27.7 |          7.9 |
| South    |               14.7 |                            10.6 |         11.9 |
| East     |               14.5 |                            16.2 |         13.5 |
| West     |               10.9 |                             3.7 |         14.9 |

**Worst States By Profit**

| state          |   sales |   profit |   margin_pct |
|:---------------|--------:|---------:|-------------:|
| Texas          |  170188 |   -25729 |        -15.1 |
| Ohio           |   77977 |   -16959 |        -21.7 |
| Pennsylvania   |  116512 |   -15560 |        -13.4 |
| Illinois       |   80166 |   -12608 |        -15.7 |
| North Carolina |   55603 |    -7491 |        -13.5 |

**Top States By Sales**

| state        |   sales |   profit |   margin_pct |
|:-------------|--------:|---------:|-------------:|
| California   |  457688 |    76381 |         16.7 |
| New York     |  310876 |    74039 |         23.8 |
| Texas        |  170188 |   -25729 |        -15.1 |
| Washington   |  138641 |    33403 |         24.1 |
| Pennsylvania |  116512 |   -15560 |        -13.4 |

**Worst Products**

| product_name                                             |   sales |   profit |
|:---------------------------------------------------------|--------:|---------:|
| Cubify CubeX 3D Printer Double Head Print                |   11100 |    -8880 |
| Lexmark MX611dhe Monochrome Laser Printer                |   16830 |    -4590 |
| Cubify CubeX 3D Printer Triple Head Print                |    8000 |    -3840 |
| Chromcraft Bull-Nose Wood Oval Conference Tables & Bases |    9918 |    -2876 |
| Bush Advantage Collection Racetrack Conference Table     |    9545 |    -1934 |

**Customer Concentration**

|   customers |   sales_share_of_top_20pct_customers |
|------------:|-------------------------------------:|
|         793 |                                   48 |

**Shipping Speed**

| ship_mode      |   order_lines |   avg_days_to_ship |
|:---------------|--------------:|-------------------:|
| Same Day       |           543 |                0   |
| First Class    |          1538 |                2.2 |
| Second Class   |          1945 |                3.2 |
| Standard Class |          5967 |                5   |

**Best Months Of Year**

|   month_no |   avg_monthly_sales |
|-----------:|--------------------:|
|         11 |               88115 |
|         12 |               81323 |
|         09 |               76912 |
|         03 |               51251 |

Interactive dashboard saved: **outputs/dashboard.html**
