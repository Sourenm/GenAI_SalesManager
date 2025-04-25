# Solve Business Problems with AI

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sourenm/GenAI_SalesManager/blob/main/Solve_Business_Problems_with_AI.ipynb)

This project demonstrates how to apply Generative AI—using OpenAI's GPT models and embeddings—to solve business problems like processing customer emails. The workflow integrates with Google Sheets to manage data and automates classification and response generation.

---

## Features

- **Automated Email Classification**  
  Classifies customer emails as *product inquiries* or *order requests* using GPT-4.

- **Semantic Product Matching**  
  Embeds product names and descriptions using `text-embedding-ada-002` to enable similarity-based processing.

- **Spreadsheet Integration**  
  Reads from and writes to Google Sheets dynamically, streamlining input/output handling.

- **Auto-Response Generation**  
  (Implied) Craft responses to classified emails and populate them into categorized output sheets.

---

## Input Format

The script expects a public Google Sheet with **two worksheets** named as follows:

### 1. `products`
Contains the product catalog with the following columns:

| Column        | Description                                |
|---------------|--------------------------------------------|
| `product_id`  | Unique identifier for each product         |
| `name`        | Name of the product                        |
| `category`    | Category under which the product falls     |
| `description` | A short description of the product         |
| `stock`       | Quantity available                         |
| `seasons`     | Applicable seasons (e.g., summer, winter)  |
| `price`       | Product price in your preferred currency   |

### 2. `emails`
Contains incoming customer emails with:

| Column      | Description                           |
|-------------|---------------------------------------|
| `email_id`  | Unique identifier for the email       |
| `subject`   | Subject line of the email             |
| `message`   | Body content of the email             |

---

## Output

A new Google Spreadsheet is created with the following tabs:

- `email-classification`: Contains `email_id` and `category` (`order request` or `product inquiry`)
- `order-status`: For structured order-related responses
- `order-response`: Plaintext responses to order-related queries
- `inquiry-response`: Plaintext responses to product inquiries

The link to this spreadsheet will be printed in the notebook output and shared publicly.

---

## Getting Started

1. **Open the Notebook in Google Colab**  
   [Solve_Business_Problems_with_AI.ipynb](https://colab.research.google.com/github/Sourenm/GenAI_SalesManager/blob/main/Solve_Business_Problems_with_AI.ipynb)

2. **Set Up Access**  
   - Authenticate your Google account when prompted
   - Insert your OpenAI API key and (optionally) base URL

3. **Run All Cells**  
   - The notebook will process the input data, classify emails, and generate responses.

---

## Dependencies

- `openai`
- `pandas`
- `numpy`
- `gspread`, `gspread_dataframe`
- `google-auth`
- `IPython.display`

---

## Author

**Sourena Naser Moghaddasi**  
Backend / GenAI / ML Engineer
[LinkedIn]([https://www.linkedin.com/in/sourenm](https://www.linkedin.com/in/sourena-naser-moghaddasi-2903b1a8/))

