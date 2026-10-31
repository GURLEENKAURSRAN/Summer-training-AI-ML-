# Day 17 – Introduction to Streamlit

## Overview
On Day 17, I learned about **Streamlit**, an open-source Python library used to create interactive web applications easily. It helps convert Python scripts into web apps without requiring HTML, CSS, or JavaScript.

I explored its basic functions, display elements, widgets, data handling, and visualization features.

## Topics Covered

### 1. Introduction to Streamlit
- Streamlit is a Python framework used to build interactive web applications.
- It is commonly used for Data Science, Machine Learning, and Data Visualization projects.
- It allows users to create applications using simple Python code.

### 2. Installing Streamlit
Streamlit can be installed using pip.

```bash
pip install streamlit
```

To check the installed version:

```bash
streamlit --version
```

### 3. Creating the First Streamlit App
To create a simple application, we first import Streamlit.

```python
import streamlit as st

st.title("My First Streamlit App")
st.write("Welcome to my application!")
```

To run the application:

```bash
streamlit run app.py
```

### 4. Displaying Text
Streamlit provides different functions to display text and information.

```python
import streamlit as st

st.title("Welcome to Streamlit")
st.header("Introduction")
st.subheader("Learning Python")
st.text("This is simple text.")
st.write("Streamlit makes app development easy.")
st.markdown("**Hello!** Welcome to my app.")
```

### 5. Displaying Data
Streamlit makes it easy to display data in tabular form.

```python
import streamlit as st
import pandas as pd

data = {
    "Name": ["Aman", "Riya", "Simran"],
    "Age": [20, 21, 19]
}

df = pd.DataFrame(data)

st.dataframe(df)
st.table(df)
```

- `st.dataframe()` displays an interactive table.
- `st.table()` displays a static table.

### 6. Using Input Widgets
Widgets allow users to interact with the application.

**Text Input:**

```python
name = st.text_input("Enter your name")
st.write("Hello", name)
```

**Number Input:**

```python
age = st.number_input("Enter your age", min_value=1)
st.write("Your age is:", age)
```

**Slider:**

```python
marks = st.slider("Select your marks", 0, 100)
st.write("Your marks:", marks)
```

**Button:**

```python
if st.button("Click Me"):
    st.write("Button clicked!")
```

### 7. Selection Widgets
Streamlit provides widgets to select options.

```python
course = st.selectbox(
    "Select your course",
    ["CSE", "IT", "ECE"]
)

st.write("Selected course:", course)
```

We can also use:

```python
option = st.radio(
    "Choose an option",
    ["Python", "Java", "C++"]
)

st.write(option)
```

### 8. Checkboxes
Checkboxes allow users to select or deselect an option.

```python
agree = st.checkbox("I agree")

if agree:
    st.write("Thank you!")
```

### 9. Displaying Images
Streamlit allows us to display images in web applications.

```python
import streamlit as st

st.image("image.jpg", caption="My Image")
```

### 10. Creating Charts
Streamlit provides built-in functions to create visualizations.

```python
import streamlit as st
import pandas as pd

data = pd.DataFrame({
    "Marks": [70, 80, 65, 90, 85]
})

st.line_chart(data)
st.bar_chart(data)
st.area_chart(data)
```

These functions help represent data visually.

### 11. File Uploading
The file uploader widget allows users to upload files through the application.

```python
uploaded_file = st.file_uploader("Upload a CSV file")

if uploaded_file is not None:
    df = pd.read_csv(uploaded_file)
    st.dataframe(df)
```

### 12. Layout and Sidebar
Streamlit provides layout options to organize application content.

**Sidebar:**

```python
st.sidebar.title("Menu")
choice = st.sidebar.selectbox(
    "Choose an option",
    ["Home", "About", "Contact"]
)

st.write("You selected:", choice)
```

**Columns:**

```python
col1, col2 = st.columns(2)

with col1:
    st.write("First Column")

with col2:
    st.write("Second Column")
```

### 13. Adding Headings and Messages
Streamlit provides different message functions to display information.

```python
st.success("Task completed successfully!")
st.info("This is an information message.")
st.warning("This is a warning message.")
st.error("Something went wrong!")
```

## Key Learnings

1. Learned the basics of Streamlit and its applications.
2. Understood how to create and run a Streamlit web app.
3. Learned to display text, tables, and images.
4. Explored interactive widgets such as buttons, sliders, and select boxes.
5. Learned to upload and display CSV files.
6. Understood how to create charts and organize app layouts.
7. Learned how Streamlit can be used to build simple Data Science applications.

## Practice Questions

1. What is Streamlit?
2. Why is Streamlit used in Data Science?
3. How can we install Streamlit?
4. How do we run a Streamlit application?
5. What is the difference between `st.write()` and `st.text()`?
6. What is the purpose of `st.dataframe()`?
7. How does `st.button()` work?
8. What is the use of `st.selectbox()`?
9. How can we upload a CSV file in Streamlit?
10. How can we display charts using Streamlit?
11. What is the purpose of `st.sidebar()`?
12. How can we divide an application into columns?

## Conclusion
Today, I learned how to use Streamlit to create simple and interactive web applications using Python. I explored different widgets, data display functions, file uploading, and visualization features. These concepts will help me develop interactive applications for Data Science and Machine Learning projects.

**Google Colab / Practice Link:** [Add your Day 17 project or notebook link here]
