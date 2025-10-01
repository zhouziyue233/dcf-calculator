[DCF_README.md](https://github.com/user-attachments/files/22633207/DCF_README.md)
# 📊 DCF Valuation Calculator

An interactive web-based tool for conducting Discounted Cash Flow (DCF) analysis on publicly listed companies.

## Features

✨ **Comprehensive DCF Analysis**
- Free Cash Flow (FCF) projections
- Terminal value calculation using perpetuity growth method
- Enterprise value to equity value conversion
- Intrinsic value per share calculation

📈 **Advanced Financial Modeling**
- Customizable projection periods (1-10 years)
- WACC/discount rate calculations
- CAPM-based cost of equity calculator
- Net debt adjustments

🎨 **Modern User Interface**
- Clean, professional design
- Responsive layout for all devices
- Real-time calculations
- Visual results presentation

## How to Use

### 1. Open the Calculator
Simply open `dcf-calculator.html` in any modern web browser (Chrome, Firefox, Safari, Edge).

### 2. Enter Company Information
- **Company Name/Ticker**: Enter the company you're analyzing (e.g., "Apple Inc. (AAPL)")
- **Shares Outstanding**: Total number of shares in millions (find in company's financial statements)
- **Current Stock Price**: Current market price for comparison

### 3. Input Cash Flow Projections
- **Current Year FCF**: Most recent annual free cash flow in millions
  - Formula: Operating Cash Flow - Capital Expenditures
  - Find in the company's Cash Flow Statement
- **Growth Rate**: Expected annual FCF growth rate (%)
- **Projection Period**: Number of years to project (typically 5-10 years)

### 4. Set Valuation Parameters
- **Discount Rate (WACC)**: Weighted Average Cost of Capital (%)
  - Represents the required rate of return
  - Typically 8-12% for most companies
- **Terminal Growth Rate**: Perpetual growth rate after projection period (%)
  - Usually 2-3% (GDP growth rate)
  - Must be lower than discount rate
- **Net Debt**: Total Debt minus Cash & Cash Equivalents (in millions)

### 5. Advanced Options (Optional)
Click "Show Advanced Options" to calculate WACC using CAPM:
- **Risk-Free Rate**: Typically 10-year Treasury yield (%)
- **Market Risk Premium**: Expected market return - risk-free rate (typically 5-7%)
- **Beta**: Stock's volatility relative to market (find on financial websites)
- Click "Calculate WACC from CAPM" to auto-populate discount rate

### 6. Calculate & Analyze
- Click "🚀 Calculate Intrinsic Value"
- Review the results:
  - **Intrinsic Value Per Share**: Estimated fair value
  - **Upside/Downside**: Comparison with current price
  - **Cash Flow Projections**: Year-by-year breakdown
  - **Terminal Value**: Long-term value calculation

## Understanding the Results

### Valuation Indicators
- ✅ **Undervalued**: Intrinsic value > Current price (positive upside)
- ⚠️ **Overvalued**: Intrinsic value < Current price (negative upside)

### Key Metrics Explained
- **Enterprise Value**: Total value of the business (debt + equity)
- **Equity Value**: Value belonging to shareholders (EV - Net Debt)
- **Intrinsic Value Per Share**: Equity Value / Shares Outstanding
- **PV (Present Value)**: Future cash flows discounted to today's value

## Example: Valuing a Tech Company

```
Company Information:
- Company: Tech Corp (TECH)
- Shares Outstanding: 1,000 million
- Current Stock Price: $100

Cash Flow Projections:
- Current Year FCF: $5,000 million
- Growth Rate: 8%
- Projection Period: 5 years

Valuation Parameters:
- Discount Rate (WACC): 10%
- Terminal Growth Rate: 2.5%
- Net Debt: $2,000 million
```

**Calculation Steps:**
1. Project FCF for 5 years at 8% growth
2. Calculate present value of each year's FCF
3. Calculate terminal value at year 5
4. Sum all present values = Enterprise Value
5. Subtract net debt = Equity Value
6. Divide by shares = Intrinsic Value Per Share

## Tips for Accurate Analysis

### 1. Finding Financial Data
- **FCF**: Company's Cash Flow Statement
- **Shares Outstanding**: Balance Sheet or company filings
- **Beta**: Yahoo Finance, Bloomberg, or financial data providers
- **Net Debt**: Balance Sheet (Total Debt - Cash)

### 2. Setting Growth Rates
- Historical FCF growth (last 3-5 years)
- Industry growth rates
- Company guidance
- Analyst estimates
- Be conservative - overly optimistic growth leads to overvaluation

### 3. Choosing Discount Rate
- Higher risk companies = higher discount rate
- Use CAPM for cost of equity
- Adjust for company-specific risks
- Typical ranges: 8-15%

### 4. Terminal Growth Rate
- Should not exceed GDP growth (2-3%)
- Reflects steady-state growth
- Lower is more conservative

### 5. Sensitivity Analysis
- Test different growth rates
- Adjust discount rates
- Compare scenarios
- Consider best/base/worst cases

## Important Disclaimers

⚠️ **Investment Warning**
- This tool is for educational and analytical purposes only
- DCF models are based on assumptions and projections
- Not financial advice - always do comprehensive research
- Consult with financial professionals before making investment decisions

📊 **Model Limitations**
- Accuracy depends on input quality
- Future projections are uncertain
- Does not account for all risk factors
- Should be used alongside other valuation methods (P/E, P/B, comparable companies)

## Technical Requirements

- Modern web browser (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+)
- JavaScript enabled
- No installation or internet connection required (runs locally)

## Formulas Used

### Free Cash Flow Projection
```
FCF(year n) = FCF(year n-1) × (1 + growth rate)
```

### Present Value of FCF
```
PV of FCF = FCF / (1 + discount rate)^year
```

### Terminal Value (Perpetuity Growth Method)
```
Terminal Value = FCF(final year) × (1 + terminal growth) / (discount rate - terminal growth)
```

### Intrinsic Value Per Share
```
Enterprise Value = Σ(PV of projected FCF) + PV of Terminal Value
Equity Value = Enterprise Value - Net Debt
Intrinsic Value = Equity Value / Shares Outstanding
```

### CAPM (Capital Asset Pricing Model)
```
Cost of Equity = Risk-Free Rate + Beta × Market Risk Premium
```

## File Structure

```
dcf-calculator.html    # Main application (all-in-one file)
DCF_README.md         # This documentation
```

## Support

For questions or issues:
1. Review this documentation
2. Check input values for accuracy
3. Ensure discount rate > terminal growth rate
4. Verify all required fields are filled

---

**Version**: 1.0  
**Created**: October 2025  
**License**: Free to use for personal and educational purposes

Happy Investing! 📈
