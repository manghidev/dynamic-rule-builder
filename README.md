# Dynamic Rule Builder

A visual tool for creating, testing, and exporting complex business logic rules with an intuitive interface.

## 🌟 Features

- **Visual Rule Builder**: Create complex logical conditions using an intuitive interface
- **Multi-language Support**: Available in English (US) and Spanish (Mexico)
- **Real-time Testing**: Test your rules with custom variables and see immediate results
- **JSON Export**: Export your rules as structured JSON for integration with other systems
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Dynamic Variables**: Define and manage custom variables with different data types
- **Nested Logic Groups**: Create complex rule hierarchies with AND/OR conditions
- **Auto-detection**: Automatically detects and handles strings, numbers, and booleans

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- No installation required - runs entirely in the browser

### Usage

1. Open `index.html` in your web browser
2. The application will load with default example variables
3. Start building your logic rules using the interface

## 📖 How to Use

### Step 1: Define Your Variables

1. In the **"Define Your Variables"** section, click **"+ Add Variable"**
2. Enter a variable name (e.g., `user_age`, `country_code`)
3. Enter a test value (supports strings, numbers, and booleans)
4. Variables will automatically appear in the rule builder

### Step 2: Build Your Logic

1. In the **"Build Your Logic"** section, choose between:
   - **ALL**: All conditions must be met (AND logic)
   - **ANY**: Any condition can be met (OR logic)

2. Click **"Add Rule"** to create a new condition:
   - Select a variable from the dropdown
   - Choose an operator (equals, not equals, greater than, etc.)
   - Enter a comparison value

3. Click **"Add Group"** to create nested logic groups for complex rules

### Step 3: Test and Export

1. Click **"Evaluate and Generate JSON"** to test your rules
2. See the result (VALID/INVALID) based on your test data
3. Copy the generated JSON structure for use in your applications

## 🔧 Supported Operators

| Operator | Symbol | Description |
|----------|--------|-------------|
| Equals | `==` | Value is equal to |
| Not Equals | `!=` | Value is not equal to |
| Greater Than | `>` | Value is greater than |
| Greater or Equal | `>=` | Value is greater than or equal to |
| Less Than | `<` | Value is less than |
| Less or Equal | `<=` | Value is less than or equal to |

## 📊 Data Types

The application automatically detects and handles:
- **Strings**: Text values (e.g., "US", "active")
- **Numbers**: Integer and decimal values (e.g., 25, 18.5)
- **Booleans**: True/false values (e.g., true, false)

## 📋 JSON Output Format

The generated JSON follows this structure:

```json
{
  "condition": "AND",
  "rules": [
    {
      "variable": "user_age",
      "operator": ">=",
      "value": 18
    },
    {
      "variable": "country_code",
      "operator": "==",
      "value": "US"
    },
    {
      "condition": "OR",
      "rules": [
        {
          "variable": "is_active",
          "operator": "==",
          "value": true
        }
      ]
    }
  ]
}
```

## 🎉 Examples

### Example 1: Age Verification

**Variables:**
- `user_age`: 25
- `country_code`: "US"

**Rule:**
- user_age >= 18 AND country_code == "US"

**Result:** VALID ✅

### Example 2: User Segmentation

**Variables:**
- `is_premium`: true
- `login_count`: 50
- `country_code`: "MX"

**Rule:**
- (is_premium == true OR login_count > 30) AND country_code == "MX"

**Result:** VALID ✅

### Example 3: Complex Business Logic

**Variables:**
- `subscription_tier`: "gold"
- `account_age_days`: 120
- `last_login_days`: 7
- `has_payment_method`: true

**Rule:**
- (subscription_tier == "gold" OR account_age_days > 90) AND (last_login_days <= 30 AND has_payment_method == true)

**Result:** VALID ✅

## 🎯 Use Cases

Perfect for:
- **Business Rules Engines**: Define complex business logic
- **Form Validation**: Create dynamic validation rules
- **User Segmentation**: Define user groups based on criteria
- **A/B Testing**: Set up test conditions
- **Access Control**: Define permission rules
- **Marketing Campaigns**: Target specific user segments

## 🎨 Technologies Used

- **HTML5**: Semantic markup
- **CSS3**: Styling with animations and responsive design
- **JavaScript (ES6+)**: Application logic and DOM manipulation
- **Tailwind CSS**: Utility-first CSS framework via CDN
- **Heroicons**: Beautiful SVG icons

## 🌍 Language Support

- **English (US)**: Default language
- **Spanish (Mexico)**: Full translation available

Switch languages using the language selector at the bottom of the page.

## 🛠️ Development

### File Structure

```
project/
├── index.html          # Main application file
├── README.md          # This documentation
└── (no build process required)
```

### Key Components

1. **Translation System**: Multi-language support with `translations` object
2. **Rule Builder**: Dynamic DOM manipulation for rule creation
3. **Variable Manager**: Real-time variable synchronization
4. **Evaluation Engine**: Logic processing and result calculation
5. **JSON Generator**: Export functionality for integration

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes following the code style
4. Commit your changes using **semantic commit messages**:
   - `feat: add new rule operator support`
   - `fix: resolve variable selector bug`
   - `docs: update README examples`
   - `style: improve button hover animations`
   - `refactor: optimize rule evaluation logic`
   - `test: add validation for edge cases`
   - `chore: update dependencies`
5. Push to the branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request with a clear description

## 🆘 Support

If you encounter any issues or have questions:
1. Check the documentation above
2. Review the code comments in `index.html`
3. Create an issue in the repository

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

**Built with ❤️ for developers who need powerful rule engines without the complexity.**