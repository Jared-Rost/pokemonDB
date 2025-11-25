# PokémonDB - Relational Database Project 🎮💾

> A comprehensive relational database exploring the Pokémon universe and its interconnected data

Developed for **University of Manitoba COMP 3380** - Database Concepts and Usage

## 📋 Overview

PokémonDB is a full-stack database application that leverages publicly available Pokémon datasets to create a relational database system. The project demonstrates complex relationships between various entities in the Pokémon universe, including Pokémon species, moves, abilities, types, and more. It features a web-based query interface, custom visualization tools, and automated data processing scripts.

### Key Features

- 🗃️ **Relational Database Design** - Normalized schema with complex entity relationships
- 🔍 **Interactive Query Interface** - Web-based UI for executing custom queries
- 📊 **Data Visualization** - Graph and chart support for query results
- 🎨 **ER Diagram Tool** - Custom Python tool for visualizing database schemas
- 🐍 **Data Processing Scripts** - Automated CSV parsing and SQL generation
- 🌐 **Full-Stack Application** - Backend API with frontend interface

## 🛠️ Tech Stack

### Backend (57.9% Python, 27.2% Go)
- **Python** - Data processing scripts and ER diagram tool
- **Go** - Backend API server
- **SQL** - Database queries and schema design
- **PostgreSQL/MySQL** - Relational database system

### Frontend (9.9% JavaScript, 3.1% CSS, 1.8% HTML)
- **JavaScript** - Interactive UI logic
- **HTML/CSS** - Web interface styling
- **Query Builder** - Dynamic parameter input system

### DevOps (0.1% Makefile)
- **Make** - Build automation

## 🚀 Getting Started

### Prerequisites

- Python 3.x with tkinter
- Go 1.x or higher
- SQL database server (PostgreSQL or MySQL)
- Access to University of Manitoba database server (for original deployment)

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Jared-Rost/pokemonDB.git
   cd pokemonDB
   ```

2. **Set Up Python Environment**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Database Connection**
   - Update database connection settings in configuration files
   - Ensure database server is accessible

4. **Build and Run**
   ```bash
   make
   ```

### Important Note

⚠️ **This project no longer runs in its original form** as it requires remote access to the University of Manitoba database server, which is no longer available. The code serves as a reference implementation and portfolio piece.

## 🏗️ Project Structure

```
pokemonDB/
├── Scripts/
│   ├── ErDiagramDrawer/    # Python tool for ER diagram visualization
│   │   ├── main.py         # Main diagram tool
│   │   └── README.md       # Tool documentation
│   ├── UI/                 # Query interface and metadata
│   │   ├── queries.json    # Query definitions
│   │   └── README.md       # UI documentation
│   └── [data processing]   # CSV to SQL conversion scripts
├── SQL/                    # Database schema and queries
├── Backend/                # Go API server
├── Frontend/               # Web interface
├── Makefile               # Build automation
└── README.md              # This file
```

## 🎨 Custom Tools

### ER Diagram Drawer

A Python-based tool for creating and editing Entity-Relationship diagrams.

**Features:**
- Load database schema from JSON
- Interactive drag-and-drop interface
- Click and drag entities to arrange layout
- Save diagrams (Ctrl+S)
- Optional GUI controls (keys 'a' and 's')

**Usage:**
```bash
cd Scripts/ErDiagramDrawer
python3 main.py
```

**Dependencies:**
- tkinter (usually included with Python)

### Query Interface

A metadata-driven query system that dynamically generates UI forms.

**Parameter Types:**
- `int` - Single number (e.g., 123)
- `string` - Text string (e.g., "Pikachu")
- `string_set` - List of strings (e.g., ["Fire", "Water"])
- `int_set` - List of integers (e.g., [1, 2, 3])

**Display Types:**
- `string` - Text-based results
- `graph` - X-Y plane visualization

**Query Definition Example:**
```json
{
    "query_name": {
        "parameters": [
            {
                "name": "pokemon_id",
                "order": [1, 3],
                "type": "int"
            }
        ],
        "return_parameters": [
            {
                "name": "pokemon_name",
                "order": [1],
                "type": "string"
            }
        ],
        "display": "string",
        "sql_file": "example.sql"
    }
}
```

## 📊 Database Schema

The database models various aspects of the Pokémon universe:

- **Pokémon** - Species information, stats, abilities
- **Moves** - Attack moves with type, power, accuracy
- **Types** - Type effectiveness relationships
- **Abilities** - Special abilities and effects
- **Evolution** - Evolution chains and conditions
- **Cards** - Trading card game data
- **Games** - Version-specific information

## 🔍 Sample Queries

The system supports various complex queries:
- Find Pokémon by type and stat ranges
- Analyze type effectiveness matchups
- Track evolution chains
- Search moves by power and accuracy
- Compare stats across generations

## 💡 Technical Highlights

### Data Processing
- Automated CSV to SQL conversion using Excel formulas
- Python scripts for data cleaning and transformation
- Batch processing of large datasets

### Database Design
- Normalized schema (3NF/BCNF)
- Complex many-to-many relationships
- Referential integrity constraints
- Efficient indexing strategies

### Full-Stack Integration
- RESTful API design
- Dynamic query generation
- Parameterized queries for security
- JSON-based metadata configuration

## 📚 Data Sources

Uses publicly available Pokémon datasets from:
- Official Pokémon databases
- Community-maintained APIs
- Trading card game databases
- Video game data dumps
