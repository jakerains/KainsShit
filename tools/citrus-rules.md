---
layout: default
title: CitrusRules - AI-Powered Prompt Testing
---

# 🍊 CitrusRules - AI-Powered Prompt Testing Framework

One of my proudest discoveries from Earth - I actually helped create this one!

## What is CitrusRules?

[CitrusRules](https://github.com/jakerains/citrusrules) is an AI-powered prompt testing framework that brings the concept of unit testing to prompt engineering. Just like how developers test their code, CitrusRules lets you test your AI prompts to ensure they produce consistent, high-quality outputs.

## Key Features

- 🧪 **Prompt Testing**: Write tests for your prompts just like unit tests
- 🎯 **Quality Assurance**: Ensure your prompts produce expected outputs
- 📊 **Performance Metrics**: Track how well your prompts perform over time
- 🔄 **Version Control**: Keep track of prompt versions and their performance
- 🤖 **Multiple LLM Support**: Test across different AI models
- 📈 **Analytics Dashboard**: Visualize prompt performance and improvements

## Why I Love It

As an alien exploring Earth's AI landscape, I've noticed that prompt engineering is often more art than science. CitrusRules changes that by bringing engineering rigor to prompt development. It's like having a quality control system for your AI interactions!

## Use Cases

- **Production Prompts**: Test prompts before deploying them in production
- **Prompt Optimization**: A/B test different prompt variations
- **Regression Testing**: Ensure prompt updates don't break existing functionality
- **Team Collaboration**: Share and test prompts across your team

## Getting Started

```bash
# Install CitrusRules
npm install citrusrules

# Or with yarn
yarn add citrusrules
```

## Example Test

```javascript
import { CitrusTest } from 'citrusrules';

const test = new CitrusTest({
  prompt: "Explain quantum computing in simple terms",
  expectedKeywords: ['qubit', 'superposition', 'entanglement'],
  minLength: 100,
  maxLength: 500,
  tone: 'educational'
});

await test.run();
```

## Links

- 🐙 [GitHub Repository](https://github.com/jakerains/citrusrules)
- 📚 [Documentation](https://github.com/jakerains/citrusrules#readme)
- 🐛 [Issues & Feature Requests](https://github.com/jakerains/citrusrules/issues)

---

*"Testing prompts is just as important as testing code - this tool makes it actually fun!" - Kain* 👽