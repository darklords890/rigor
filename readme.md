# rigor
Statistical testing tools for LLM experiments. Stop eyeballing results, test for significance.

## The Problem

Teams compare LLM prompts by looking at raw accuracy numbers:
- Prompt A (reasoning): 60%
- Prompt B (direct): 53.3%

They ship Prompt A because it looks 7% better.

But with only 30 test queries, that difference could easily be random noise. Without statistical testing, you might:
- Ship a worse prompt based on chance variation
- Waste weeks optimizing for insignificant gains
- Report evaluation results that can't be replicated

## What This Does

`rigor` tells you if differences are real or just noise. Proper significance tests, confidence intervals, and effect sizes - specifically designed for LLM evaluation patterns (binary outcomes, paired comparisons, small sample sizes).

## What This Does

`rigor` provides statistical testing functions specifically for LLM experiments:
- **Proper significance tests** (McNemar, Wilcoxon, bootstrap)
- **Confidence intervals** for metrics
- **Effect size** calculation (Cohen's d)
- **Sample size** determination before you run experiments

## Installation

Not yet published to PyPI. For now, the easiest way to use this is:

**Option 1: Run the tutorial notebook**
- Open [tutorials/mmlu_prompt_comparison.ipynb](tutorials/mmlu_prompt_comparison.ipynb) on GitHub
- Click the "Open in Colab" badge
- All functions are defined inline — just run the cells

**Option 2: Copy functions directly**
- Copy the statistical functions from Cell 6 of the tutorial notebook
- Paste into your own code


## Status

**Alpha / Work in Progress**

Currently includes:
-  Comparison tests (McNemar, Wilcoxon, paired t-test, bootstrap)
-  Confidence intervals (Wilson, bootstrap)
-  Effect sizes (Cohen's dz)

Roadmap:
- Multiple comparison corrections
- Power analysis
- Integration with eval frameworks (RAGAS, DeepEval)
- Visualization tools

## License

MIT

## Author

Subhrajit Nag

[LinkedIn](https://www.linkedin.com/in/subhrajit-nag-8332a6a4/)
