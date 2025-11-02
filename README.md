# Parabank-QA-Automation-Project-Selenium-Python-
This project demonstrates automated testing using Selenium WebDriver and Python for a demo banking website, [Parabank](https://parabank.parasoft.com).    It is designed to showcase QA automation skills relevant to the Quality Assurance Engineer or Analyst role.

The Project Includes:
Writing and maintaining Selenium test scripts.
Using Page Object Model (POM) for clean test architecture.
Implementing waits, assertions, and validations.
Running tests with **pytest** and generating reports.
Configurable browser setup (Chrome, headless mode).

Automated Test: Open New Account
1. Open the Parabank website.  
2. Log in using test credentials.  
3. Navigate to "Open New Account" page.  
4. Open a new account using default options.  
5. Validate success message.  
6. Logout from the application.

Key Skills Demonstrated:

- Selenium WebDriver automation
- Python programming
- Test structuring with Pytest
- Page Object Model design pattern
- Assertions and validation checks
- Headless Chrome support

Configuration
Create and activate a virtual environment:
python -m venv .venv
Windows: .\.venv\Scripts\activate
macOS / Linux: source .venv/bin/activate

Install dependencies
pip install -r requirements.txt

Configure test credentials
Edit utils/config.py and set:
TEST_USERNAME = "skylark" #python code -- mine credential demo
TEST_PASSWORD = "Pera.sr.pass.007" #python code -- mine credential demo
HEADLESS = False  # True for headless mode # python code
You can manually register a user on Parabank
 if default credentials don’t work.

Run in normal mode
pytest -q

------------------------------------------

How It Works

Page Object Model separates locators and page actions from tests.

Browser Setup: utils/browser_setup.py uses webdriver-manager to automatically install the correct ChromeDriver.

Test Flow:

LoginPage logs in.

HomePage navigates to “Open New Account.”

OpenAccountPage opens a new account and validates the success message.

Assertions are flexible to handle dynamic success text (case-insensitive match).

Future Enhancements:

Add more tests for account transactions, transfers, and bill payments.

Implement data-driven testing with CSV/Excel.

Integrate with CI/CD pipelines (GitHub Actions) for automated execution.

Add screenshot capture on test failure for reporting.

Extend to cross-browser testing (Firefox, Edge).

References

Selenium Documentation

Pytest Documentation

Parabank Demo Site

- Debugging with prints and waits

