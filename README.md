# Bitfinex Funding Earnings Connector for Looker Studio

This connector allows you to fetch and visualize your **Funding Earnings** data from the Bitfinex API in Looker Studio. Use it to analyze your daily and total earnings over customizable date ranges.

---

## Features

- **Retrieve Funding Earnings** directly from the Bitfinex API.
- **Dynamic Date Filtering** for customized time ranges.
- **Metrics and Dimensions**:
  - `Date`: The date of the earnings (YYYY-MM-DD).
  - `Currency`: The currency in which the earnings were made.
  - `Funding Earnings`: The total earnings for each day.

---

## Requirements

1. **Bitfinex API Credentials**:
   - Log in to your Bitfinex account and generate an API key with the following permissions:
     - `Read Funding`
     - `Read Wallets`
2. **Access to Looker Studio**:
   - You need a Google account to use Looker Studio.
3. Permissions to deploy and manage custom connectors in Google Apps Script.

---

## Setup Instructions

### Step 1: Clone this Repository

```bash
git clone https://github.com/your-repo/bitfinex-funding-earnings.git
```

### Step 2: Open the Code in Google Apps Script

1. Go to [Google Apps Script](https://script.google.com/).
2. Create a new project:
   - Click **Start a new project** and select **Editor**.
3. Copy the contents of the `main.gs` file from this repository.
   - Paste the code into the Apps Script editor, replacing any existing code.
4. Save the project:
   - Click **File > Save** and name the project, for example, `Bitfinex Funding Earnings`.

---

### Step 3: Deploy the Connector

1. In the Apps Script editor, click on **Deploy > New Deployment**.
2. Select **Google Data Studio Connector** as the deployment type.
3. Configure the deployment:
   - **Version Description**: Provide a short description, e.g., `Initial deployment`.
   - **OAuth Scopes**: Ensure the following scope is added:
     - `https://www.googleapis.com/auth/script.external_request`
4. Click **Deploy** and copy the **Deployment ID**.

---

### Step 4: Add the Connector to Looker Studio

1. Open [Looker Studio](https://lookerstudio.google.com/).
2. Go to **Create > Data Source**.
3. Select **Build Your Own Connector**.
4. Paste the **Deployment ID** from Apps Script and click **Next**.
5. Authenticate using your Bitfinex API credentials:
   - Enter your **API Key** and **API Secret**.
6. Click **Connect** to finalize the connection.

---

### Step 5: Visualize Your Data

1. After connecting the data source, link it to a Looker Studio report.
2. Add visualizations such as charts or tables to analyze your **Funding Earnings**.
3. Use filters and date selectors to customize the data view.
   - For example, filter earnings by specific date ranges or currencies.

---

## 🛠 Configuration Options

### Metrics and Dimensions Available

- **Date**: The date of the earnings (YYYY-MM-DD).
- **Currency**: The currency in which the earnings were made (e.g., USD, EUR).
- **Funding Earnings**: The total earnings for the day.

### Dynamic Filters

- **Date Range**: Use Looker Studio’s date filter to analyze specific periods.
- **Currency Filter**: Focus on earnings for a specific currency.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.