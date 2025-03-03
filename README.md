# 📊 Sustainable Development Analysis Based on SUSENAS 2017 Data

## 👥 Author   
**Jihan Fadila** (105222022)  
📧 Email: jihan4han97@gmail.com

---

## 📌 Project Description
This project aims to analyze the potential for sustainable development in various provinces of Indonesia using data from the 2017 National Socioeconomic Survey (SUSENAS) and population projection data. The analysis identifies the most potential provinces for development and clusters regions based on socioeconomic characteristics.

## Data Structure
The data used comes from various sources, including:
- **SUSENAS 2017** by BPS-Statistics Indonesia
- **Population Projection 2017** by BPS-Statistics Indonesia
- **Province data** obtained through web scraping

The main columns in the dataset include:

1. `CHILDREN` - Percentage of children in the population
2. `FEMALE` - Percentage of females in the population
3. `ELDERLY` - Percentage of elderly people in the population
4. `FHEAD` - Percentage of female-headed households
5. `FAMILYSIZE` - Average number of family members per household
6. `NOELECTRIC` - Percentage of households without electricity access
7. `LOWEDU` - Percentage of population with low education
8. `GROWTH` - Population growth rate
9. `POVERTY` - Poverty rate
10. `ILLITERATE` - Percentage of illiterate people
11. `NOTRAINING` - Percentage of people without training
12. `DPRONE` - Disaster-prone vulnerability
13. `RENTED` - Percentage of households renting homes
14. `NOSEWER` - Percentage of households without sanitation access
15. `POPULATION` - Total population

## 🛠 Analysis Steps

### 1. Data Collection and Understanding
- Importing data from external sources
- Conducting an initial data exploration, including checking data types and missing values
- Displaying data distribution using visualizations such as boxplots

### 2. Data Preprocessing
- Merging the main dataset with province data using region codes
- Filling missing values based on external sources
- Normalizing percentage values to a range of 0-1
- Correcting province data mismatches with region codes

### 📊 3. Insight and Analysis
#### **A. Identifying Potential Areas for Development (Sustainability Index)**
- Calculating the Sustainability Index based on factors such as poverty, electricity access, water access and education

  **Suistainability Index Formula:**
  **Sustainability_Index = w1×(1−POVERTY) + w2×(1−NOELECTRIC) + w3×TAPWATER + w4×(1−LOWEDU) + w5×(1−ILLITERATE)**

  where:
  **𝑤1=0.3
  𝑤2=0.2
  𝑤3=0.2
  𝑤4=0.15
  𝑤5=0.15**
  
- Visualizing the development index across Indonesia using maps
- Identifying provinces with the highest Sustainability Index as priority development areas

#### **Result:**
- The province with the highest Sustainability Index is **East Kalimantan** with an index value of **0.82213**. This indicates that the province has the highest potential for short-term development.
- **North Kalimantan** has a Sustainability Index of **0.794466**, making it the most optimal province for long-term development among those with the highest population growth rates (**4.277%**) and a moderate population of **627,255 people**. If growth factors remain stable, the long-term development potential in North Kalimantan is expected to be high. The government could implement periodic development in this province, given its considerable potential and optimal development opportunities.

#### **B. Clustering Regions Based on Socioeconomic Characteristics**
- Using Principal Component Analysis (PCA) to reduce dimensions
- Determining the optimal number of clusters using the Elbow method
- Performing clustering using the K-Means algorithm with K=3
- Identifying characteristics of each cluster based on factors such as population, growth rate, and family structure
- Visualizing clustering results with different colors for each group of provinces

#### **Result:**
- **Cluster 0 (Purple)**: Represents regions with high population but moderate values for other factors.
- **Cluster 1 (Turquoise)**: Represents regions with the highest population growth rate (**>4%**), largest family size, and the highest number of children.
- **Cluster 2 (Yellow)**: Represents regions dominated by a higher percentage of females but with low growth rates and the highest elderly population.
- The clustering results indicate that **Cluster 2** has the least optimal potential for long-term development due to the high proportion of elderly people and low growth rates.

### 🎯 4. Recommendations for Future Work
- **Short-Term Development:** Based on the highest Sustainability Index, **East Kalimantan (0.82213)** is identified as the most optimal province for short-term development.
- **Long-Term Development:**
  - **East Kalimantan (0.82213)** is also the best candidate for long-term development due to its large population (**3,639,252 people**) and moderate growth rate (**1.8478%**).
  - **North Kalimantan (0.794466)** has the highest population growth rate (**4.277%**) with a moderate population of **627,255 people**, making it another strong candidate for long-term development if growth factors remain stable.
- **Research Enhancements:** Additional factors such as land area, geographical conditions, and birth rates should be considered to improve analysis accuracy.

## Technologies Used
- **Python** for data analysis
- **Pandas** for data manipulation
- **NumPy** for numerical computations
- **Matplotlib & Seaborn** for data visualization
- **BeautifulSoup** for web scraping
- **Geopandas** for spatial data mapping
- **Scikit-learn** for clustering and PCA analysis

## Conclusion
This analysis demonstrates that a data-driven approach can assist in sustainable development planning. **East Kalimantan (0.82213) and North Kalimantan (0.794466)** are identified as high-potential development areas; however, additional factors should be explored further for more accurate decision-making.
