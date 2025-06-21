# NZ First Home Buyer Loan Calculator

A comprehensive web-based calculator to help New Zealand first-time home buyers estimate their maximum loan amount and understand bank lending criteria.

## 🏠 Overview

This tool provides real-time calculations based on the three main criteria New Zealand banks use to assess home loan applications:
- **Debt-to-Income (DTI) limits** - RBNZ regulations on income multiples
- **Loan-to-Value Ratio (LVR)** - Maximum 90% for first home buyers
- **Serviceability testing** - Stress testing at higher interest rates

## ✨ Features

- **Real-time calculations** - Results update as you adjust inputs
- **Comprehensive tooltips** - Hover over "?" icons for detailed explanations
- **Stress testing** - Tests affordability at rates 2.5% above current
- **Visual indicators** - Clear pass/fail status with color coding
- **Mobile responsive** - Works on all devices
- **No dependencies** - Pure HTML/CSS/JavaScript

## 🚀 Quick Start

1. **Download the file**
   ```bash
   git clone https://github.com/yourusername/nz-home-loan-calculator.git
   cd nz-home-loan-calculator
   ```

2. **Open in browser**
   ```bash
   # Simply open the HTML file in any modern web browser
   open index.html
   ```

3. **Or serve locally**
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   ```

## 📊 How It Works

### Input Parameters
- **Gross Annual Income** - Your total pre-tax income
- **Available Deposit** - Cash available for property purchase
- **Target Property Value** - Price of property you want to buy
- **Existing Debts** - Monthly payments on current debts
- **Living Expenses** - Monthly living costs
- **Interest Rate** - Current mortgage rates
- **DTI Limit** - Regulatory debt-to-income multiple

### Calculations

The calculator determines your maximum loan using three criteria:

1. **DTI Assessment**
   ```
   Maximum Loan = Annual Income × DTI Multiple
   ```

2. **LVR Assessment**
   ```
   Maximum Loan = Property Value × 0.90
   ```

3. **Serviceability Assessment**
   ```
   Monthly Capacity = Income - Debts - Expenses
   Stress Test = Payment at (Current Rate + 2.5%)
   Maximum Loan = Based on payment capacity
   ```

Your actual maximum is the **lowest** of these three amounts.

## 🎯 Key Metrics Explained

| Metric | Description | First Home Buyer Limit |
|--------|-------------|------------------------|
| **LVR** | Loan ÷ Property Value | 90% maximum |
| **DTI** | Total Debt ÷ Annual Income | 6-7x typically |
| **Serviceability** | Can you afford payments? | Stress tested +2.5% |

## 🔧 Customization

### Modifying DTI Limits
```javascript
// In the HTML, update the select options
<select id="dtiLimit">
    <option value="6">6x Income</option>
    <option value="6.5">6.5x Income</option>
    <option value="7">7x Income</option>
    <option value="8">8x Income</option> <!-- Add new option -->
</select>
```

### Adjusting Stress Test Rate
```javascript
// Change the stress test margin (currently +2.5%)
const stressTestRate = interestRate + 3.0; // Increase to +3.0%
```

### Styling
The CSS uses CSS custom properties for easy theming:
```css
:root {
    --primary-color: #3498db;
    --success-color: #27ae60;
    --warning-color: #e74c3c;
}
```

## 📱 Browser Support

- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- ✅ Mobile browsers

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Keep the tool simple and focused
- Maintain mobile responsiveness
- Add tooltips for new features
- Test calculations thoroughly
- Follow existing code style

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Important Disclaimer

**This calculator is for estimation purposes only and does not constitute financial advice.**

- Results are indicative only and may not reflect actual bank decisions
- Banks have individual lending criteria and may assess applications differently
- Interest rates and regulations change frequently
- Always consult with qualified mortgage advisors and banks for official pre-approval
- The calculator assumes a 30-year mortgage term

## 🏦 NZ Banking Context

This calculator is designed specifically for the New Zealand property market and incorporates:

- **RBNZ LVR restrictions** - 90% maximum for first home buyers
- **Proposed DTI limits** - 6-7x income multiples
- **Stress testing requirements** - Standard bank practices
- **First Home Buyer schemes** - Relevant deposit requirements

## 📞 Support

- 🐛 **Bug reports**: [Open an issue](https://github.com/yourusername/nz-home-loan-calculator/issues)
- 💡 **Feature requests**: [Start a discussion](https://github.com/yourusername/nz-home-loan-calculator/discussions)
- 📧 **Contact**: your.email@example.com

## 🎉 Acknowledgments

- Reserve