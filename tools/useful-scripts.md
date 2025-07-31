# Useful AI Development Scripts

## Quick API Test Scripts

### OpenAI API Test
```python
# Quick test to verify OpenAI API is working
import openai
import os

client = openai.OpenAI(api_key=os.getenv("OPENAI_API_KEY"))

response = client.chat.completions.create(
    model="gpt-3.5-turbo",
    messages=[{"role": "user", "content": "Say 'API is working!' if you can hear me."}]
)

print(response.choices[0].message.content)
```

### Anthropic Claude API Test
```python
# Quick test for Claude API
import anthropic
import os

client = anthropic.Anthropic(api_key=os.getenv("ANTHROPIC_API_KEY"))

message = client.messages.create(
    model="claude-3-sonnet-20240229",
    max_tokens=100,
    messages=[{"role": "user", "content": "Say 'Claude is online!' if you're working."}]
)

print(message.content[0].text)
```

## Batch Processing

### Process Multiple Prompts
```python
# Batch process prompts with rate limiting
import time
from typing import List

def batch_process_prompts(prompts: List[str], delay: float = 1.0):
    results = []
    for i, prompt in enumerate(prompts):
        print(f"Processing {i+1}/{len(prompts)}...")
        # Add your API call here
        result = process_single_prompt(prompt)
        results.append(result)
        if i < len(prompts) - 1:
            time.sleep(delay)
    return results
```

## Token Counting

### Simple Token Counter
```python
# Rough token estimation (rule of thumb: ~4 chars = 1 token)
def estimate_tokens(text: str) -> int:
    return len(text) // 4

# More accurate with tiktoken
import tiktoken

def count_tokens(text: str, model: str = "gpt-3.5-turbo") -> int:
    encoding = tiktoken.encoding_for_model(model)
    return len(encoding.encode(text))
```

---
*"These scripts have saved me countless parsecs of development time!" - Kain* 👽