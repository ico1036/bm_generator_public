# Business Idea to IR Presentation Generator

A sophisticated multi-agent system that transforms detailed business ideas into professional, investor-ready IR (Investor Relations) presentations using specialized AI agents working in parallel with feedback loops.

## Overview

This system generates comprehensive 8-section investor presentations that meet professional VC standards, including problem analysis, value propositions, financial projections, and investment strategies.

### Key Features

- **Multi-Agent Architecture:** 9 specialized agents working in parallel and coordination
- **Feedback Loop System:** Critic agents provide quality assurance and improvement recommendations
- **Professional Output:** Investor-grade presentations with visual design and data visualization
- **Portable Framework:** Compatible with multiple agentic IDEs (Claude Code, Cursor, etc.)
- **Comprehensive Coverage:** All 8 critical sections of professional IR presentations

## System Architecture

```
Input: Detailed Business Idea → Multi-Agent Processing → Output: Professional IR Presentation

┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│ Business Idea   │ →  │ HR Orchestrator  │ →  │ 8-Section IR    │
│ Description     │    │ Agent            │    │ Presentation    │
└─────────────────┘    └──────────────────┘    └─────────────────┘
                               │
                    ┌──────────┴──────────┐
                    │                     │
            ┌───────▼────────┐    ┌──────▼──────┐
            │ Content Agents │    │ Critic      │
            │ (Parallel)     │◄──►│ Agents      │
            │                │    │ (Feedback)  │
            └────────────────┘    └─────────────┘
                    │                     │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │ Presentation        │
                    │ Designer Agent      │
                    └─────────────────────┘
```

## Agent Ecosystem

### Core Agents

| Agent | Role | Sections | Expertise |
|-------|------|----------|-----------|
| **HR Orchestrator** | Main coordinator | All | Project management, agent coordination |
| **Business Analyst** | Problem & solution analysis | 1-3 | Market analysis, value propositions |
| **Financial Analyst** | Financial modeling | 7 | Financial projections, unit economics |
| **Market Researcher** | Market & competition | 4-6 | Business models, GTM, competitive analysis |
| **Strategy Consultant** | Planning & funding | 8 | Strategic planning, milestone tracking |

### Quality Assurance Agents

| Agent | Role | Focus | When Active |
|-------|------|-------|-------------|
| **VC Red Team** | Investor perspective critic | Investment readiness | Always |
| **Technical Critic** | Technical feasibility | Technology validation | Tech businesses |
| **Financial Critic** | Financial model validation | Financial accuracy | Complex models |

### Output Agent

| Agent | Role | Responsibility |
|-------|------|----------------|
| **Presentation Designer** | Visual design & assembly | Professional formatting, final presentation |

## IR Presentation Sections

The system generates professional presentations with these 8 sections:

1. **Problem/Opportunity** - Compelling pain points that change investor heart rates
2. **Value Proposition** - Quantified value delivery with ROI calculations  
3. **Underlying Magic** - Visual demonstration of proprietary technology/methodology
4. **Business Model** - Clear monetization strategy and customer wallet targeting
5. **Go-to-Market Plan** - Cost-effective customer acquisition without financial strain
6. **Competitive Analysis** - Comprehensive market landscape and positioning
7. **Financial Projections** - Bottom-up 3-year modeling with KPIs and metrics
8. **Current Status & Use of Funds** - Progress demonstration and investment justification

## Quick Start Guide

### For Claude Code Users

1. **Prepare Your Business Idea**
   ```markdown
   Use the input template: templates/business_idea_input_template.md
   Fill out comprehensive business details
   ```

2. **Initiate System**
   ```markdown
   Submit your business idea to Claude Code
   System automatically deploys HR Orchestrator
   ```

3. **Processing Flow**
   ```markdown
   Phase 1: Business analysis and agent deployment (parallel)
   Phase 2: Content generation by specialized agents
   Phase 3: Critic feedback and refinement loops
   Phase 4: Final assembly and professional formatting
   ```

