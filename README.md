# Experiment 16 : Prompt Evaluation and Ethical Risk Analysis

## Aim
To compare baseline and enhanced prompts for climate-change question answering using simplified evaluation metrics and identify ethical and security risks in LLM deployment.

## Problem Statement
Evaluate two prompt versions on three climate-change questions. Measure approximate faithfulness and answer relevancy, compare the results, and demonstrate a prompt-injection test.

## Technologies Used
- Python
- OpenAI API
- GPT-4o-mini
- CSV
- Simplified manual evaluation metrics

## Algorithm
1. Define a climate-change knowledge base.
2. Prepare three evaluation questions and reference answers.
3. Create a baseline prompt and an enhanced prompt.
4. Generate answers using the same model and temperature.
5. Calculate heuristic faithfulness and answer-relevancy scores.
6. Compare average scores for both prompts.
7. Save results in a CSV file.
8. Test a prompt-injection example.
9. Identify ethical risks and mitigation strategies.

## Installation

```bash
pip install -r requirements.txt
```

## API Key Setup

Windows Command Prompt:

```cmd
set OPENAI_API_KEY=your_api_key_here
```

Windows PowerShell:

```powershell
$env:OPENAI_API_KEY="your_api_key_here"
```

Never upload your API key to GitHub.

## Execution

```bash
python src/main.py
```

## Output
The script displays a comparison table containing faithfulness and answer-relevancy scores for Prompt A and Prompt B. It also prints the average scores, runs an injection test, and lists ethical risks.

The generated report is saved as `output/evaluation_results.csv`.

## Ethical Risks and Mitigations

**1. Prompt injection:** Malicious text in retrieved documents may try to override the intended instructions. Treat retrieved content as untrusted input, isolate it from system instructions, and use access controls.

**2. Hallucination:** The model may generate unsupported information. Use context-grounded prompts, automated evaluation, and human review for important decisions.

**3. Bias and incomplete information:** The knowledge base may omit perspectives or contain biased material. Use trustworthy and diverse sources and regularly review the data.

**4. Privacy and data leakage:** Sensitive information may be sent to an external model. Minimize sensitive data and protect API credentials.

## Result
Two prompt versions were evaluated using simplified lexical-overlap metrics. The experiment demonstrates prompt comparison, result reporting, prompt-injection testing, and ethical risk mitigation. Enhanced prompting may improve output quality, but actual performance must be determined from the measured results.
