# 📚 PDF Knowledge Extractor & Multimodal RAG Assistant

## 💡 Project Idea

A smart system designed to extract and analyze content from complex academic files — even those containing scanned images, tables, or unstructured layouts.  
The extracted content is summarized and stored in a knowledge base, then used in a **Multimodal Retrieval-Augmented Generation (RAG)** pipeline to answer user questions intelligently.

Unlike standard RAG systems that work only with text, this solution supports **text, tables, and images** — making it ideal for highly structured or visual documents such as scientific papers or medical leaflets.

---

## 🧠 System Components

### 🔍 PDF Parsing & Content Extraction
- Uses the `unstructured` library to split PDF content into **text**, **tables**, and **images**.
- Handles messy layouts, scanned pages, and multi-format documents.

### 🖼️ OCR for Embedded Images
- Applies `pytesseract` to extract text from embedded figures or scanned pages.
- Converts all visual content into searchable chunks for the RAG pipeline.

### 📑 Summarization
- Leverages **LLaMA 3** via **Groq** to summarize raw extracted chunks.
- Summaries are stored and later used to improve RAG response quality.

### 🧠 Vector Storage & Document Indexing
- Embeds all content (text, tables, image text) using **LangChain**.
- Stored in a **Chroma** vector DB, with metadata indicating content type (`text`, `table`, or `image`).

### 💬 Multimodal RAG (Retrieval-Augmented Generation)
- Retrieves the most relevant text/table/image chunks based on user queries.
- Combines multiple types of content to generate rich, contextual answers.

---

## 🛠️ Tech Stack

| Tool / Library         | Purpose                                     |
|------------------------|---------------------------------------------|
| `unstructured`         | PDF content chunking and preprocessing      |
| `pytesseract`          | OCR for image-based text                    |
| `LangChain`            | Chaining logic and embedding queries        |
| `Chroma`               | Vector database for fast semantic search    |
| `Groq - LLaMA 3`       | Summarization and final response generation |
| `matplotlib` + `PyMuPDF` | Visual annotation for debugging             |

---

## 🌟 Features

✅ Multimodal RAG — supports scanned images, tables, and text  
✅ Automatically detects and extracts structured medical/scientific content  
✅ Classifies and organizes content types intelligently  
✅ Fast, contextual answers with reference to original PDF locations  
✅ Fully automated — no manual effort required  

---

## 🧪 Example Usage

1. Upload a scientific or medical PDF file  
2. The system processes it and stores summarized chunks  
3. Ask a question like:  
   _“What risks are associated with this drug?”_  
4. System retrieves matching content (even from tables/images) and generates a high-quality answer  
5. Displays the source with page number and visual if available

---

<div align="center">
  
<img src="https://github.com/user-attachments/assets/61f29223-83ed-4e71-a952-062d63b6b5af" alt="Screenshot 1" width="400" style="margin: 10px;"  />
<img src="https://github.com/user-attachments/assets/eb5d33b9-d9f4-4ab5-a1e3-5c4fbeeea7a1"  alt="Screenshot 1" width="400" style="margin: 10px;"  />
<img src="https://github.com/user-attachments/assets/ae1e9f7c-abb0-4bcf-962f-870b2abd47dd"  alt="Screenshot 1" width="400" style="margin: 10px;"  />
<img src="https://github.com/user-attachments/assets/3bc8def4-5fa1-4b55-bd48-ca9325daeeba"  alt="Screenshot 1" width="400" style="margin: 10px;"  />
<img src="https://github.com/user-attachments/assets/3bc8def4-5fa1-4b55-bd48-ca9325daeeba"  alt="Screenshot 1" width="400" style="margin: 10px;"  />
<img src="https://github.com/user-attachments/assets/1c1c53a7-c828-4df5-a3b2-6bdc8460e70d"  alt="Screenshot 1" width="400" style="margin: 10px;"  />

</div>

---

🤝 Contribution
Feel free to fork the repo, open issues, or submit pull requests. Suggestions and improvements are welcome!

## 📫 Contact

If you have any questions or want to collaborate, feel free to reach out to me:

- ✉️ **Email:** [alaaismailmohamed144@gmail.com](mailto:alaaismailmohamed144@gmail.com)  
- 🔗 **LinkedIn:** [Alaa Ismail](https://www.linkedin.com/in/alaa-ismail-b09493264)


