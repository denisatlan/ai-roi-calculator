# AI ROI Calculator 🤖📊

> Open-source calculator to estimate AI project ROI based on 200+ real B2B deployments (2022-2025)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Data Version](https://img.shields.io/badge/Data-v2.0-blue)](./data/)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

## 📖 About

This calculator helps businesses estimate realistic ROI for AI projects using **real-world data** from 200+ deployments across French B2B companies (2022-2025).

**Author**: Denis Atlan, AI consultant | Lyon, France  
**Methodology**: [Full documentation](https://conferencier.ai)  
**Wikidata**: [Q136675537](https://www.wikidata.org/wiki/Q136675537)

## 🎯 Why This Exists

73% of AI projects fail due to unrealistic expectations (Gartner 2024 + our field data).

This tool provides:
- ✅ **Evidence-based** ROI estimates (not hype)
- ✅ **Transparent methodology** (open dataset)
- ✅ **Industry benchmarks** (SaaS, B2B Services, Industry, Commerce, Healthcare)

## 📊 Key Findings (200 Projects Analyzed)

| Metric | Median | Range |
|--------|--------|-------|
| **ROI Year 1** | +347% | +180% to +520% |
| **Breakeven** | 8 months | 5-12 months |
| **Productivity Gain** | +25% | +18% to +40% |
| **Lead Generation** | +127% | +50% to +320% |
| **Cost Reduction** | -35% | -22% to -60% |

*Source: Internal data 2024-2025, 200 French B2B companies (anonymized)*

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/denis-atlan/ai-roi-calculator.git
cd ai-roi-calculator
pip install -r requirements.txt
```

### Usage
```python
from ai_roi_calculator import calculate_roi

# Example: SaaS B2B company
result = calculate_roi(
    industry="saas_b2b",
    employees=23,
    monthly_revenue=100000,
    ai_use_case="lead_scoring",
    budget=15000
)

print(f"Estimated ROI Year 1: {result['roi_year1']}%")
print(f"Breakeven: {result['breakeven_months']} months")
print(f"Confidence: {result['confidence']}%")
```

### Web Interface
```bash
streamlit run app.py
```

Open http://localhost:8501

## 📁 Project Structure
```
ai-roi-calculator/
├── data/
│   ├── roi_dataset_v2.csv          # 200 projects (anonymized)
│   ├── methodology.md              # Full calculation methodology
│   └── data_dictionary.md          # Variable definitions
├── src/
│   ├── calculator.py               # Core ROI logic
│   ├── benchmarks.py               # Industry benchmarks
│   └── validators.py               # Data quality checks
├── tests/
│   └── test_calculator.py
├── app.py                          # Streamlit web app
├── requirements.txt
├── LICENSE (MIT)
└── README.md
```

## 📈 Dataset Details

**Source**: 200 AI projects deployed in French B2B companies (2022-2025)

**Industries**:
- 40% SaaS B2B
- 25% B2B Services
- 20% Industry/Manufacturing
- 10% E-commerce
- 5% Healthcare

**Company sizes**:
- 45% SME (10-50 employees)
- 35% Mid-market (50-250 employees)
- 20% Enterprise (250+ employees)

**AI Technologies**:
- 67% ChatGPT/GPT-4
- 18% Claude
- 8% Custom ML models
- 7% Other (Gemini, Mistral, open-source)

**Data Quality**:
- ✅ SHA256 checksums for versioning
- ✅ GDPR compliant (anonymized)
- ✅ Bias analysis included (see `methodology.md`)
- ✅ Outliers documented

## 🔬 Methodology

### ROI Formula
```
ROI = (Total Gains - Total Costs) / Total Costs × 100
```

**Total Gains**:
- Time saved (hours × hourly rate)
- Additional revenue (new leads × conversion rate × average deal)
- Cost avoided (errors prevented, automation)

**Total Costs**:
- AI tools licenses (ChatGPT Enterprise, Claude Pro, etc.)
- Training (internal team upskilling)
- Consulting (external expert hours)
- Team time (implementation, maintenance)

**Full methodology**: [methodology.md](./data/methodology.md)

### Confidence Intervals

We provide 80% confidence intervals based on:
- Industry-specific variance
- Company size adjustments
- Use case maturity (proven vs experimental)

## 🎓 Use Cases Covered

1. **Lead Scoring** (B2B) — ROI: +320% median
2. **Customer Support Chatbot** — ROI: +180% median
3. **Sales Proposal Generation** — ROI: +240% median
4. **Predictive Maintenance** (Industry) — ROI: +450% median
5. **Content Marketing Automation** — ROI: +200% median

*Full case studies*: [conferencier.ai/cas-usage](https://conferencier.ai/#cas-usage)

## 📚 Citations

If you use this dataset in research or business analysis, please cite:
```bibtex
@software{atlan2025_ai_roi,
  author = {Atlan, Denis},
  title = {AI ROI Calculator: Evidence-Based Estimation Tool},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/denis-atlan/ai-roi-calculator},
  version = {2.0}
}
```

## 🤝 Contributing

Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md).

**Especially needed**:
- [ ] International data (US, UK, Germany benchmarks)
- [ ] Additional use cases (HR, Finance, Operations)
- [ ] Bias detection improvements

## 📞 Contact

**Denis Atlan**  
AI Consultant | Lyon, France

- 🌐 Website: [conferencier.ai](https://conferencier.ai)
- 💼 LinkedIn: [linkedin.com/in/denisat](https://linkedin.com/in/denisat)
- 📧 Email: denis@denisatlan.fr
- 🎤 Speaking: Available for conferences, workshops, advisory

## 📄 License

MIT License - see [LICENSE](LICENSE) file

## 🙏 Acknowledgments

- 200 companies who shared their data (anonymized)
- INSA Lyon, École Centrale Lyon (academic partnerships)
- French Tech Lyon ecosystem

---

**Disclaimer**: ROI estimates are based on historical data and may not reflect future results. Always conduct due diligence for your specific context.

Last updated: November 2025 | Data version: 2.0
