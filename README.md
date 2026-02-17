# Covoro Demo Automation

This is a Playwright-based automation project for testing the Covoro platform.

## Project Structure

```
.
├── .github/                # GitHub Actions workflows
│   └── workflows/
├── node_modules/           # Project dependencies
├── pages/                  # Page Object Model files
│   ├── dashboard.page.ts
│   ├── FinalSubmitInvoice.page.ts
│   ├── FinalSubmitInvoiceAlternate.page.ts
│   ├── invoice.page.ts
│   └── login.page.ts
├── playwright-report/      # HTML test reports
├── test-results/           # Test execution results (JSON)
├── tests/                  # Test suites
│   └── uae-regression-test-suite.spec.ts
├── utilities/              # Utility scripts
│   └── parse-report.js
├── .gitignore              # Git ignore file
├── Dockerfile              # Docker configuration
├── package.json            # Project metadata and dependencies
├── package-lock.json       # Exact dependency versions
└── playwright.config.ts    # Playwright configuration
```

### Key Components

*   **`pages/`**: This directory contains the Page Object Models (POMs) for the application. Each file corresponds to a page in the application and encapsulates the selectors and actions for that page.
*   **`tests/`**: This directory contains the test suites. The tests use the POMs from the `pages/` directory to interact with the application and perform assertions.
*   **`playwright.config.ts`**: This is the main configuration file for Playwright. It defines the test directory, reporters, browsers, and other settings.
*   **`package.json`**: This file lists the project's dependencies and defines scripts for running tasks.

## Getting Started

### Prerequisites

*   [Node.js](https://nodejs.org/) (v18 or higher)
*   npm (comes with Node.js)

### Installation

1.  Clone the repository:
    ```bash
    git clone <repository-url>
    ```
2.  Navigate to the project directory:
    ```bash
    cd covoro-demo-automation
    ```
3.  Install the dependencies:
    ```bash
    npm install
    ```
4.  Create a `.env` file in the root of the project and add the following environment variables:
    ```
    DEMO_USERNAME=<your-username>
    DEMO_PASSWORD=<your-password>
    ```

## Running Tests

To run the tests, use the following command:

```bash
npm test
```

This will run all the tests in the `tests/` directory.

### Running a specific test file

To run a specific test file, you can pass the file path as an argument:

```bash
npm test -- tests/uae-regression-test-suite.spec.ts
```

## Viewing Reports

After running the tests, an HTML report will be generated in the `playwright-report/` directory. You can open the `index.html` file in your browser to view the report.

```bash
npx playwright show-report
```
