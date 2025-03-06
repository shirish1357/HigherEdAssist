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

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/<your-username>/HigherEdAssist.git
   cd HigherEdAssist
