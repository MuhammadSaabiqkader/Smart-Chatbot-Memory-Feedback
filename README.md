# Smart-Chatbot-Memory-Feedback
An AI chatbot with conversation memory and user feedbackSmart Chatbot with Memory & Feedback

An AI-powered conversational chatbot built with Python, Hugging Face Transformers, and Gradio. This project combines conversational context, simple personal memory, and user feedback in an interactive chat interface.

Overview

Smart Chatbot with Memory & Feedback is a learning project that explores how language models can generate conversational responses while using recent chat history and a small collection of saved user facts.

The application uses the pretrained Facebook BlenderBot 400M Distill model and provides a simple interface for chatting, saving supported memories, and rating responses.

Features

- AI-powered conversations — Generate responses using a pretrained BlenderBot model.
- Conversation context — Include recent messages when generating a reply.
- Simple personal memory — Save, retrieve, and forget selected personal facts.
- Feedback collection — Rate responses as helpful or not helpful.
- Local JSON storage — Save memory and feedback records in local JSON files.
- Interactive interface — Chat through a Gradio web interface.
- GPU support — Use CUDA when an available compatible GPU is detected; otherwise, use the CPU.

Tech Stack

Technology| Purpose
Python| Core programming language
PyTorch| Model execution and inference
Hugging Face Transformers| Loading and using BlenderBot
BlenderBot 400M Distill| Conversational language model
Gradio| Interactive chatbot interface
JSON| Local memory and feedback storage
Jupyter Notebook| Development and experimentation

Project Structure

Smart-Chatbot-Memory-Feedback/
├── README.md
└── Smart_Chatbot_Memory_Feedback_FIXED.ipynb

The files "user_memory.json" and "chatbot_feedback.json" are created locally when the notebook runs and saves memory or feedback.

Getting Started

Prerequisites

- Python
- Jupyter Notebook or Google Colab
- An internet connection to download the pretrained model and required packages
- Sufficient RAM and storage for model execution

1. Clone the Repository

git clone https://github.com/Muhammadsaabiqkader/Smart-Chatbot-Memory-Feedback.git
cd Smart-Chatbot-Memory-Feedback

2. Install Dependencies

Run the following command in a notebook cell:

%pip install -U transformers torch gradio

3. Run the Notebook

Open "Smart_Chatbot_Memory_Feedback_FIXED.ipynb" in Jupyter Notebook or Google Colab.

Execute the notebook cells from top to bottom to install the dependencies, load the model, initialize memory and feedback storage, and launch the chatbot interface.

Note: The first model download may take some time. CPU execution may also be slower than GPU execution.

Try the Chatbot

The notebook supports the following example commands:

Message| Purpose
"remember my name is Arun"| Save a name
"remember I am learning Python"| Save a personal fact
"what do you remember about me?"| Retrieve saved facts
"forget my name"| Remove the saved name

You can also continue a conversation and rate the latest response using the Helpful and Not helpful buttons.

Memory & Feedback Storage

The application uses two local files:

- "user_memory.json" — Stores supported personal facts.
- "chatbot_feedback.json" — Stores feedback ratings, timestamps, and associated conversation messages.

These files are intended for a simple single-user learning demonstration. Feedback collection does not automatically retrain or fine-tune the language model.

Limitations

- The memory system recognizes specific command patterns rather than arbitrary natural language.
- BlenderBot may produce inaccurate, repetitive, or contextually irrelevant responses.
- The notebook does not provide separate accounts or isolated memory for multiple users.
- Local files in temporary hosted notebook environments may be lost when the runtime resets.
- Model quality and response speed depend on the available hardware.

Privacy & Responsible Use

This is an educational prototype, not a production-ready chatbot.

Avoid entering passwords, financial details, confidential information, or other sensitive personal data. Saved memory and feedback files may contain conversation-related information, so handle them carefully before sharing the project.

Future Enhancements

- Add persistent storage with a database.
- Improve memory retrieval and natural-language memory commands.
- Support multiple users with separate conversation histories.
- Build a more advanced web interface.
- Add automated tests and structured error handling.
- Explore improved conversational models.

Author

Muhammad Saabiq Kader

Computer Science and Business Systems | AI & Machine Learning Enthusiast

- GitHub: "Muhammadsaabiqkader" (https://github.com/Muhammadsaabiqkader)

---

Developed as an educational project to explore conversational AI, memory management, and feedback collection.
