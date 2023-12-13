# Langchain Project

This project contains Python code and Jupyter notebooks for generating summary of book "Crime And Punishment" and prompt template for personalized study plans. Find GPT for study planner [here](https://chat.openai.com/g/g-ftmU3BXvS-study-planner)

## Files in this repository

- [`README.md`](command:_github.copilot.openRelativePath?%5B%22README.md%22%5D "README.md"): This file.
- [`summary.json`](command:_github.copilot.openRelativePath?%5B%22summary.json%22%5D "summary.json"): A JSON file containing history of generated summaries of book.
- [`tasks.ipynb`](command:_github.copilot.openRelativePath?%5B%22tasks.ipynb%22%5D "tasks.ipynb"): A Jupyter notebook containing tasks for generating personalized study plans and summarizing books.
- [`.gitignore`](command:_github.copilot.openRelativePath?%5B%22.gitignore%22%5D ".gitignore"): A file specifying untracked files that Git should ignore.

## Usage


### Generate a Book Summary

The [`tasks.ipynb`](command:_github.copilot.openRelativePath?%5B%22tasks.ipynb%22%5D "tasks.ipynb") notebook contains a Python script for generating a summary of a book. The script first splits the book into chapters, cleans documents, then generates a summary for each chapter, and finally concatenates the summaries into a single summary. It also appends the generated summary to [`summary.json`](command:_github.copilot.openRelativePath?%5B%22summary.json%22%5D "summary.json") to compare generated content for given prompt. This is achieved using langchains map reduce summarizer and OpenAI's GPT-3.5, 16K context model.

### Generate a Personalized Study Plan

The [`tasks.ipynb`](command:_github.copilot.openRelativePath?%5B%22tasks.ipynb%22%5D "tasks.ipynb") notebook contains a Python script for generating a personalized study plan for a student. The script takes into account the student's academic performance, learning style, extracurricular activities, personal objectives and challenges, personal interests, schedule, progress tracking needs, and supportive resources and tools.

To generate a study plan, run the following code in the [`tasks.ipynb`](command:_github.copilot.openRelativePath?%5B%22tasks.ipynb%22%5D "tasks.ipynb") notebook:

```python
prompt = PromptTemplate.from_template(prompt)
formatted_prompt = prompt.format(
    name="John Wesley",
    level="high school",
    grades="A in Math, B in English, C in Science",
    style="visual",
    activities="playing soccer",
    goals="acing SATs",
    challenges="lack of motivation and focus"
)
print('\n'.join(textwrap.wrap(formatted_prompt, 80)))
```

Replace the arguments to `prompt.format()` with the student's information.