# PlaywrightWebAutomationTesting

## What is Playwright?

Playwright is a powerful end-to-end testing framework developed by Microsoft that enables reliable testing of modern web applications. It allows you to automate interactions with web pages across multiple browsers including Chromium, Firefox, and WebKit (Safari).

### Key Features:
- **Cross-browser testing**: Run tests on Chromium, Firefox, and WebKit
- **Cross-platform**: Works on Windows, macOS, and Linux
- **Mobile testing**: Test mobile web apps with device emulation
- **Fast and reliable**: Parallel test execution and auto-wait for elements
- **Rich debugging**: Screenshots, videos, traces, and step-by-step debugging
- **Multiple languages**: Supports JavaScript, TypeScript, Python, Java, and .NET

## Project Structure

```
├── playwright.config.ts    # Playwright configuration file
├── tests/                  # Test files directory
│   └── example.spec.ts    # Sample test file
├── test-results/          # Test execution results
├── playwright-report/     # HTML test reports
└── package.json          # Node.js dependencies
```

## Prerequisites

- Node.js (version 16 or higher)
- npm or yarn package manager

## Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd PlaywrightWebAutomationTesting-
```

2. Install dependencies:
```bash
npm install
```

3. Install Playwright browsers:
```bash
npx playwright install
```

## How to Run Tests

### Running All Tests
```bash
# Run all tests
npx playwright test

# Run tests in headed mode (see browser)
npx playwright test --headed

# Run tests in a specific browser
npx playwright test --project=chromium
npx playwright test --project=firefox
npx playwright test --project=webkit
```

### Running Specific Tests
```bash
# Run a specific test file
npx playwright test tests/example.spec.ts

# Run a specific test by name
npx playwright test --grep "has title"
```

### Debug Mode
```bash
# Run tests in debug mode
npx playwright test --debug

# Run with UI mode for interactive testing
npx playwright test --ui
```

### Viewing Test Reports
```bash
# Open the HTML report
npx playwright show-report
```

## VS Code Integration

This project includes VS Code configuration for enhanced development experience:

1. **Install the Playwright Test extension** for VS Code
2. Use the Test Explorer panel to run individual tests
3. Set breakpoints and debug tests directly in VS Code

## Configuration

The `playwright.config.ts` file contains the main configuration:
- Test directory: `./tests`
- Browsers: Chromium, Firefox, WebKit
- Reporter: HTML reports
- Parallel execution enabled
- Trace collection on test failures

## Writing Tests

Tests are written using Playwright's test API. Here's a basic example:

```typescript
import { test, expect } from '@playwright/test';

test('example test', async ({ page }) => {
  await page.goto('https://example.com');
  await expect(page).toHaveTitle(/Example/);
  await page.click('button');
  await expect(page.locator('.result')).toBeVisible();
});
```

## Learning Resources

### Official Documentation
- [Playwright Documentation](https://playwright.dev/) - Official documentation
- [API Reference](https://playwright.dev/docs/api/class-playwright) - Complete API reference
- [Best Practices](https://playwright.dev/docs/best-practices) - Testing best practices

### Tutorials and Guides
- [Getting Started Guide](https://playwright.dev/docs/intro) - Step-by-step introduction
- [Writing Tests](https://playwright.dev/docs/writing-tests) - How to write effective tests
- [Locators Guide](https://playwright.dev/docs/locators) - Finding and interacting with elements
- [Assertions](https://playwright.dev/docs/test-assertions) - Available assertions for testing

### Video Resources
- [Playwright YouTube Channel](https://www.youtube.com/c/MicrosoftDeveloper/search?query=playwright) - Official videos
- [Test Automation University](https://testautomationu.applitools.com/playwright-tutorial/) - Free comprehensive course

### Community and Support
- [GitHub Repository](https://github.com/microsoft/playwright) - Source code and issues
- [Discord Community](https://discord.gg/playwright-807756831384403968) - Community support
- [Stack Overflow](https://stackoverflow.com/questions/tagged/playwright) - Q&A platform

### Advanced Topics
- [Page Object Model](https://playwright.dev/docs/pom) - Organizing test code
- [Test Fixtures](https://playwright.dev/docs/test-fixtures) - Reusable test setup
- [Visual Comparisons](https://playwright.dev/docs/test-screenshots) - Screenshot testing
- [Network Interception](https://playwright.dev/docs/network) - Mocking API calls
- [Authentication](https://playwright.dev/docs/auth) - Handling login flows

## Contributing

1. Fork the repository
2. Create a feature branch
3. Write tests for your changes
4. Ensure all tests pass
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.