# 📝 UPSC Essay Evaluator | Parallel Workflow with Agentic AI

<image-placeholder />

An AI-powered UPSC essay evaluation project that uses LLMs and structured output to analyse essay language quality, generate detailed feedback, and assign a score out of 10.

Built using **Python, LangGraph, LangChain, and Google Gemini**, this project explores workflow orchestration and parallel processing for automated essay evaluation.

---

## 🚀 Project Overview

Essay writing is an important part of UPSC preparation. Evaluating an essay requires careful attention to language quality, clarity, and the effectiveness of written communication.

This project explores how an AI-powered workflow can assist in essay evaluation by accepting an essay as input, processing it through a structured workflow, and generating an evaluation result.

The workflow uses **Google Gemini** as the LLM and LangChain's structured output functionality to produce consistent, machine-readable evaluation results.

## 🎯 Project Objectives

- Build an AI-powered UPSC essay evaluation system.
- Explore parallel workflow orchestration.
- Integrate Google Gemini with LangChain.
- Generate detailed essay feedback.
- Assign a numerical score out of 10.
- Work with structured LLM responses using an evaluation schema.
- Understand state management and workflow invocation.

## ⚙️ How It Works

The workflow follows a structured execution pipeline:

1. **Essay Input:** Accepts the essay as input.
2. **Initial State:** Stores the essay in a workflow state.
3. **Workflow Execution:** Passes the initial state to the workflow using `workflow.invoke()`.
4. **LLM Evaluation:** Uses Google Gemini to evaluate the essay.
5. **Structured Output:** Uses an `EvaluationSchema` to organise the model's response.
6. **Final Result:** Produces evaluation feedback and a score out of 10.

## 🧠 Core Concepts Explored

| Concept | Description |
|---|---|
| LangGraph | Workflow orchestration and execution |
| Parallel Workflows | Organising independent evaluation tasks |
| State Management | Passing essay data through workflow state |
| Prompt Engineering | Designing instructions for essay evaluation |
| LLM Integration | Connecting Gemini with LangChain |
| Structured Output | Producing schema-based evaluation responses |

## 💻 Implementation Highlights

### 1. Initial State

The essay is supplied to the workflow through an initial state dictionary.

```python
initial_state = {
    "essay": essay
}
```

### 2. Workflow Invocation

The workflow is executed by passing the initial state:

```python
result = workflow.invoke(initial_state)
```

### 3. LLM Integration

The project integrates Google Gemini through LangChain's Google Generative AI integration.

### 4. Structured Evaluation

The model uses a predefined `EvaluationSchema` through LangChain's structured output interface.

```python
structured_model = model.with_structured_output(
    EvaluationSchema
)
```

This helps organise the evaluation response into a predictable structure.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| LangGraph | Workflow orchestration |
| LangChain | LLM integration |
| Google Gemini | Essay evaluation |
| Pydantic | Structured evaluation schema |
| python-dotenv | Environment variable management |
| Jupyter Notebook | Development environment |

## 📂 Project Structure

```text
parallel_workflow_upsc_essayEvaluator_agenticAI/
│
├── 5_upsc_essay_workflow.ipynb
├── .env.example
├── .gitignore
└── README.md
```

## ⚡ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/priyanshukr001/parallel_workflow_upsc_essayEvaluator_agenticAI.git
```

### 2. Navigate to the Project

```bash
cd parallel_workflow_upsc_essayEvaluator_agenticAI
```

### 3. Create a Virtual Environment

```bash
python3 -m venv myenv
```

Activate it on macOS/Linux:

```bash
source myenv/bin/activate
```

### 4. Install Dependencies

```bash
python -m pip install langgraph langchain langchain-google-genai pydantic python-dotenv jupyter
```

### 5. Configure the Gemini API Key

Generate an API key through [Google AI Studio](https://aistudio.google.com/app/apikey).

Create a `.env` file in the project directory.

```env
Gemini_API_KEY=your_gemini_api_key
```

Make sure the environment variable name matches the one used in your notebook.

**Security:** Never upload your `.env` file or expose your API key in notebook outputs.

### 6. Run Jupyter Notebook

```bash
jupyter notebook
```

Open `5_upsc_essay_workflow.ipynb` and execute the notebook cells.

## 📊 Expected Output

The evaluator is designed to generate:

- Essay language-quality evaluation.
- Detailed written feedback.
- A numerical score out of 10.
- Structured evaluation output.

The exact output fields depend on the `EvaluationSchema` defined in the notebook.

## ⚠️ API Usage and Rate Limits

This project uses the Google Gemini API.

- API availability depends on the selected model and your account's usage limits.
- Free-tier requests may be subject to rate limits.
- A quota error such as HTTP 429 indicates that a model usage limit has been exceeded.
- Check [Gemini API Rate Limits](https://ai.google.dev/gemini-api/docs/rate-limits) when requests fail.

## 🔮 Future Enhancements

- Add separate evaluation criteria for content quality, coherence, grammar, and structure.
- Generate criterion-wise scores and actionable suggestions.
- Introduce comparative essay evaluation.
- Build a Streamlit-based interface for students.
- Add essay history and performance tracking.
- Explore multi-agent evaluation and advanced workflow orchestration.

## 👨‍💻 Author

**Priyanshu Kumar**

Mathematics and Computing  
Delhi Technological University

- GitHub: [@priyanshukr001](https://github.com/priyanshukr001)
- LinkedIn: [Priyanshu Kumar](https://www.linkedin.com/in/priyanshu-kumar-68a736229/)

---

⭐ If you find this project interesting, consider giving the repository a star!

*Part of my journey into Agentic AI, LangChain, LangGraph, and LLM-powered applications.*
