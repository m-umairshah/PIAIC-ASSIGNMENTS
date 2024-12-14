## **1. Messages**
The `messages` parameter stores the entire conversation between the user and the AI. It has three roles:
- **System**: Tells the AI how to behave (e.g., polite, formal).  
- **User**: Includes the input or question asked by the user.  
- **Assistant**: Holds the AI's response.

### **Example**
```json
[
  {"role": "system", "content": "You are a helpful assistant."},
  {"role": "user", "content": "What is AI?"},
  {"role": "assistant", "content": "AI stands for Artificial Intelligence."}
]
```

---

## **2. Model**
The `model` parameter lets you choose which AI model to use. Each model has different capabilities. For example:
- `gemini-1`: Smarter but slower and costly.
- `gemini-1-turbo`: Faster and cheaper.

### **Example**
```json
"model": "gemini-1-turbo"
```

---

## **3. Max Completion Tokens**
This parameter controls how long the AI’s response can be. Tokens are parts of words or whole words. It is useful for limiting the length of the reply.

### **Example**
```json
"max_tokens": 100
```

---

## **4. n**
The `n` parameter decides how many different responses the AI should give for the same input. This is useful if you want multiple options to choose from.

### **Example**
```json
"n": 3
```
The AI will give three different responses for the same question.

---

## **5. Stream**
The `stream` parameter decides whether the response should appear in real-time (like typing) or all at once.  
- **True**: The response is shown in parts, as if typing.  
- **False**: The entire response is displayed at once.

### **Example**
```json
"stream": true
```

---

## **6. Temperature**
The `temperature` parameter controls how creative or random the AI’s responses are.  
- **Low value (e.g., 0.2)**: Makes the answers more focused and serious.  
- **High value (e.g., 1.0)**: Makes the answers creative and diverse.

### **Example**
```json
"temperature": 0.7
```

---

## **7. Top_p**
The `top_p` parameter is another way to control creativity. It limits the AI’s word choices to the most probable ones.  
- **Small value (e.g., 0.5)**: Focused response.  
- **Large value (e.g., 0.9)**: More variety in the response.

### **Example**
```json
"top_p": 0.8
```

---

## **8. Tools**
The `tools` parameter allows the AI to use extra resources, like a calculator or a search engine. This makes the AI more capable.

### **Example**
```json
"tools": ["calculator", "web-search"]
```

---

## **How These Parameters Work Together**
These parameters work together to control the AI's behavior. For example:
- `Messages` provides context for the conversation.  
- `Model` decides the quality of the response.  
- `Temperature` and `Top_p` control the creativity.  
- `Max Completion Tokens` limits the length of the reply.  
- `Stream` improves the experience for real-time apps.
