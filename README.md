# AI-Powered Sales Buddy 🤖💼

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)](https://flask.palletsprojects.com/)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4-orange.svg)](https://openai.com)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> An intelligent sales companion that transforms how sales teams capture, analyze, and act on sales data using AI-driven insights.

Developed for the **"Reimagining Sales with AI" Hackathon** organized by **QA Catalyst**.

## 🌟 Overview

The AI Sales Buddy is a comprehensive Flask-based web application designed to empower sales teams with intelligent automation and insights. It streamlines the entire sales process from meeting notes to market analysis, helping sales representatives and leadership teams make data-driven decisions.

## ✨ Key Features

### 🎯 Internal Sales Activity Reporter
- **Interactive Chat Interface**: Intuitive form for logging client interactions
- **AI-Powered Sentiment Analysis**: Automatic sentiment detection using OpenAI GPT API
- **Sales Pipeline Tracking**: Monitor opportunities and proposal status
- **Real-time Analytics**: Auto-calculated metrics including:
  - Total active clients
  - Number of client visits
  - Proposals submitted
  - Estimated sales value
- **Smart Dashboard**: Visual overview of recent activities and performance metrics

### 📊 Market & Industry Insights Engine
- **Company Intelligence**: AI-generated business insights tailored to specific companies
- **Comprehensive Market Analysis**:
  - Latest industry developments
  - Competitor landscape analysis
  - Market trends and patterns
  - Risk assessment and opportunities
- **RESTful API**: JSON endpoint for programmatic access to company insights
- **User-friendly Interface**: Clean UI for viewing and analyzing market data

## 🛠️ Technology Stack

| Component | Technology |
|-----------|------------|
| **Backend** | Python Flask, SQLAlchemy, SQLite |
| **Frontend** | HTML5, CSS3, Jinja2 Templates |
| **AI Integration** | OpenAI GPT-3.5/4 API (ChatCompletion) |
| **Authentication** | Flask-Login with JWT-ready configuration |
| **Database** | SQLite (development), PostgreSQL-ready |
| **Visualization** | Jinja-based Dashboard Views |

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- OpenAI API key
- pip package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ai-powered-sales-buddy.git
   cd ai-powered-sales-buddy
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   Edit `.env` file and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   SECRET_KEY=your_secret_key_here
   ```

5. **Initialize the database**
   ```bash
   flask db init
   flask db migrate -m "Initial migration"
   flask db upgrade
   ```

6. **Run the application**
   ```bash
   python app.py
   ```

The application will be available at `http://localhost:5000`

## 📱 Usage

### Sales Activity Logging
1. Navigate to the Sales Reporter section
2. Fill in client meeting details through the chat-like interface
3. The AI will automatically analyze sentiment and extract key insights
4. View real-time updates to your sales metrics

### Market Insights
1. Access the Market Insights section
2. Enter a company name to get AI-powered analysis
3. Review comprehensive reports on market trends and opportunities
4. Use the API endpoint `/api/insights/<company_name>` for programmatic access

## 🏗️ Project Structure

```
ai-powered-sales-buddy/
├── app.py                 # Main Flask application
├── config.py             # Configuration settings
├── requirements.txt      # Python dependencies
├── .env.example         # Environment variables template
├── models/
│   ├── __init__.py
│   ├── user.py          # User authentication model
│   └── sales.py         # Sales data models
├── routes/
│   ├── __init__.py
│   ├── auth.py          # Authentication routes
│   ├── sales.py         # Sales activity routes
│   └── insights.py      # Market insights routes
├── templates/
│   ├── base.html        # Base template
│   ├── dashboard.html   # Main dashboard
│   ├── sales_form.html  # Sales logging form
│   └── insights.html    # Market insights view
├── static/
│   ├── css/
│   ├── js/
│   └── images/
└── tests/
    ├── test_app.py
    ├── test_models.py
    └── test_routes.py
```

## 🔌 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/insights/<company>` | GET | Get AI-powered company insights |
| `/api/sales/activities` | GET | Retrieve sales activities |
| `/api/sales/metrics` | GET | Get sales performance metrics |
| `/api/sentiment/analyze` | POST | Analyze text sentiment |

## 🧪 Testing

Run the test suite:
```bash
python -m pytest tests/
```

For coverage report:
```bash
python -m pytest --cov=. tests/
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📋 Roadmap

- [ ] Advanced analytics dashboard
- [ ] Integration with CRM systems
- [ ] Mobile app development
- [ ] Multi-language support
- [ ] Advanced AI models integration
- [ ] Real-time notifications
- [ ] Export functionality (PDF, Excel)

## 🐛 Known Issues

- Sentiment analysis accuracy may vary with complex business terminology
- API rate limiting may affect bulk operations
- Dashboard performance with large datasets needs optimization

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **QA Catalyst** for organizing the "Reimagining Sales with AI" Hackathon
- **OpenAI** for providing the GPT API
- **Flask** community for excellent documentation and support
- All contributors and testers who helped improve this project

## 📞 Support

If you encounter any issues or have questions:

- 📧 connect me
