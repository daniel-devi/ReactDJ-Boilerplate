# ReactDJ Project Boilerplate

A React and Django boilerplate featuring basic authentication, an admin panel, and a landing page. This setup is perfect for quickly starting new projects with a solid foundation in both frontend and backend technologies.

---

## **Features**
- **Basic Authentication**: Includes login, logout, signup, and password reset functionalities.
- **Admin Panel Setup**: Pre-configured with Jazzmin for a modern and customizable admin interface.
- **User Model Integration**: Basic user models ready for customization and extension.
- **CORS Setup**: Handles cross-origin requests effortlessly.
- **JWT Integration**: Uses JWT for secure authentication and session management.

---

## 🛠️ **Dependencies**
### **Frontend**
- **React**: Frontend library for building interactive UIs.
- **Axios**: For making HTTP requests to the backend.

### **Backend**
- **Django**: Powerful Python web framework.
- **Django Rest Framework (DRF)**: For building robust APIs.
- **Jazzmin**: Custom admin theme to enhance the Django admin interface.
- **corsheaders**: Handles Cross-Origin Resource Sharing.
- **jwt-decode**: Decodes JSON Web Tokens on the frontend for secure access.

---

## 📦 **Setup Instructions**

### **1. Clone the repository**
```bash
git clone https://github.com/your-username/reactdj-boilerplate.git
cd reactdj-boilerplate
```

### **2. Install Dependencies**
#### **Frontend**
```bash
cd Frontend
npm install
```

#### **Backend**
```bash
cd Backend
pip install -r requirements.txt
```

### **3. Run the Project**
#### **Backend**
```bash
python manage.py runserver
```

#### **Frontend**
```bash
cd Frontend
npm run dev
```

---

## 📂 **Project Structure**
```
ReactDJ-Boilerplate/
│
├── frontend/                # React frontend
│   ├── src/
│   ├── public/
│   └── package.json
│
├── backend/                 # Django backend
│   ├── manage.py
│   ├── requirements.txt
│   └── Backend/
│       ├── settings.py
│       ├── urls.py
│       └── wsgi.py
│
├── docs/                    # Documentation
├── README.md                # Project documentation
└── LICENSE                  # License information
```

---

## 🔑 **Special Notes**
- **Secret Key**: Each project should use a unique secret key. Replace the default in `settings.py` for production deployments.
- **Admin Panel**: Accessible at `/admin` with customizable themes via Jazzmin.

---

## 🤝 **Contributing**
Contributions are welcome! Please open an issue first to discuss potential changes.

---

## 📄 **License**
This project is free to use and distributed under the MIT License. See the `LICENSE` file for details.

---

## 📘 **Documentation**
Detailed project documentation can be found in the `/docs` folder, including setup guides, API customization tips.

---

This setup should get you started quickly, and contributions are always appreciated! 🚀