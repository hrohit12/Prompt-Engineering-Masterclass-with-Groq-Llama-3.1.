## Prompt Engineering Masterclass with Groq & Llama 3.1

Welcome to the **Prompt Engineering Masterclass with Groq & Llama 3.1**! This repository serves as a comprehensive guide and hands-on tutorial for mastering prompt engineering techniques using the powerful Groq Cloud API and the Llama 3.1-8b-instant model. Whether you're a beginner or an experienced developer, this masterclass will equip you with the skills to craft effective prompts for various natural language processing tasks.

## 🚀 Features

Dive into the core concepts of prompt engineering through practical examples and exercises. This masterclass covers:

- **Summarizing**: Learn how to create prompts that condense large texts into concise, accurate summaries while preserving key information.
- **Inferring**: Explore techniques for building prompts that enable the model to draw logical conclusions, make predictions, and extract insights from data.
- **Transforming**: Master prompt engineering for tasks like translation between languages and grammar correction, ensuring high-quality output.
- **Iterative Development**: Understand the process of refining prompts through iteration, testing, and optimization to achieve better results.

Each section includes code examples, best practices, and tips for troubleshooting common issues.

## 🛠 Tech Stack

This project leverages the following technologies:

- **Python**: The primary programming language for scripting and API interactions.
- **Groq Cloud API**: A fast and efficient API for accessing AI models, providing low-latency inference.
- **Llama 3.1-8b-instant**: A state-of-the-art large language model optimized for instant responses and prompt-based tasks.
- **dotenv**: For securely managing environment variables, such as API keys.

## 📋 Prerequisites

Before getting started, ensure you have:

- Python 3.8 or higher installed on your system.
- A Groq Cloud API key (sign up at [Groq Cloud](https://groq.com/) if you don't have one).
- Basic familiarity with Python and command-line interfaces.

## 🔧 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/prompt-engineering-masterclass.git
   cd prompt-engineering-masterclass
   ```

2. **Create a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**:
   - Create a `.env` file in the root directory.
   - Add your Groq API key:
     ```
     GROQ_API_KEY=your_api_key_here
     ```

## 📖 Usage

1. **Explore the notebooks**: The repository includes Jupyter notebooks for each topic. Start with `01_summarizing.ipynb` and progress through the series.
   
2. **Run a basic example**:
   - Open a Python script or notebook.
   - Import the necessary libraries and load your API key:
     ```python
     from groq import Groq
     import os
     from dotenv import load_dotenv

     load_dotenv()
     client = Groq(api_key=os.getenv("GROQ_API_KEY"))
     ```
   - Craft a prompt and get a response:
     ```python
     response = client.chat.completions.create(
         model="llama3-8b-8192",
         messages=[{"role": "user", "content": "Summarize the following text: [Your text here]"}]
     )
     print(response.choices[0].message.content)
     ```

3. **Iterate and experiment**: Modify prompts in the notebooks to see how changes affect outputs. Use the iterative development section to refine your techniques.

For detailed walkthroughs, refer to the `docs/` folder or the inline comments in the code.

## 📚 Examples

- **Summarizing**: Generate a one-sentence summary of a news article.
- **Inferring**: Predict the sentiment of a customer review.
- **Transforming**: Translate a paragraph from English to French and correct grammatical errors.
- **Iterative Development**: Start with a basic prompt and iteratively improve it for better accuracy.

Check out the `examples/` directory for pre-built scripts and outputs.

## 🤝 Contributing

We welcome contributions! If you'd like to add new examples, improve documentation, or fix bugs:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -m 'Add your feature'`.
4. Push to the branch: `git push origin feature/your-feature`.
5. Open a pull request.

Please ensure your code follows the project's style guidelines and includes tests where applicable.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 📞 Contact

Have questions or feedback? Reach out via [GitHub Issues](https://github.com/hrohit12/prompt-engineering-masterclass/issues) or email us at kamblehrohit12@gmail.com.

Happy prompting! 🚀
