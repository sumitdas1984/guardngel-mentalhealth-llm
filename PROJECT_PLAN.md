# GuardnGel Mental Health LLM – Project Plan

## **Goal**

Develop a **domain‑specialized LLaMA 3.2 (1B)** model fine‑tuned for **youth mental health support**.  
The model will power GuardnGel's platform to provide **empathetic, stigma‑breaking, and proactive guidance**.

## **Phases**

### **Phase 1: Requirements & Design (1 week)**

- Define model scope & limitations.
- Draft AI persona/system prompt.
- Map GuardnGel use cases (screening, psychoeducation, stigma‑breaking).

### **Phase 2: Data Strategy (2–3 weeks)**

- Gather public datasets (CounselChat, mental health forums).
  There are good open datasets for counseling/mental‑health:
  - CounselChat (Hugging Face): Real mental health Q&A from online forums.
  - Reddit Mental Health Support (Hugging Face): Reddit posts about mental health struggles.
  - Mental Health Counselor Conversations (Curated in research papers; can extract dialogues).
- Generate synthetic dialogues with LLMs.
- Mental health dataset (~20k–50k instruction‑response pairs).
- Data cleaning & formatting scripts.
- Collaborate with experts for real-world scenarios.

### **Phase 3: Fine‑Tuning (3–4 weeks)**

- Use **QLoRA** to fine‑tune LLaMA 3.2 (1B).
- Train with curated & synthetic data.
- Evaluate for empathy, accuracy, and tone.

### **Phase 4: Safety Layer (1–2 weeks)**

- Build crisis keyword detection & escalation prompts.
- Add disclaimers & ethical guidelines.

### **Phase 5: Conversion & Deployment (2 weeks)**

- Merge LoRA adapters & convert to **GGUF**.
- Create **Ollama Modelfile** for local inference.
- Deploy via **FastAPI** for integration.

### **Phase 6: Testing & Iteration (2–3 weeks)**

- Domain expert reviews & youth focus groups.
- Continuous improvements based on feedback.

## **Deliverables**

- Fine‑tuned **mental health model** in GGUF format.
- **Ollama deployment** with system instructions.
- **FastAPI service** exposing chat endpoints.
- Safety & moderation scripts.

## **Tech Stack**

- **Transformers + PEFT (QLoRA)**
- **Datasets (Hugging Face)**
- **llama.cpp** for GGUF conversion
- **Ollama** for inference
- **FastAPI** for deployment

## **Success Metrics**

- 85%+ expert‑rated empathetic & helpful responses.
- 0 unsafe outputs in moderated test set.
- <2s inference latency on target hardware.
- Positive engagement from youth pilot testing.
