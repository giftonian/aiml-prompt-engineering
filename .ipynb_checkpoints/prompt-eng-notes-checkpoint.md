# Prompt Engineering for Developers

- Focus of this course is Instructions Tuned LLMs, instead of Base LLMs

## Principles
1. Write clear and specific instructions
- Tactic 1: Use delimiters i.e., Triple quotes, Triple backticks, Triple dashes, tags
- Example: prompt = f""" Summarize the text delimited by triple backticks \ into a single sentence. ```{text}``` """
- With above example, you can avoid Prompt Injection. It means, if user tries to inject his own command, the model will still summarize his wordings instead of acting upon the command.
- Tactic 2: Ask the structured output
- prompt = f""" Generate a list of three made-up book titles along \ with their authors and genres. Provide them in JSON format with the following keys: book_id, titile, author, genre."""
- Tactic 3: Check whether conditions are satisfied e.g.,:
- Check assumptions required to do the task. You may also tell model to handle the edge cases. See, Steps prompt example in jupyter notebook
- Tactic 4: Few-shot prompting
- Give successfull examples of completing tasks, then ask model to perform the task

2. Give LLM/Model time to think

