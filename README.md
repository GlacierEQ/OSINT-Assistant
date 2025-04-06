# OSINT Assistant

An AI-enhanced OSINT (Open Source Intelligence) tool for gathering, analyzing, and reporting on information from various web sources. This tool leverages the power of Perplexity AI to provide deeper insights and more accurate analysis.

## Features

- 🔍 **Web Search:** Collect information from multiple sources based on specific queries
- 🧠 **AI-Powered Analysis:** Use Perplexity AI for enhanced content analysis
- 📊 **Entity Recognition:** Identify key people, organizations, and concepts from collected data
- 🔗 **Connection Analysis:** Map relationships between identified entities
- 📈 **Pattern Recognition:** Identify trends and patterns in the collected data
- 📝 **Comprehensive Reporting:** Generate structured reports with visualizations and actionable insights
- 📤 **Data Export:** Save results in JSON format with proper serialization using Pydantic

## Installation

### Prerequisites

- Python 3.8+
- pip package manager

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/AXRoux/OSINT-Assistant.git
   cd osint-assistant
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your environment variables:
   ```bash
   cp .env.example .env
   ```
   
4. Edit the `.env` file and add your Perplexity API key:
   ```
   PERPLEXITY_API_KEY=your_api_key_here
   ```

## Usage

### Basic Usage

Run a search query:
```bash
python osint_assistant.py --query "quantum computing advances"
```

### Advanced Options

Save the results to a file:
```bash
python osint_assistant.py --query "quantum computing advances" --save
```

Specify the number of results to collect:
```bash
python osint_assistant.py --query "quantum computing advances" --results 15
```

Output results as JSON:
```bash
python osint_assistant.py --query "quantum computing advances" --json
```

Override the API key from environment file:
```bash
python osint_assistant.py --query "quantum computing advances" --api-key "your-api-key"
```

### Command Line Arguments

| Argument | Short | Description |
|----------|-------|-------------|
| `--query` | `-q` | The search query to investigate |
| `--results` | `-r` | Number of results to collect (default: 10) |
| `--save` | `-s` | Save the collected data to a file |
| `--api-key` | `-k` | Perplexity API key (overrides .env file) |
| `--json` | `-j` | Output results as JSON |

## API Key Setup

This tool uses the Perplexity AI API for enhanced intelligence gathering and analysis. To use this feature:

1. Sign up for an account at [Perplexity AI](https://www.perplexity.ai/)
2. Navigate to the API section to generate an API key
3. Add the key to your `.env` file or use the `--api-key` command line argument

Note: The tool will still function without an API key, but will fall back to simulated data rather than real AI-powered analysis.

## Data Models

The tool uses Pydantic models for data validation and serialization:

- `SearchResult`: Represents a single search result with title, URL, snippet, etc.
- `ContentAnalysis`: Contains analysis of a specific URL including credibility, entities, and sentiment
- `OSINTReport`: The complete report with all collected data and analyses

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

When contributing to this project, please:

1. Ensure code follows PEP 8 style guide for Python code
2. Write unit tests for new features
3. Update documentation as needed
4. Make sure not to commit any API keys or sensitive information
5. Verify that all tests pass before submitting a PR

## Security Notes

⚠️ **IMPORTANT**: This tool requires API keys to function properly.

- Never commit your `.env` file with real API keys to GitHub
- Always use the `.env.example` file as a template
- Consider using GitHub Secrets for CI/CD workflows if adding automation

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This tool is for educational and research purposes only. Always ensure you comply with relevant laws and regulations when conducting OSINT research. The authors are not responsible for any misuse of this tool. 
