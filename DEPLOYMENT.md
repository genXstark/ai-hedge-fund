# Deployment Guide

## GitHub Pages Deployment

This repository includes a GitHub Actions workflow that automatically deploys the frontend application to GitHub Pages.

### Setup Instructions

1. **Enable GitHub Pages in Repository Settings:**
   - Go to your repository on GitHub
   - Navigate to **Settings** → **Pages**
   - Under "Build and deployment":
     - Source: Select **GitHub Actions**
   - Save the settings

2. **Trigger Deployment:**
   The deployment will automatically trigger on:
   - Any push to the `main` branch
   - Manual workflow dispatch from the Actions tab

3. **Access the Deployed Site:**
   Once deployed, your site will be available at:
   ```
   https://[your-username].github.io/ai-hedge-fund/
   ```

### Local Development

To run the frontend locally:

```bash
cd app/frontend
npm install
npm run dev
```

The application will be available at `http://localhost:5173`

### Build Configuration

The build process is configured in `.github/workflows/deploy-pages.yml` and uses:
- Node.js 20
- Vite for building
- GitHub Pages for hosting

The `vite.config.ts` is configured to automatically adjust the base path when building for GitHub Pages using the `GITHUB_PAGES` environment variable.

## Important Notes

### Educational Purpose Only

**⚠️ CRITICAL DISCLAIMER ⚠️**

This AI Hedge Fund application is designed for **EDUCATIONAL AND RESEARCH PURPOSES ONLY**:

- ❌ **NOT for real trading or investment**
- ❌ **NOT a financial advice tool**
- ❌ **Does NOT execute real trades**
- ❌ **Does NOT support cryptocurrency trading**
- ❌ **Does NOT support leveraged trading**
- ❌ **Cannot and will not guarantee any profits**

### What This System Does

✅ Simulates trading decisions using AI agents
✅ Analyzes stock market data (AAPL, GOOGL, MSFT, NVDA, TSLA, etc.)
✅ Demonstrates AI decision-making processes
✅ Provides educational insights into algorithmic trading concepts
✅ Allows backtesting of trading strategies

### What This System Does NOT Do

❌ Execute real trades on any exchange
❌ Connect to real trading accounts
❌ Handle real money or cryptocurrency
❌ Provide investment advice
❌ Guarantee any level of profit

### Risk Warning

**Trading and investing involve substantial risk of loss.**

- Past performance does not indicate future results
- AI predictions are not guaranteed to be accurate
- No trading system can guarantee profits
- Always consult with a licensed financial advisor before making investment decisions
- Never invest more than you can afford to lose

### Liability Disclaimer

The creators and contributors of this project:
- Assume NO liability for any financial losses
- Provide NO warranties or guarantees
- Are NOT responsible for any trading decisions made based on this tool
- Recommend consulting professional financial advisors for investment decisions

By using this software, you acknowledge that:
1. You understand it is for educational purposes only
2. You will not use it for real trading without proper expertise and risk management
3. You accept full responsibility for any decisions you make
4. You have read and understood all disclaimers

## Technical Support

For technical issues with the deployment:
1. Check the Actions tab for build logs
2. Ensure all dependencies are correctly specified
3. Verify the GitHub Pages settings are correct

For questions about the project, please open an issue on GitHub.

## Contributing

Contributions are welcome! Please:
1. Read the main README.md
2. Follow the existing code style
3. Keep pull requests focused and small
4. Ensure all builds pass before submitting

## License

This project is licensed under the MIT License. See LICENSE file for details.
