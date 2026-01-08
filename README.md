# Career Counsellor – Multi-Agent AI System

## Overview
Career Counsellor is a **multi-agent AI-powered career research and guidance system** designed to help Indian students after Class 10 make informed academic and career decisions.  
The system leverages **Google ADK**, **Gemini LLMs**, and **tool-augmented agents** to provide real-time, structured, and data-backed career insights.

---

## Key Features
- **Multi-Agent Architecture**: Uses parallel and sequential agents for scalable and modular career research.
- **Real-Time Career Research**: Fetches up-to-date career trends, salary ranges, entrance exams, and subject requirements using Google Search.
- **Cross-Country Salary Normalization**: Built-in currency conversion enables salary comparison across **India, US, and Japan**.
- **Domain Coverage**:
  - AI & Technology careers
  - Math-intensive fields
  - Research-based paths (ISRO, DRDO, IISc, IISER)
  - Science majors (Medical, Engineering, Agriculture, Biotechnology, etc.)
- **Decision-Ready Output**: Aggregates multi-source research into a concise executive summary with key takeaways.

---

## System Architecture

### 1. Parallel Research Agents
Independent agents run simultaneously to reduce latency and improve coverage:
- **AIResearcher** – AI and emerging tech careers
- **MathResearcher** – Math-intensive and analytical careers
- **ResearchFieldResearcher** – Research-focused institutions and paths
- **ScienceResearcher** – Medical, engineering, and science majors

### 2. Aggregator Agent
- Synthesizes outputs from all research agents
- Produces a **180–220 word executive summary**
- Highlights subject alignment, salary trends, exams, and fallback options

### 3. Orchestration
- **ParallelAgent** executes independent research concurrently
- **SequentialAgent** ensures aggregation runs after research completion

---

## Tech Stack
- **Language**: Python
- **Framework**: Google ADK
- **LLMs**: Gemini (gemini-2.5-flash-lite)
- **Tools**: Google Search (tool-augmented retrieval)
- **Architecture**: Parallel + Sequential Agent Orchestration

---

## Output Structure
The final output is structured for easy downstream consumption:
{
  "final_report": "Executive career summary with key takeaways"
}
----
## Google ADK Web UI Demonstration

This section showcases the use of the **Google ADK Web UI** for developing, executing, and debugging the multi-agent career counsellor system.

---

### Multi-Agent Orchestration View

This view illustrates the **parallel and sequential orchestration** of agents within the system:

- Parallel execution of **AIResearcher, MathResearcher, ResearchFieldResearcher, and ScienceResearcher**
- Clear visualization of **agent dependencies and execution order**
- Tool invocations (e.g., **Google Search**) during agent execution
- AggregatorAgent execution only after all parallel agents complete

<p align="center">
  <img src="./images/adk_multi_agent_orchestration.png" width="750">
  <br>
  <em>Parallel and sequential agent orchestration in Google ADK Web UI</em>
</p>

---

### Agent Execution, Events, and Output Inspection

This view demonstrates how the Web UI supports **interactive testing and debugging**:

- Displays **event logs and intermediate outputs** from each agent
- Shows how user queries propagate across multiple agents
- Enables inspection of **structured responses** for real-world prompts
- Helps validate correctness, completeness, and consistency of outputs

<p align="center">
  <img src="./images/adk_agent_execution_output.png" width="750">
  <br>
  <em>Agent execution trace and structured output inspection</em>
</p>

---

### Benefits of Using Google ADK Web UI

- Improves **observability** of multi-agent workflows  
- Enables **rapid iteration** on prompts, tools, and orchestration logic  
- Simplifies debugging of **tool-augmented LLM behavior**  
- Ensures reliability before downstream integration or deployment  

---
