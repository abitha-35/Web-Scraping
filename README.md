# Web-Scraping

# 🚗 Used Cars Data Scraper & Visualizer - Hyderabad (Cars24)

This project is a **web scraping and data visualization** application built using Python. It scrapes used car listings from [Cars24 Hyderabad](https://www.cars24.com/buy-used-car/) and processes the data to extract car model names, prices, and locations. The final data is visualized using pie charts, bar graphs, and line plots.

---

## 📌 Features

- Scrapes car data from Cars24 using `requests` and `BeautifulSoup`.
- Extracts:
  - Car models
  - Specifications (KM driven, fuel type, transmission, owner type, EMI, and price)
  - Location
- Cleans and structures data using `pandas`.
- Saves data into a CSV file.
- Visualizes the data using `matplotlib` through:
  - Pie chart
  - Bar graph
  - Line plot

---

## 🧰 Technologies Used

- `requests` – to fetch HTML content.
- `BeautifulSoup` – to parse and extract data from HTML.
- `pandas` – to clean, manipulate, and save data.
- `matplotlib` – to visualize the data.

---

## 📄 Data Flow

1. **Scrape Data**:
   - Sends a GET request to the Cars24 Hyderabad page.
   - Parses the HTML content to locate and extract the container with car listings.

2. **Clean and Process**:
   - Splits and filters the raw text content into structured data fields.
   - Removes inconsistent or incomplete entries manually.
   - Stores relevant fields: car model, specification, and location.

3. **DataFrame Creation**:
   - Structures data using pandas DataFrame.
   - Extracts only the area name from the location string.
   - Saves final cleaned data to `cars2025.csv`.

4. **Data Visualization**:
   - **Pie Chart**: Proportion of different car listings and specifications.
   - **Bar Chart**: EMI comparison between selected cars.
   - **Line Plot**: Car models vs. their locations for a visual distribution.

---

## 📊 Sample Output

**CSV File (`cars2025.csv`) Format**:
| Car_models                | Car Specifications                              | Locations   |
|--------------------------|--------------------------------------------------|-------------|
| Maruti Swift Dzire VDI   | 17k km Diesel Manual 1st owner EMI ₹12368/m ₹5  | Bachupally  |
| Maruti Dzire VXI AMT     | 20k km Petrol Auto 1st owner EMI ₹12356/m ₹6    | Bachupally  |
| Hyundai Elite i20 ASTA   | 53k km Petrol Manual 1st owner EMI ₹10831/m ₹5  | Bachupally  |
| Maruti Swift VXI         | 68k km Petrol Manual 1st owner EMI ₹11730/m ₹6  | Bachupally  |
| Nissan MAGNITE XL        | 79k km Petrol Manual 1st owner EMI ₹10616/m ₹5  | Kompally    |

**Visualizations**:
- 📊 Pie Chart showing the distribution of car specs.
- 📉 Bar Chart comparing EMI of selected cars.
- 📈 Line Plot of car models by their location.

