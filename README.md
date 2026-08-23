# 🔬 Scientific Image Generation Platform

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/)
[![React](https://img.shields.io/badge/react-18.0+-61DAFB.svg)](https://reactjs.org/)
[![FastAPI](https://img.shields.io/badge/fastapi-0.104.0-009688.svg)](https://fastapi.tiangolo.com/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

> 🚀 **An AI-powered web application for generating scientific images including microscopy, medical scans, satellite imagery, and scientific visualizations using Diffusion Models, GAN, UNet, and Gemini API.**

---

## 📋 Table of Contents

- [✨ Features](#-features)
- [🎯 Use Cases](#-use-cases)
- [🛠️ Technology Stack](#️-technology-stack)
- [📸 Screenshots](#-screenshots)
- [🚀 Quick Start](#-quick-start)
- [📁 Project Structure](#-project-structure)
- [🗄️ Database Schema](#️-database-schema)
- [🔗 API Documentation](#-api-documentation)
- [🎨 UI Design](#-ui-design)
- [🤖 AI Models](#-ai-models)
- [📊 Performance](#-performance)
- [🔮 Future Enhancements](#-future-enhancements)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [🙏 Acknowledgments](#-acknowledgments)
- [📞 Contact](#-contact)

---

## ✨ Features

### 🖼️ Image Generation Capabilities
- **Microscopy Images**: Generate cellular structures, tissue samples, and microscopic organisms
- **Medical Scans**: Create MRI, CT, X-ray, and ultrasound-style medical imagery
- **Satellite Imagery**: Generate Earth observation images, terrain maps, and geographical visualizations
- **Scientific Visualizations**: Create charts, diagrams, molecular structures, and physics simulations

### 🧠 AI Model Integration
- **Diffusion Models**: High-quality, detailed image generation with fine control
- **GANs (Generative Adversarial Networks)**: Quick, realistic image synthesis
- **UNet Architecture**: Specialized for medical and scientific image segmentation and generation
- **Gemini API Integration**: Enhanced capabilities for complex scientific visualizations

### 🎨 User Experience
- **Modern React UI**: Clean, responsive, and intuitive interface with Material-UI
- **Parameter Controls**: Fine-tune every aspect of image generation
- **Real-time Preview**: See results as they're being generated
- **History Tracking**: Complete generation history with search and filter
- **Download & Share**: Export generated images in multiple formats (PNG, JPG, SVG)
- **Dark/Light Mode**: Eye-friendly themes for comfortable viewing
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices

### 🔒 Security & Performance
- **JWT Authentication**: Secure user access and data protection
- **Rate Limiting**: Prevent API abuse and ensure fair usage
- **Async Processing**: Non-blocking generation for better performance
- **SQL Database**: Efficient storage and retrieval of user data and generations
- **Input Validation**: Robust validation for all user inputs
- **Error Handling**: Graceful error handling with user-friendly messages

---

## 🎯 Use Cases

| Domain | Application |
|--------|-------------|
| **Academic Research** | Generate training data for ML models, create synthetic datasets |
| **Medical Education** | Create teaching materials, case studies, and visualization aids |
| **Scientific Publication** | Generate figures, diagrams, and visualizations for papers |
| **Content Creation** | Create engaging scientific content for blogs and social media |
| **Data Augmentation** | Expand limited datasets for training AI models |
| **Visual Communication** | Explain complex concepts through imagery |
| **Drug Discovery** | Generate molecular structures and biological imagery |
| **Environmental Science** | Create satellite imagery and climate visualizations |

---

## 🛠️ Technology Stack

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| React | 18.2.0 | UI Library |
| Material-UI | 5.14.19 | Component Library |
| Framer Motion | 10.16.5 | Animations |
| Axios | 1.6.2 | HTTP Client |
| React Router | 6.20.0 | Navigation |
| React Hook Form | 7.47.0 | Form Handling |
| Chart.js | 4.4.0 | Data Visualization |

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| FastAPI | 0.104.0 | Web Framework |
| SQLAlchemy | 2.0.23 | ORM |
| Pydantic | 2.5.0 | Data Validation |
| JWT | 3.3.0 | Authentication |
| Celery | 5.3.4 | Task Queue |
| Redis | 5.0.1 | Caching |

### AI/ML
| Technology | Version | Purpose |
|------------|---------|---------|
| PyTorch | 2.1.0 | Deep Learning |
| Diffusers | 0.24.0 | Diffusion Models |
| Transformers | 4.35.0 | Hugging Face Models |
| OpenCV | 4.8.1.78 | Image Processing |
| Google Gemini API | Latest | AI Generation |

### Database
| Technology | Purpose |
|------------|---------|
| PostgreSQL | Production Database |
| SQLite | Development Database |
| Alembic | Database Migrations |

---

## 📸 Screenshots

### Home Page
![Home Page](screenshots/home.png)
*Landing page with features overview and quick generation demo*

### Image Generation Page
![Generation Page](screenshots/generate.png)
*Parameter controls, model selection, and real-time preview*

### Gallery Page
![Gallery Page](screenshots/gallery.png)
*Grid view of generated images with filters and search*

### History Page
![History Page](screenshots/history.png)
*Timeline view of all generations with filters*

### Settings Page
![Settings Page](screenshots/settings.png)
*User preferences and API configuration*

---

## 🚀 Quick Start

### Prerequisites
- Python 3.9 or higher
- Node.js 16 or higher
- npm 7 or higher
- Git
- Google Gemini API Key (get from [Google AI Studio](https://makersuite.google.com/app/apikey))

### Installation

#### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/sci-image-generation-platform.git
cd sci-image-generation-platform

# Navigate to backend directory
cd backend

# Create and activate virtual environment
python -m venv venv

# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
cp .env.example .env

# Edit .env with your configurations
# Add your GEMINI_API_KEY and other settings
nano .env

# Navigate to frontend directory
cd ../frontend

# Install dependencies
npm install

# Create .env file
cp .env.example .env

# Edit .env with your API URL
nano .env

# Navigate to database directory
cd ../database

# Initialize database
python init_db.py

# Run migrations
python migrate.py

cd backend
source venv/bin/activate  # On Windows: venv\Scripts\activate
uvicorn main:app --reload --host 0.0.0.0 --port 8000

cd frontend
npm start