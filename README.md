
# WellPred Disease Prediction System

A web application built with **Django** and **Machine Learning** (Scikit-learn) that provides predictions for various diseases based on user input.

The system currently supports prediction for the following conditions:

  * Heart Disease
  * Kidney Disease
  * Cervical Conditions

-----

## Getting Started

Follow these steps to set up and run the project on your local machine.

### Prerequisites

You need the following software installed on your system:

  * **Python 3.10+** (The project environment uses Python 3.12)
  * **Git** (For cloning the repository)

### 1\. Clone the Repository

Open your terminal or command prompt and run the following command to download the project files:

```bash
git clone https://github.com/tharun-k-m/wellpred_django.git
```

### 2\. Set up the Virtual Environment

It is highly recommended to use a **virtual environment** to manage dependencies.

**On Windows:**

```bash
python -m venv env
.\env\Scripts\activate
```

**On macOS/Linux:**

```bash
python3 -m venv env
source env/bin/activate
```

*(The environment name `env` matches the one in your folder structure.)*

### 3\. Install Dependencies

With the virtual environment activated, install all required packages using `pip`.

```bash
pip install -r requirements.txt
```

*Note: This step assumes you have a `requirements.txt` file in the root directory listing packages like Django, pandas, and scikit-learn.*

### 4\. Database Migrations

Apply the initial database migrations for the Django project.

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5\. Run the Server

Finally, start the Django development server:

```bash
python manage.py runserver
```

The application will now be running at: **[http://127.0.0.1:8000/](https://www.google.com/search?q=http://127.0.0.1:8000/)**

-----

## Project Structure Highlights

| Directory | Purpose |
| :----- | :----- |
| `DjangoWellPred/` | The main Django project configuration (settings, URLs). |
| `app/` | Primary Django application (views, basic models, logic). |
| `templates/` | Contains HTML templates (`heart/`, `kidney/`, `cervical/` UI). |
| `static/` | Static assets like CSS and JavaScript. |
| `pickles/` | **Crucial:** Stores the pre-trained machine learning models (e.g., `heart_model.pkl`). |
| `env/` | The Python Virtual Environment. |

## How Prediction Works

1.  A user navigates to a prediction page (e.g., `/heart/`).
2.  The user inputs the required health parameters into the form.
3.  The Django view loads the corresponding machine learning model from the `pickles/` directory using `joblib` or `pickle`.
4.  The input data is processed (e.g., scaled, encoded) and fed into the model.
5.  The model returns a prediction (e.g., 0 or 1).
6.  The result is displayed to the user on the webpage.

## Contributing

If you find a bug or have an enhancement idea, please open an issue or submit a pull request\!


You can also connect with me on tharunkm000@gmail.com or https://www.linkedin.com/in/tharunkm/


-----
