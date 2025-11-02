# Parabank QA Automation Project Selenium Python
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


<img width="1337" height="837" alt="user configuration" src="https://github.com/user-attachments/assets/6a9710f1-c527-49b9-bad4-f8f9d79ca9dc" />
<img width="1447" height="843" alt="open account" src="https://github.com/user-attachments/assets/142a9dbf-36ab-43be-8b8c-425b50716da4" />
<img width="1357" height="852" alt="Login" src="https://github.com/user-attachments/assets/0cbfbf7c-d467-4ee5-b6ca-1202153a7bfa" />
<img width="1217" height="828" alt="homepage" src="https://github.com/user-attachments/assets/f1b81be0-3227-4216-bf64-d5d81c358dd7" />
<img width="1441" height="847" alt="browser setup" src="https://github.com/user-attachments/assets/aaa9120b-2636-4232-8091-b049fcf717ce" />

