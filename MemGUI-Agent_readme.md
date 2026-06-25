# MemGUI-Agent: An End-to-End Long-Horizon Mobile GUI Agent with Proactive Context Management

## 🌟 Simple Explanation
When AI agents try to perform long and complex tasks on a smartphone, they usually try to remember *everything* they have done so far. This leads to information overload, where the AI gets confused and forgets critical details. 

**MemGUI-Agent** solves this by actively managing its own memory. Instead of passively recording every click and swipe, it uses a system called **ConAct (Context-as-Action)** to continuously summarize and fold its past actions and screen states, keeping its memory small, neat, and highly effective for long-horizon tasks.

## 📊 Memory Management Comparison (Diagram)

```mermaid
flowchart LR
    subgraph Traditional ReAct Agent
    A[Step 1] --> B[Step 1+2] --> C[Step 1+2+3] --> D[Prompt Explosion & Forgetting]
    end

    subgraph MemGUI-Agent (ConAct)
    E[Step 1] --> F{Active Context Folding}
    F --> G[Compact Folded History]
    F --> H[Folded UI State]
    G & H --> I[Clear Context for Step 2]
    end
```

## 🧠 Key Innovations
- **ConAct Framework:** Treats context management as a "first-class action". The AI actually executes commands to update its own memory.
- **Structured Memory Fields:** The context is maintained in three concise fields:
  1. *Folded Action History*
  2. *Folded UI State*
  3. *Recent Step Record*
- This approach avoids the common pitfall of "ReAct-style prompting" which dilutes important information over long trajectories.

## 📈 Metrics & Full Details
- **ArXiv ID:** [2606.19926](https://arxiv.org/abs/2606.19926)
- **Dataset (MemGUI-3K):** The team introduced a massive new dataset featuring **2,956 trajectories** with full ConAct annotations for supervised training and offline analysis.
- **Model (MemGUI-8B-SFT):** Trained an **8 Billion parameter** model on the MemGUI-3K dataset.
- **Performance:** Achieved **State-of-the-Art (SOTA)** open-data performance on the MemGUI-Bench. It also demonstrated excellent generalization capabilities on out-of-distribution benchmarks like MobileWorld.

## 🔗 Resources
- **Project Website:** [memgui-agent.github.io](https://memgui-agent.github.io/)
