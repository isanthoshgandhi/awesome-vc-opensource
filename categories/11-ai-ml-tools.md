# 11. 🤖 AI & ML Tools for VC

> Artificial intelligence and machine learning tools for deal screening, startup evaluation, market prediction, and investment decision support.

[← Back to main list](../README.md)

---

## Stage Coverage

| 🌱 Pre-Seed | 🌿 Seed | 🚀 Series A/B | 📈 Series C/D | 🏢 Late Stage |
|:---:|:---:|:---:|:---:|:---:|
| ✅ | ✅ | ✅ | ✅ | ✅ |

---

## LLM-Powered Investment Tools

### [AI4Finance-Foundation/FinGPT](https://github.com/AI4Finance-Foundation/FinGPT)
**Language:** Python | **Stars:** ⭐ 14K+ | **Stages:** 🌍 All Stages

Open-source financial large language model framework. Fine-tuned on financial news, SEC filings, earnings calls, and market data. Supports sentiment analysis, robo-advisory, and financial forecasting tasks.

**Key capabilities:**
- Financial sentiment analysis on news and social media
- Earnings call summarization and Q&A
- Market trend prediction
- SEC filing analysis and due diligence support

---

### [OpenBB-finance/OpenBBTerminal](https://github.com/OpenBB-finance/OpenBBTerminal)
**Language:** Python | **Stars:** ⭐ 28K+ | **Stages:** 🌍 All Stages

Open-source Bloomberg Terminal alternative with AI-powered analytics. Covers equities, crypto, macro data, and alternative data sources.

**AI features:**
- Natural language queries for financial data
- AI-powered chart analysis
- Automated research report generation
- Portfolio optimization algorithms

---

### [virattt/ai-hedge-fund](https://github.com/virattt/ai-hedge-fund)
**Language:** Python | **Stars:** ⭐ 8K+ | **Stages:** 📈 Series C/D | 🏢 Late Stage

AI-powered hedge fund simulation using multiple LLM agents. Each agent specializes in a different investment philosophy (value, growth, momentum, risk management).

**Agents included:**
- Warren Buffett-style value investor agent
- Cathie Wood-style growth investor agent
- Risk management and portfolio sizing agent
- Technical analysis agent

---

### [startup-valuation-ML](https://github.com/ShivamGupta0914/Startup-Valuation-using-ML)
**Language:** Python | **Stars:** ⭐ 200+ | **Stages:** 🌱 Pre-Seed | 🌿 Seed | 🚀 Series A/B

Machine learning models for startup valuation prediction. Trained on historical funding data, team metrics, market size, and traction signals.

**Models included:**
- Random forest valuation predictor
- Gradient boosting for funding round prediction
- Feature importance analysis for key value drivers
- Comparable company analysis automation

---

## Pitch Deck & Document AI

### [julep-ai/pitch-deck-analyzer](https://github.com/julep-ai/pitch-deck-analyzer)
**Language:** Python | **Stars:** ⭐ 500+ | **Stages:** 🌱 Pre-Seed | 🌿 Seed | 🚀 Series A/B

AI-powered pitch deck analysis tool. Extracts key metrics, evaluates narrative strength, benchmarks against successful decks, and generates investment memos automatically.

**Analysis includes:**
- Team background evaluation
- Market size (TAM/SAM/SOM) extraction
- Business model assessment
- Competitive landscape mapping
- Red flag detection

---

### [Investment-memo-LLM](https://github.com/lgaleana/investment-memo)
**Language:** Python | **Stars:** ⭐ 300+ | **Stages:** 🌿 Seed | 🚀 Series A/B

Automated investment memo generation using LLMs. Takes a company name or website URL and produces a structured VC-style investment memo covering market opportunity, business model, team, risks, and recommendation.

---

## Curated Resource Lists

### [georgezouq/awesome-ai-in-finance](https://github.com/georgezouq/awesome-ai-in-finance)
**Language:** Markdown | **Stars:** ⭐ 3K+ | **Stages:** 🌍 All Stages

Curated list of AI and machine learning tools specifically for finance and investment. Covers deep learning for trading, NLP for financial text, portfolio optimization, and risk management.

**Categories:**
- Time series forecasting models
- NLP for earnings calls and news
- Reinforcement learning for trading
- Alternative data sources and APIs
- Explainable AI for investment decisions

---

## AI Screening Workflow

### AI Pitch Screener (Anthropic Claude SDK)

