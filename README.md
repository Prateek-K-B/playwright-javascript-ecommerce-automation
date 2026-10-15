# 🧪 SauceDemo Playwright Automation Testing Project

An end-to-end test automation project built using **Playwright and JavaScript** to validate the complete shopping journey on [SauceDemo](https://www.saucedemo.com/), a demo e-commerce application.

The project covers login validation, product inventory, sorting, shopping cart operations, checkout workflows, and order completion.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Playwright | Browser automation and end-to-end testing |
| JavaScript | Test scripting |
| Node.js | JavaScript runtime |
| Playwright Test | Test execution and assertions |
| HTML Reporter | Test result reporting |
| Git and GitHub | Version control and project hosting |

## 📁 Project Structure

```text
playwright-javascript-ecommerce-automation/
├── tests/
│   ├── 01_login.spec.js
│   ├── 02_inventory.spec.js
│   ├── 03_cart.spec.js
│   └── 04_checkout.spec.js
├── .gitignore
├── package.json
├── package-lock.json
├── playwright.config.js
└── README.md
```

## 🌐 Application Under Test

**Application:** [https://www.saucedemo.com/](https://www.saucedemo.com/)

The application is used to test the following workflows:

- User login and authentication validation
- Product inventory and product sorting
- Shopping cart operations
- Checkout form validation
- Order review and price verification
- Order completion and confirmation

### Demo Test Credentials

The tests use the publicly provided SauceDemo test accounts.

| Username | Password | Scenario |
|---|---|---|
| `standard_user` | `secret_sauce` | Successful login and shopping workflows |
| `locked_out_user` | `secret_sauce` | Locked-out user validation |

These are public demo credentials, not personal account credentials.

## ✅ Test Coverage

### 1. Login Tests

**File:** `tests/01_login.spec.js`

| Test Case | Expected Result |
|---|---|
| Valid login | User is redirected to the inventory page |
| Invalid password | Appropriate error message is displayed |
| Empty username and password | Username validation error is displayed |
| Locked-out user | Locked-out error message is displayed |

### 2. Inventory Tests

**File:** `tests/02_inventory.spec.js`

| Test Case | Expected Result |
|---|---|
| Verify product count | Six products are displayed |
| Sort products A to Z | Products are sorted alphabetically |
| Sort products Z to A | Products are sorted in reverse alphabetical order |
| Sort prices low to high | Lowest-priced product appears first |
| Sort prices high to low | Highest-priced product appears first |
| Open a product | Product details are displayed |
| Verify product prices | All six products have prices |
| Verify Add to Cart buttons | All six products have Add to Cart buttons |

### 3. Shopping Cart Tests

**File:** `tests/03_cart.spec.js`

| Test Case | Expected Result |
|---|---|
| Add one product | Cart badge displays one item |
| Add two products | Cart badge displays two items |
| Add all products | Cart badge displays six items |
| Remove a product | Cart badge updates appropriately |
| Open shopping cart | Cart page is displayed |
| Verify product name | Correct product name is displayed |
| Verify product price | Correct product price is displayed |
| Remove product from cart | Selected product is removed |
| Continue shopping | User returns to inventory |
| Proceed to checkout | Checkout information page opens |

### 4. Checkout Tests

**File:** `tests/04_checkout.spec.js`

#### Checkout Information

| Test Case | Expected Result |
|---|---|
| Open checkout form | Checkout information page is displayed |
| Submit an empty form | First Name validation error appears |
| Submit without last name | Last Name validation error appears |
| Submit without postal code | Postal Code validation error appears |
| Enter all required information | User proceeds to order review |
| Click Cancel | User returns to the cart |

#### Order Review

| Test Case | Expected Result |
|---|---|
| Verify order review URL | Correct checkout URL is displayed |
| Verify product name | Correct product name is displayed |
| Verify product price | Correct product price is displayed |
| Verify subtotal | Subtotal is displayed |
| Verify tax | Tax amount is displayed |
| Verify total | Final order total is displayed |
| Click Cancel | User returns to inventory |
| Click Finish | Order confirmation page opens |

#### Order Completion

| Test Case | Expected Result |
|---|---|
| Verify confirmation URL | Checkout completion page is displayed |
| Verify success message | Order confirmation message appears |
| Verify confirmation image | Confirmation image is visible |
| Click Back Home | User returns to inventory |
| Verify empty cart | Cart badge is no longer displayed |

## 📊 Test Execution Summary

The following results were obtained during local Chromium test execution.

| Test File | Tests Passed |
|---|---:|
| `01_login.spec.js` | 4 |
| `02_inventory.spec.js` | 8 |
| `03_cart.spec.js` | 10 |
| `04_checkout.spec.js` | 19 |
| **Total** | **41** |

**Local execution result: 41 tests passed in Chromium.**

These results describe the local test run and do not imply that GitHub Actions has passed.

## ⚙️ Setup and Installation

### Prerequisites

- Node.js 18 or above
- npm
- Git
- PyCharm or Visual Studio Code

### Installation Steps

Clone the repository:

```bash
git clone https://github.com/Prateek-K-B/playwright-javascript-ecommerce-automation.git
```

Navigate to the project directory:

```bash
cd playwright-javascript-ecommerce-automation
```

Install dependencies:

```bash
npm ci
```

Install the Chromium browser required by Playwright:

```bash
npx playwright install chromium
```

## ▶️ Running the Tests

### Run all tests in Chromium

```bash
npx playwright test --project=chromium
```

### Run tests with the browser visible

```bash
npx playwright test --headed --project=chromium
```

### Run individual test files

Login tests:

```bash
npx playwright test tests/01_login.spec.js --project=chromium
```

Inventory tests:

```bash
npx playwright test tests/02_inventory.spec.js --project=chromium
```

Shopping cart tests:

```bash
npx playwright test tests/03_cart.spec.js --project=chromium
```

Checkout tests:

```bash
npx playwright test tests/04_checkout.spec.js --project=chromium
```

### View the HTML report

```bash
npx playwright show-report
```

The report provides a detailed breakdown of test execution, including passed and failed tests and execution times. Screenshots and traces are available when generated by the configured test runner.

## 🧠 Key Concepts Demonstrated

| Concept | Purpose |
|---|---|
| `test.describe()` | Groups related test cases |
| `test.beforeEach()` | Executes setup steps before each test |
| `page.goto()` | Navigates to a webpage |
| `page.fill()` | Enters text into input fields |
| `page.click()` | Clicks page elements |
| `expect().toHaveURL()` | Verifies the current URL |
| `expect().toHaveText()` | Validates element text |
| `expect().toBeVisible()` | Checks element visibility |
| `expect().toHaveCount()` | Verifies the number of matching elements |
| CSS selectors | Locate elements using CSS patterns |
| `.first()` | Selects the first matching element |
| Reusable helper functions | Reduce duplicated code |

## 👨‍💻 Author

**Prateek K B**

- GitHub: [Prateek-K-B](https://github.com/Prateek-K-B)
- LinkedIn: [Prateek Byadgi](https://www.linkedin.com/in/prateekbyadgi/)

## 📄 License

This project is based on an existing open-source project. Please check the original repository's license and comply with its attribution and redistribution requirements before redistributing modified code.
