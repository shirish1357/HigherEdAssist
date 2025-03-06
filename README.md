# HigherEdAssist: Academic Program Advisor

HigherEdAssist is an interactive AI-driven tool that helps prospective students explore and understand various academic programs. It leverages a **fine-tuned SentenceTransformer model** for generating context-specific embeddings, along with an OpenAI Chat API for conversation flow.

## Features

- **Contextual Program Embeddings**  
  Each program’s description and keywords are combined to form a rich text input, which is then encoded by the fine-tuned model for more accurate recommendations.

- **Recommendation Engine**  
  Users can input their **interests** and **skills**; the tool computes a weighted embedding and compares it against each program’s embedding using cosine similarity.

- **Program Descriptions**  
  A separate tool function provides detailed program descriptions, including prerequisites and career outcomes.

- **Gradio UI**  
  A user-friendly Gradio interface allows you to chat with HigherEdAssist, ask for program details, or request recommendations.

## Concept

### Project Idea
HigherEdAssist aims to bridge the gap between prospective students and the wealth of academic programs offered at universities. By leveraging a **fine-tuned SentenceTransformer model**, we can capture domain-specific nuances of program descriptions, prerequisites, and outcomes. This approach enables the system to make more accurate and context-rich recommendations.

### Execution
1. **Data Preparation**  
   - We compile a dictionary (`program_info`) of academic programs, each containing a detailed description, prerequisites, career outcomes, and a list of keywords.
   - The description and keywords are concatenated to form a “contextual text,” which is then converted into embeddings.

2. **Fine-Tuned Model**  
   - A base model (e.g., `all-MiniLM-L6-v2`) is fine-tuned on domain-specific text, such as academic program summaries or descriptions.
   - This produces a model that better understands the language and key concepts of higher education.

3. **Embedding & Similarity**  
   - For each program, we precompute its embedding using the fine-tuned model.
   - When a user enters their interests and skills, we create a combined embedding (with adjustable weights, e.g., 60% interests / 40% skills).
   - We then compute the cosine similarity between the user’s combined embedding and each program’s embedding to rank and recommend the most relevant programs.

4. **Tool Calls & Chat**  
   - The system uses an OpenAI Chat API that can call specific tools: one for program descriptions, another for generating recommendations.
   - Gradio provides a web-based chat interface where users can ask questions or request recommendations in natural language.

5. **Outcome**  
   - By blending AI-based language understanding with domain knowledge of academic programs, HigherEdAssist offers a friendly, interactive way for students to discover suitable programs and gather important details.
