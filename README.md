# CUNI FSV Research Publications Explorer

A web-based research publication browser for Charles University's Faculty of Social Sciences (FSV) academic publications. This single-page application allows users to search, sort, and explore thousands of academic theses and papers harvested from the university's institutional repository.

## Features

- **Multi-Dataset Support** - Browse three different publication collections:
  - IPS Theses (110 records from Institute of Political Studies)
  - All FSV Theses (19,851 records across all FSV departments)
  - Prague Papers IR (146 records on History of International Relations)

- **Advanced Search** - Full-text search across titles, authors, supervisors, keywords, abstracts, and institutes

- **Sortable Columns** - Sort by year, title, author, supervisor, or institute (ascending/descending)

- **Pagination** - Configurable page sizes (25, 50, or 100 records) with intuitive navigation

- **Expandable Abstracts** - View truncated abstracts with option to expand full text

- **Performance Optimized** - IndexedDB caching for instant loading of large datasets with progress indicators

- **Responsive Design** - Works on desktop and mobile devices

## Tech Stack

- HTML5
- CSS3 (Flexbox, animations, responsive design)
- Vanilla JavaScript
- IndexedDB for client-side caching

## Data Source

Publications are harvested from Charles University's DSpace repository using the OAI-PMH (Open Archives Initiative Protocol for Metadata Harvesting) protocol.

Each record includes:
- Title and abstract
- Author and supervisor
- Keywords and subjects
- Publication year
- Institute/department
- Direct link to full publication

## Project Structure

```
fsv-publications/
├── explore.html           # Main application (single-page app)
├── records.json           # IPS Theses dataset (~110 records)
├── all_fsv_records.json   # All FSV Theses dataset (~19,851 records)
├── prague_papers_ir.json  # Prague Papers IR dataset (~146 records)
└── README.md
```

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/fsv-publications.git
   ```

2. Open `explore.html` in a web browser, or serve it via a local server:
   ```bash
   # Using Python
   python -m http.server 8000

   # Using Node.js
   npx serve
   ```

3. Select a dataset from the dropdown and start exploring publications.

## Usage

- **Search**: Type in the search box to filter records across all fields
- **Sort**: Click column headers to sort (click again to reverse order)
- **Navigate**: Use pagination controls at the bottom to browse through results
- **View Details**: Click "Expand" on any abstract to read the full text
- **Access Publication**: Click the handle link to view the full publication in DSpace

## License

This project provides access to publicly available academic metadata from Charles University's institutional repository.
