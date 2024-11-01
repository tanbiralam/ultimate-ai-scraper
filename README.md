# Project Documentation

## Table of Contents

1. [streamlit_app.py](#streamlit_app.py)
2. [scraper.py](#scraper.py)
3. [pagination_detector.py](#pagination_detector.py)
4. [assets.py](#assets.py)
5. [api_management.py](#api_management.py)

---

## 1. `streamlit_app.py`

### Description

This file serves as the main entry point for the Streamlit application. It initializes the app, handles user interactions, and integrates various functionalities through a user-friendly interface.

### Key Functionalities

- **User Interface Initialization**: Sets up the layout and components of the Streamlit application, including headers, inputs, and buttons.
- **Session State Management**: Utilizes Streamlit’s session state to maintain user inputs and other necessary data across app interactions.
- **Integration of Components**: Calls functions from other modules (like API management and pagination detection) to provide a cohesive experience.
- **API Key Input**: Facilitates user input for API keys, which are crucial for accessing external services.

### Notable Implementations

- Use of Streamlit components (e.g., `st.text_input`, `st.button`) for user interactions.
- Streamlit’s session state to persist user data across interactions.

---

## 2. `scraper.py`

### Description

This file is responsible for scraping data from web pages using specified selectors. It implements the core scraping logic that interacts with web pages and retrieves content.

### Key Functionalities

- **Web Scraping**: Uses libraries (like BeautifulSoup and requests) to fetch and parse HTML content from target URLs.
- **Selector-Based Extraction**: Implements functions to extract information based on CSS selectors provided by the user.
- **Data Handling**: Processes and structures the scraped data for further usage or analysis.

### Notable Implementations

- Utilizes exception handling to manage potential errors during web requests or parsing.
- Support for dynamic content extraction based on user-defined selectors, enhancing flexibility.

---

## 3. `pagination_detector.py`

### Description

This module detects pagination within web pages, allowing the scraper to navigate through multiple pages of content efficiently.

### Key Functionalities

- **Pagination Detection**: Identifies pagination elements (like "Next" buttons or page numbers) within HTML documents.
- **URL Generation**: Constructs new URLs to access additional pages based on the detected pagination elements.
- **Integration with Scraping Logic**: Works alongside the `scraper.py` module to enhance scraping capabilities across multi-page documents.

### Notable Implementations

- Use of regex or specific selectors to identify pagination links.
- Dynamic URL construction that adapts to different website structures.

---

## 4. `assets.py`

### Description

This file manages static assets and resources used throughout the application, such as images, CSS, and JavaScript files.

### Key Functionalities

- **Asset Management**: Centralizes the storage and retrieval of static assets required by the Streamlit app.
- **Dynamic Loading**: Facilitates the dynamic loading of assets into the app as needed, ensuring a smooth user experience.

### Notable Implementations

- Organized structure for asset files, making it easy to maintain and access resources.

---

## 5. `api_management.py`

### Description

This module manages API keys required for external service interactions, ensuring secure and flexible access to various APIs.

### Key Functionalities

- **API Key Retrieval**: Implements functions to fetch API keys from either the session state or environment variables, prioritizing user-defined values.
- **Fallback Mechanism**: Provides a fallback to environment variables if keys are not present in the session state.

### Notable Implementations

- User-friendly approach to managing multiple API keys with clear separation based on API name.
- Conditional checks to warn users if an API key is missing.

---

## Running the Scraper

To run the scraper application across different operating systems (Windows, Linux, and macOS), follow the instructions below. Ensure that you have the necessary dependencies installed, such as Python and any required libraries.

### Prerequisites

1. **Python Installation**: Ensure that Python 3.7 or later is installed on your system. You can download it from the [official Python website](https://www.python.org/downloads/).
2. **Virtual Environment (Optional but Recommended)**:
   - It's advisable to create a virtual environment to manage dependencies. You can use `venv` for this.
   ```bash
   python -m venv venv
   source venv/bin/activate  # On macOS/Linux
   venv\Scripts\activate     # On Windows
   ```
3. **Install Required Libraries**: Install the necessary libraries by running the following command in your terminal:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Application

#### For Windows

1. Open Command Prompt.
2. Navigate to the project directory where `streamlit_app.py` is located:
   ```bash
   cd path\to\your\project
   ```
3. Run the Streamlit application:
   ```bash
   streamlit run streamlit_app.py
   ```

#### For Linux and macOS

1. Open a terminal.
2. Navigate to the project directory where `streamlit_app.py` is located:
   ```bash
   cd path/to/your/project
   ```
3. Run the Streamlit application:
   ```bash
   streamlit run streamlit_app.py
   ```

### Accessing the Application

Once the application is running, it will provide a local URL (usually `http://localhost:8501`) in the terminal. Open this URL in your web browser to access the Streamlit application and interact with the scraper.

### Notes

- Ensure that you have all API keys configured in the environment or session state as required by the application.
- If you encounter any permission issues or errors related to missing libraries, make sure your environment is correctly set up and that you have the necessary permissions to execute the scripts.

---

## Conclusion

This documentation provides a comprehensive overview of each file within the project. Each module plays a critical role in building a cohesive web scraping and data extraction application. Proper implementation of features like session management, API integration, and dynamic content handling enhances the overall functionality and user experience.