```python
#!/usr/bin/env python3
"""
AI-powered pitch deck screener using Anthropic Claude.
Evaluates startups across 6 key VC criteria.
"""

import anthropic
import json
from dataclasses import dataclass
from typing import Optional

@dataclass
class StartupProfile:
    name: str
    sector: str
    stage: str
    description: str
    team_background: str
    market_size: str
    revenue: Optional[str] = None
    growth_rate: Optional[str] = None

def screen_startup(startup: StartupProfile) -> dict:
    """Screen a startup using Claude AI across key VC criteria."""
    
    client = anthropic.Anthropic()
    
    prompt = f"""You are an experienced venture capital partner evaluating a startup investment opportunity.

## Startup Profile
- **Company:** {startup.name}
- **Sector:** {startup.sector}  
- **Stage:** {startup.stage}
- **Description:** {startup.description}
- **Team:** {startup.team_background}
- **Market Size:** {startup.market_size}
- **Revenue:** {startup.revenue or 'Pre-revenue'}
- **Growth:** {startup.growth_rate or 'N/A'}

## Evaluation Criteria
Please evaluate this startup across these 6 dimensions (score each 1-10):

1. **Team** - Founder-market fit, domain expertise, execution ability
2. **Market** - TAM size, growth rate, timing, market dynamics
3. **Product** - Differentiation, defensibility, technical moat
4. **Traction** - Revenue, growth, customer validation, PMF signals
5. **Business Model** - Unit economics, scalability, margin potential
6. **Risk Profile** - Key risks, regulatory, competitive threats

## Output Format
Respond in valid JSON with this structure:
{{
  "scores": {{
    "team": <1-10>,
    "market": <1-10>,
    "product": <1-10>,
    "traction": <1-10>,
    "business_model": <1-10>,
    "risk_profile": <1-10>
  }},
  "overall_score": <weighted average>,
  "verdict": "PASS" | "CONDITIONAL PASS" | "PASS TO PARTNER" | "DECLINE",
  "investment_thesis": "<2-3 sentence bull case>",
  "key_risks": ["<risk1>", "<risk2>", "<risk3>"],
  "due_diligence_priorities": ["<item1>", "<item2>", "<item3>"],
  "comparable_companies": ["<comp1>", "<comp2>"],
  "suggested_check_size": "<range>",
  "summary": "<executive summary paragraph>"
}}"""

    message = client.messages.create(
        model="claude-opus-4-5",
        max_tokens=1500,
        messages=[{"role": "user", "content": prompt}]
    )
    
    response_text = message.content[0].text
    
    # Parse JSON response
    try:
        result = json.loads(response_text)
    except json.JSONDecodeError:
        # Extract JSON from markdown code blocks if present
        import re
        json_match = re.search(r'```json\n(.*?)```', response_text, re.DOTALL)
        if json_match:
            result = json.loads(json_match.group(1))
        else:
            result = {"raw_response": response_text}
    
    return result

def batch_screen(startups: list[StartupProfile]) -> list[dict]:
    """Screen multiple startups and rank by overall score."""
    results = []
    for startup in startups:
        print(f"Screening {startup.name}...")
        screening = screen_startup(startup)
        screening["company"] = startup.name
        screening["stage"] = startup.stage
        results.append(screening)
    
    # Sort by overall score descending
    results.sort(key=lambda x: x.get("overall_score", 0), reverse=True)
    return results

# Example usage
if __name__ == "__main__":
    pipeline = [
        StartupProfile(
            name="DataFlow AI",
            sector="B2B SaaS / Analytics",
            stage="Seed",
            description="AI-powered data pipeline automation for mid-market enterprises",
            team_background="Ex-Databricks engineer + ex-McKinsey data consultant",
            market_size="$12B TAM, growing 35% YoY",
            revenue="$180K ARR",
            growth_rate="22% MoM for 4 months"
        ),
        StartupProfile(
            name="GreenCredit",
            sector="Climate FinTech",
            stage="Pre-Seed",
            description="Carbon credit verification platform using satellite imagery + ML",
            team_background="NASA scientist + climate policy expert",
            market_size="$50B voluntary carbon market by 2030",
        ),
    ]
    
    results = batch_screen(pipeline)
    
    print("\n=== SCREENING RESULTS (Ranked by Score) ===")
    for i, result in enumerate(results, 1):
        print(f"\n#{i}: {result['company']} ({result['stage']})")
        print(f"  Overall Score: {result.get('overall_score', 'N/A')}/10")
        print(f"  Verdict: {result.get('verdict', 'N/A')}")
        print(f"  Thesis: {result.get('investment_thesis', 'N/A')}")
```

---

## Additional Resources

| Resource | Description |
|----------|-------------|
| [Hugging Face Finance Models](https://huggingface.co/models?filter=finance) | Pre-trained models for financial NLP |
| [awesome-quant](https://github.com/wilsonfreitas/awesome-quant) | Quantitative finance libraries |
| [ML-For-Finance](https://github.com/PacktPublishing/Machine-Learning-for-Finance) | ML techniques applied to finance |

---

## Stage-Specific AI Use Cases

| Stage | Primary AI Use Cases |
|-------|---------------------|
| 🌱 Pre-Seed | Founder background research, market sizing, patent analysis |
| 🌿 Seed | Pitch deck scoring, team assessment, competitive mapping |
| 🚀 Series A/B | Revenue forecasting, cohort analysis, GTM optimization |
| 📈 Series C/D | Market share prediction, M&A target screening |
| 🏢 Late Stage | IPO readiness scoring, comparable analysis, risk modeling |
