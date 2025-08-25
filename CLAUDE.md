# Business Idea to IR Presentation Generator

## System Overview

This multi-agent system transforms detailed business ideas into professional, investor-ready IR (Investor Relations) presentations with 8 comprehensive sections. The system uses specialized agents working in parallel with feedback loops to ensure high-quality, credible outputs.

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    HR ORCHESTRATOR AGENT                    │
│                   (Main Coordinator)                        │
└─────────────────┬───────────────────────────────────────────┘
                  │
     ┌────────────┴────────────┐
     │                         │
┌────▼────┐              ┌────▼────┐
│ CONTENT │              │ CRITIC  │
│ AGENTS  │◄────────────►│ AGENTS  │
│         │  FEEDBACK    │         │
│(Parallel│   LOOP       │         │
│Execution│              │         │
└─────────┘              └─────────┘
     │                         │
     ▼                         ▼
┌─────────────────────────────────┐
│    PRESENTATION DESIGNER        │
│      (Final Assembly)           │
└─────────────────────────────────┘
```

### Agent Ecosystem

#### Core Orchestration
- **HR Orchestrator** (`.claude/agents/hr_orchestrator.md`) - Main coordinator and agent manager

#### Content Generation (Parallel Execution)
- **Business Analyst** (`.claude/agents/business_analyst.md`) - Sections 1-3 (Problem, Value Prop, Magic)
- **Financial Analyst** (`.claude/agents/financial_analyst.md`) - Section 7 (Financial Projections)
- **Market Researcher** (`.claude/agents/market_researcher.md`) - Sections 4-6 (Business Model, GTM, Competition)
- **Strategy Consultant** (`.claude/agents/strategy_consultant.md`) - Section 8 (Status, Timeline, Funding)

#### Quality Assurance (Feedback Loop)
- **VC Red Team** (`.claude/agents/vc_red_team.md`) - Investor perspective critic (always active)
- **Technical Critic** (`.claude/agents/technical_critic.md`) - Technical feasibility validator
- **Financial Critic** (`.claude/agents/financial_critic.md`) - Financial model validator

#### Final Assembly
- **Presentation Designer** (`.claude/agents/presentation_designer.md`) - Visual design and final formatting

## Usage Instructions

### For Claude Code Users

When a user provides a business idea for IR presentation generation, follow this orchestration protocol:

#### Phase 1: Business Idea Analysis and Agent Deployment
```markdown
Use the Task tool to launch multiple agents concurrently:

1. **Initial Analysis**
   - Deploy HR Orchestrator agent to analyze the business idea
   - Identify required expertise areas and agent allocation
   - Determine parallel execution strategy

2. **Content Generation (Parallel)**
   - Deploy Business Analyst for sections 1-3
   - Deploy Financial Analyst for section 7  
   - Deploy Market Researcher for sections 4-6
   - Deploy Strategy Consultant for section 8
   
3. **Quality Assurance Setup**
   - Deploy VC Red Team agent for overall critique
   - Conditionally deploy Technical Critic (for tech businesses)
   - Conditionally deploy Financial Critic (for complex financial models)
```

#### Phase 2: Content Creation and Initial Review
```markdown
Task agents with specific section development:

Business Analyst Agent:
- Section 1: Problem/Opportunity (heart-rate changing pain points)
- Section 2: Value Proposition (quantified value delivery)  
- Section 3: Underlying Magic (visual technical differentiation)

Financial Analyst Agent:
- Section 7: Financial Projections and Key Metrics (bottom-up 3-year modeling)

Market Researcher Agent:
- Section 4: Business Model (clear monetization strategy)
- Section 5: Go-to-Market Plan (cost-effective customer acquisition)
- Section 6: Competitive Analysis (market landscape and positioning)

Strategy Consultant Agent:
- Section 8: Current Status, Timeline, and Use of Funds
```

#### Phase 3: Critic Review and Feedback Integration
```markdown
Deploy critic agents for feedback loops:

1. **VC Red Team Review** (Always)
   - Overall investment readiness assessment
   - Investor objection identification
   - Risk assessment and recommendations

2. **Technical Critic Review** (Tech businesses)
   - Technical feasibility validation
   - Architecture scalability assessment
   - Implementation risk evaluation

3. **Financial Critic Review** (Complex models)
   - Financial model validation
   - Assumption reality testing
   - Investment analysis rigor check
```

#### Phase 4: Refinement and Final Assembly
```markdown
1. **Content Refinement**
   - Integrate critic feedback into content sections
   - Resolve inconsistencies and gaps
   - Optimize for investor presentation standards

2. **Final Assembly**
   - Deploy Presentation Designer agent
   - Create cohesive 8-section presentation
   - Ensure professional visual design
   - Generate multiple output formats
```

### IR Presentation Requirements

The final presentation must include these 8 sections with specific quality criteria:

#### Section 1: Problem/Opportunity
- **Objective:** Make investors' hearts race with compelling pain points
- **Quality:** Emotionally resonant, quantified impact, clear urgency

#### Section 2: Value Proposition  
- **Objective:** Quantify the value of pain relief or pleasure delivery
- **Quality:** Numerical value quantification, credible ROI claims

#### Section 3: Underlying Magic
- **Objective:** Visual demonstration of proprietary technology/methodology
- **Quality:** Visual over textual, clear differentiation, defensible moats

#### Section 4: Business Model
- **Objective:** Clear monetization strategy targeting customer wallets
- **Quality:** Scalable acquisition model, defensible pricing strategy

#### Section 5: Go-to-Market Plan
- **Objective:** Cost-effective customer acquisition without financial strain
- **Quality:** Capital-efficient channels, realistic timeline, sustainable growth

#### Section 6: Competitive Analysis
- **Objective:** Comprehensive market landscape and competitive positioning  
- **Quality:** Complete competitor coverage, clear differentiation, market evolution insights

#### Section 7: Financial Projections and Key Metrics
- **Objective:** Bottom-up 3-year financial forecasts with supporting KPIs
- **Quality:** Realistic projections, documented assumptions, industry benchmarks

#### Section 8: Current Status, Timeline, and Use of Funds
- **Objective:** Progress demonstration, future planning, investment justification
- **Quality:** Clear progress proof, realistic milestones, justified fund allocation

### Feedback Loop Management

The system implements a three-round feedback process:

#### Round 1: Initial Draft Review
- HR Orchestrator collects all agent outputs
- Runs coherence check across sections
- Identifies gaps and inconsistencies  
- Generates critic assignments

#### Round 2: Critic Feedback Integration
- Relevant critic agents provide detailed feedback
- Content agents incorporate recommendations
- HR Orchestrator manages revision priorities
- Quality standards validation

#### Round 3: Final Quality Assurance
- Integrated presentation review
- Investor-readiness standards check
- Format consistency validation
- Presentation Designer deployment

### Multi-Agent Coordination Protocols

#### Parallel Execution Strategy
```markdown
Use concurrent Task tool calls for maximum efficiency:

- Content agents work simultaneously on their assigned sections
- Critic agents review outputs in parallel during feedback phases
- HR Orchestrator manages timing and dependencies
- Presentation Designer operates after all content is refined
```

#### Cross-Agent Communication
- Agents share context through HR Orchestrator
- Common business idea understanding maintained
- Consistent messaging and positioning across sections
- Integrated timeline and resource planning

#### Quality Assurance Standards
- Professional investor-grade presentation quality
- Data-driven insights and realistic projections  
- Clear value proposition articulation throughout
- Compelling storytelling with visual emphasis

## For Other Agentic IDEs

This system is designed for portability across different agentic environments:

### Agent File Structure
```
.claude/agents/
├── hr_orchestrator.md          # Main coordinator
├── business_analyst.md         # Sections 1-3
├── financial_analyst.md        # Section 7
├── market_researcher.md        # Sections 4-6
├── strategy_consultant.md      # Section 8
├── vc_red_team.md             # Investor critic
├── technical_critic.md         # Technical validator
├── financial_critic.md         # Financial validator
└── presentation_designer.md    # Final assembly
```

### Implementation Guidelines for Other IDEs

#### Agent Deployment Pattern
1. Parse business idea input
2. Launch HR Orchestrator for analysis and planning
3. Deploy content agents in parallel based on business type
4. Execute critic feedback loops based on complexity
5. Final assembly with Presentation Designer

#### Adaptation Notes
- Each `.md` file contains complete agent specifications
- Agents can be implemented as separate prompts/contexts
- Feedback loops can be managed through multi-turn conversations
- Output formats can be adapted to IDE capabilities

### System Extensibility

#### Adding New Agents
- Create specialized agents for specific industries (healthcare, fintech, etc.)
- Add regional expertise agents for different markets
- Include regulatory compliance agents for specific sectors

#### Customization Options
- Adjust presentation length and depth based on audience
- Modify visual design templates for different industries
- Customize financial modeling for different business models

## Success Metrics

### System Performance Indicators
- **Presentation Coherence Score:** Cross-section alignment and consistency
- **Investor Readiness Rating:** VC Red Team assessment score
- **Technical Feasibility Score:** Technical Critic validation rating
- **Financial Model Validity:** Financial Critic approval rating
- **Time to Completion:** Parallel processing efficiency measurement

### Quality Benchmarks
- Professional presentation standards compliance
- Industry benchmark alignment for financial projections
- Comprehensive risk identification and mitigation
- Clear investment thesis articulation

## Getting Started

To use this system:

1. **Input:** Provide detailed business idea description
2. **Processing:** System automatically deploys agents and manages workflow
3. **Output:** Receive professional 8-section IR presentation

The system is optimized for investor presentations but can be adapted for other business planning purposes.

---

*This multi-agent system represents a comprehensive approach to business idea development and investor presentation creation, leveraging specialized expertise and quality assurance through systematic feedback loops.*