4. **Receive Output**
   ```markdown
   Professional IR presentation in multiple formats:
   - PowerPoint (.pptx)
   - PDF document
   - Markdown documentation
   ```

### For Other Agentic IDEs

The system is designed for portability:

1. **Agent Implementation**: Use agent files in `claude/agents/` as prompt templates
2. **Workflow Management**: Follow orchestration logic in `CLAUDE.md`
3. **Quality Standards**: Apply feedback loop protocols for quality assurance
4. **Output Assembly**: Use presentation designer specifications for final formatting

## File Structure

```
bm_generator/
├── CLAUDE.md                          # Main orchestration logic
├── README.md                          # This file
├── .claude/
│   └── agents/                        # Specialized agent definitions
│       ├── hr_orchestrator.md         # Main coordinator
│       ├── business_analyst.md        # Sections 1-3 specialist
│       ├── financial_analyst.md       # Section 7 specialist  
│       ├── market_researcher.md       # Sections 4-6 specialist
│       ├── strategy_consultant.md     # Section 8 specialist
│       ├── vc_red_team.md            # Investor critic
│       ├── technical_critic.md        # Technical validator
│       ├── financial_critic.md        # Financial validator
│       └── presentation_designer.md   # Final assembly
└── templates/
    ├── business_idea_input_template.md    # Input format guide
    └── ir_presentation_output_template.md # Output structure reference
```

## Usage Examples

### Example Input
```markdown
Business Concept: AI-powered customer service automation platform
Industry: SaaS/B2B Technology
Target Market: Mid-market companies with customer service teams
Problem: 73% of customer service interactions could be automated but current solutions lack context understanding
Solution: Advanced NLP platform that maintains conversation context across channels
Revenue Model: Monthly subscription based on interaction volume
Funding Need: $2M Series A for product development and market expansion
```

### Expected Output
- Professional 15-slide presentation with appendix
- Quantified problem analysis with market data
- Technical architecture diagrams
- Bottom-up financial model with 3-year projections
- Competitive positioning and market analysis
- Investment justification and use of funds breakdown

## Quality Standards

### Professional Presentation Requirements
- Investor-grade visual design and formatting
- Clear narrative flow and logical progression  
- Data-driven insights with credible sources
- Realistic financial projections with documented assumptions
- Comprehensive risk assessment and mitigation strategies

### Agent Performance Standards
- Specialist expertise demonstration
- Evidence-based analysis and recommendations
- Industry benchmarking and best practices
- Constructive feedback and improvement suggestions
- Professional communication and presentation

## Advanced Features

### Feedback Loop System
- **Round 1**: Initial draft review and coherence checking
- **Round 2**: Critic feedback integration and refinement
- **Round 3**: Final quality assurance and investor readiness validation

### Parallel Processing Optimization
- Content agents work simultaneously on different sections
- Critic agents provide concurrent feedback during review phases
- HR Orchestrator manages dependencies and quality coordination

### Customization Options
- Industry-specific agent specialization
- Regional market adaptation
- Presentation length and depth adjustment
- Visual design template customization

## Contributing

To extend or modify the system:

1. **Add New Agents**: Create specialized agents for specific industries or functions
2. **Enhance Feedback Loops**: Improve critic agent capabilities and validation
3. **Expand Output Formats**: Add new presentation formats or visualization options
4. **Optimize Workflows**: Enhance parallel processing and coordination efficiency

## Support and Troubleshooting

### Common Issues
- **Incomplete Input**: Use the input template to ensure comprehensive business idea description
- **Quality Concerns**: Feedback loops automatically address most quality issues through refinement
- **Format Issues**: Presentation Designer agent handles multiple output format requirements

### Best Practices
- Provide detailed, quantifiable business information
- Include market research and competitive analysis data
- Be realistic about assumptions and projections
- Allow system to complete all feedback loops for optimal quality

