# Disneyland Guest Review Summarization & Response Pipeline

This project builds a GenAI-powered system to automatically process and respond to Disneyland guest reviews.

### What It Does
1. **Summarizes** long or noisy reviews using Hugging Face’s BART model
2. **Analyzes sentiment** (Positive/Negative) using a classification pipeline
3. **Generates responses**:
   - Rule-based fallback for offline testing
   - GPT-3.5-driven responses that adapt tone, reference details, and stay on-brand

### Example Output

**Input Review**  
_"It was a shame that so much of the park was closed when we visited, but the parades were amazing!"_

**Summary**  
"Much of the park was closed, but parades were amazing."

**Sentiment**  
`NEGATIVE`

**Final Response (via OpenAI)**  
_"We’re sorry to hear about the closures during your visit. We’re thrilled you enjoyed the parades and hope to welcome you back for an even more magical experience. Have a magical day! – Jenna, Disneyland Guest Services"_

### Use Cases
- CRM tools
- Automated TripAdvisor moderation
- Tone-aware customer support scaling

### Tech Stack
- Hugging Face Transformers
- OpenAI API (GPT-3.5)
- Python + pandas

### 🧪 How to Run Locally

```bash
# 1. Clone the repository
git clone git@github.com:chrisbacani/disneyland-genai-responder.git
cd disneyland-genai-responder

# 2. Install dependencies
pip install -r requirements.txt

# 3. Create a .env file with your OpenAI API key
echo "OPENAI_API_KEY=your_openai_key_here" > .env

# 4. Launch the notebook
jupyter notebook

---

> Author: **Christopher Bacani**, 2025
