# Adamawa Coverage Dashboard

> A data analytics dashboard for monitoring Mass Drug Administration (MDA) coverage in Adamawa State, Nigeria.

[![Streamlit](https://img.shields.io/badge/Built%20with-Streamlit-FF4B4B?style=flat&logo=streamlit)](https://streamlit.io)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat&logo=python)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## About

This dashboard is part of the **SARMAAN II Coverage Evaluation Survey** conducted by **eHealth Africa (eHA)**. It provides real-time monitoring and quality control for household survey data collected across 6 Local Government Areas (LGAs) in Adamawa State.

The dashboard helps field teams and supervisors track data collection progress, identify data quality issues, and ensure accurate coverage reporting.

## Features

### Data Monitoring
- Real-time data synchronization from KoboToolbox
- Track planned vs. reached households by community
- Monitor submission status and validation progress
- View coverage percentages and completion rates

### Quality Control
- Automated data quality checks (15+ validations)
- Identify age inconsistencies and duplicate entries
- Flag education-occupation mismatches
- Detect child eligibility issues
- Highlight missing or invalid data

### Access Control
- **Admin users**: View all LGA data
- **LGA users**: View only assigned LGA data
- Simple username-based authentication

### Visualizations
- Interactive charts and graphs
- Coverage maps by LGA and ward
- Timeline of data collection
- Validation status breakdown

## Coverage Area

- **State**: Adamawa
- **LGAs**: 6 (Demsa, Guyuk, Hong, Madagali, Michika, Song)
- **Wards**: Multiple per LGA
- **Communities**: 24
- **Target Households**: ~1,550

## Getting Started

### Prerequisites

- Python 3.8 or higher
- KoboToolbox account with data export access

### Installation

1. Clone this repository:
```bash
git clone https://github.com/eHealthAfrica/adamawa-coverage-dashboard.git
cd adamawa-coverage-dashboard
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Configure your KoboToolbox data source:

Create a file `.streamlit/secrets.toml` with:
```toml
KOBO_DATA_URL = "your_kobo_export_url_here"
```

4. Run the dashboard:
```bash
streamlit run Adamawa_ces_qc_app.py
```

The dashboard will open in your browser at `http://localhost:8501`

## User Access

### Admin
- **Username**: `Admin`
- **Access**: All 6 LGAs

### LGA Users
| Username | Access |
|----------|--------|
| Demsa | Demsa LGA only |
| Guyuk | Guyuk LGA only |
| Hong | Hong LGA only |
| Madagali | Madagali LGA only |
| Michika | Michika LGA only |
| Song | Song LGA only |

*Note: No passwords required*

## Deployment

### Deploy to Streamlit Cloud

1. Push your code to GitHub
2. Visit [share.streamlit.io](https://share.streamlit.io/)
3. Create a new app and select your repository
4. Add your `KOBO_DATA_URL` in the Secrets section
5. Deploy!

## Data Quality Checks

The dashboard automatically performs these checks:

- ✅ Age consistency (years living vs household head age)
- ✅ Education-occupation compatibility
- ✅ Valid child counts (no negative values)
- ✅ Eligible children verification
- ✅ Child age validation (1-59 months)
- ✅ Duplicate household detection
- ✅ Urban household amenities check
- ✅ Repetitive child selection detection

## Technology Stack

- **Framework**: Streamlit
- **Data Processing**: Pandas
- **Visualization**: Plotly Express
- **Data Source**: KoboToolbox API
- **Export**: Excel (OpenPyXL)

## Support

For technical support or questions:
- Open an issue in this repository
- Contact the eHA technical team
- SARMAAN II project coordinators

## Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- **eHealth Africa (eHA)** - Project implementation
- **SARMAAN II Project** - Funding and oversight
- Field teams and supervisors in Adamawa State

---

**Developed by eHealth Africa** | [www.ehealthafrica.org](https://www.ehealthafrica.org)

*Making quality healthcare available to everyone*
