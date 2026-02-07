# Zoo Management System (XML + HTML + JavaScript)

## About
A simple interactive zoo management mini-system built for an academic assignment.  
The project models a Zoo using a hierarchical **XML structure** (animals + employees) and displays the data in a basic **HTML + JavaScript** UI.

## What’s Included
- **Hierarchical XML model**:
  - Animals grouped by categories and sub-categories (e.g., Mammals → Primates → Monkey)
  - Employees grouped by organizational departments (e.g., Feeding, Security)
- **Interactive Web UI**:
  - Loads the XML data (embedded in `data.js`)
  - Sidebar menu for navigating the hierarchy
  - Details view that shows all attributes of a selected animal/employee

## Data Model (XML)
Root node: `<zoo>`

### Animals hierarchy
`Animals` contains 4 main categories:
- `Mammals` → `Primates / Canines / Rodents`
- `Carnivores` → `BigCats / Canines / Bears`
- `SeaAnimals` → `MarineMammals / MarineReptiles / Fish`
- `Birds` → `Parrots / Raptors / WaterBirds`

Each animal element includes **4 attributes**:
- `name`, `gender`, `age`, `food`

### Employees hierarchy
`Employees` contains 4 organizational departments:
- `Feeding`
- `Security`
- `Training`
- `Sales`

Each employee includes **4 attributes**:
- `name`, `seniority`, `age`, `salary`

## How the UI Works
1. `data.js` contains the XML as a string (`const zooXML = ...`)
2. `Web.html` parses the string using `DOMParser`
3. The sidebar renders buttons for each level in the XML hierarchy
4. Clicking a category navigates deeper; clicking a leaf node shows all attributes in the details panel

## How to Run
### Option A: Open directly
1. Download/clone the repository
2. Open `Web.html` in your browser

### Option B (Recommended): Run via a local server
Some browsers restrict local file access. Running a local server avoids issues:

**Python**
```bash
python -m http.server 8000
