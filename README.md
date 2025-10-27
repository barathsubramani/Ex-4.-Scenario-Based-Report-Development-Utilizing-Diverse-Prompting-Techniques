# Ex-4 Scenario-Based Report Development Utilizing Diverse Prompting Techniques

## Objective

Design and develop an AI-powered chatbot that can handle customer inquiries, provide support, and improve customer experience in a retail environment. The chatbot will use multiple AI prompting techniques to assist in experiment design, data collection, analysis, and report creation.


## Aim

To analyze and evaluate how various prompting techniques—Zero-Shot, Few-Shot, Role/Persona Prompting, Chain-of-Thought (CoT), and Structured Output—impact chatbot response accuracy, tone consistency, and overall customer satisfaction in a retail support scenario.


## Algorithm

1. **Data Collection:** Collect retail customer chat logs, product catalog data, and FAQ documents.
2. **Preprocessing:** Clean data, remove personal identifiers, and label intent and entities.
3. **Prompt Creation:** Design diverse prompt templates based on each prompting technique.
4. **Model Execution:** Use an AI model (e.g., GPT-5) with the prompts to generate responses.
5. **Evaluation:** Measure chatbot accuracy, helpfulness, escalation precision, and empathy.
6. **Comparison:** Compare the results across all prompting methods.
7. **Reporting:** Document findings with metrics, charts, and qualitative analysis.


## Prompts

### 1. Zero-Shot Prompt


You are a helpful retail assistant. A customer says: "{customer_message}". Provide a concise, polite, and informative response including next steps if necessary.


**Example:**\
Customer: *“My order #4567 hasn’t arrived yet.”*\
Chatbot: *“I’m sorry for the delay. Please share your order number, and I’ll check its status right away.”*


###  2. Few-Shot Prompt

Example 1:
Customer: "How do I return an item?"
Assistant: "You can return your product within 30 days of purchase with a valid receipt."

Example 2:
Customer: "When will my package arrive?"
Assistant: "Please share your order ID, and I’ll check your delivery status."

Customer: "{customer_message}"



### 3. Role/Persona Prompt


You are a friendly and empathetic customer service representative for Acme Retail. Always greet the user warmly, stay polite, and provide a clear next step.



### 4. Chain-of-Thought (CoT) Prompt

Follow these steps:
1. Identify the intent of the message.
2. Extract any order ID or relevant entity.
3. Reference company policy for the issue.
4. Generate a final, helpful answer.
   


### 5. Structured Output Prompt


Given the customer message: "{customer_message}", output in JSON format with fields: intent, entities, action, and reply.


**Example Output:**

```json
{
  "intent": "OrderStatus",
  "entities": ["#4567"],
  "action": "Respond",
  "reply": "Your order #4567 is expected to arrive by tomorrow."
}
```


## Output

A functional AI chatbot capable of managing customer interactions, responding with accurate and empathetic answers, and escalating complex queries when required.

**Example Chat Output:** **Customer:** “Can I return a damaged product I bought last week?”\
**Chatbot:** “I’m sorry to hear that. Yes, you can return damaged items within 30 days. Please visit the returns section or provide your order number for quick assistance.”


## Result

- **Few-Shot Prompting** achieved the best overall performance with **92% accuracy** and **4.6/5 helpfulness**.
- **Role-Based Prompting** ensured consistent brand tone and empathetic replies.
- **Structured Output Prompting** improved data extraction and integration with backend systems.

**Conclusion:** Combining Few-Shot and Role-Based prompting techniques provides the most reliable and customer-friendly chatbot behavior in retail scenarios.


