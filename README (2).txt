# Cloud Kitchen and Service Station Optimization Project

This project analyzes and optimizes the placement of cloud kitchens and their assignments to service stations using geospatial data, data visualization, and linear programming.

## Project Structure

### Task I: Data Preparation and Visualization
- Geocode addresses from a CSV using the `geopy` package to generate latitude and longitude.
- Generate 50 random service station points within a boundary around cloud kitchens.
- Create visualizations to display cloud kitchens and service stations using `matplotlib`.
- Tabulate and export coordinates for kitchens and stations using `pandas` and `tabulate`.
- Calculate haversine distances between each kitchen and station and export the distance matrix.

### Task II: Optimization Using Linear Programming
- Define and solve an assignment problem using the `pulp` package to:
  - Assign each service station to exactly one cloud kitchen.
  - Ensure each cloud kitchen serves exactly two service stations.
- Output results:
  - `.mps` file for LP model
  - Solution stored in a CSR (Compressed Sparse Row) format
  - Origin-Destination (OD) pair list with corresponding distances

### Task III: Insights and Visualization
- Generate a bar chart showing the frequency of assignments across three distance ranges: `<3 miles`, `3–6 miles`, and `>6 miles`.
- Build a network graph using `networkx` to visualize kitchen-to-station assignments.

## Deliverables

| Deliverable | File Name |
|------------|------------|
| Geocoded Cloud Kitchen Data | Pythonproject_DallasdataCo-ordinates.csv |
| Random Service Station Data | random_points.csv |
| Cleaned Address Data | Locations.txt |
| Service Station Locations | service_stations_co-ordinates.txt |
| Distance Matrix | Distances.csv |
| LP Model File | AP.mps |
| CSR Matrix | Solution.csr |
| Origin-Destination Table | OD.txt |
| Distance Frequency Plot | Frequency.jpeg |
| Assignment Network Graph | Solution.jpeg |

## Technologies Used

- Python Libraries: pandas, geopy, matplotlib, networkx, pulp, scipy, tabulate, math
- Data Visualization: Power BI-compatible CSVs, Matplotlib visualizations
- Optimization: Linear Programming with `pulp`

## How to Run

1. Update the `common_path` variable with your local file path.
2. Run each cell or script sequentially to generate outputs and visualizations.
3. Ensure you have all required Python libraries installed (`pip install -r requirements.txt` if using one).
4. Output files will be saved to your specified directory.

## Team

Project completed as part of ISE 535 course by Team 20.
