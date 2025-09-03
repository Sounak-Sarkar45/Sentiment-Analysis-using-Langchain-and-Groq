<h1>💬 Sentiment Analysis RAG with Groq &amp; FAISS</h1>

<p>
This project demonstrates how to build a <b>Retrieval-Augmented Generation (RAG)</b> pipeline 
for analyzing customer sentiment data stored in CSV files.  
It combines <b>LangChain</b>, <b>Groq LLM</b>, <b>FAISS</b>, and <b>FastEmbed embeddings</b> 
to enable natural language queries over customer reviews.  
The system retrieves relevant customer feedback and synthesizes them into 
clear, human-like insights.
</p>

<hr>

<h2>🚀 Features</h2>
<ul>
  <li><b>CSV Data Loading</b> – Load structured sentiment datasets with review text and metadata.</li>
  <li><b>Text Splitting</b> – Break large documents into manageable chunks using <code>RecursiveCharacterTextSplitter</code>.</li>
  <li><b>Vector Database</b> – Store and search review embeddings with <b>FAISS</b>.</li>
  <li><b>RAG Function</b> – Retrieve the most relevant reviews and pass them into the LLM for answer synthesis.</li>
  <li><b>Groq LLM Integration</b> – Use <b>LLaMA-3.1</b> hosted on Groq for natural, accurate responses.</li>
  <li><b>Guided Answers</b> – Ensures answers exclude metadata and are written in a natural tone.</li>
</ul>

<hr>

<h2>🛠️ Tech Stack</h2>
<ul>
  <li><b>Python</b> – Pipeline orchestration.</li>
  <li><b>Pandas + CSVLoader</b> – Load structured review datasets.</li>
  <li><b>LangChain</b> – Framework for embeddings, text splitting, and RAG logic.</li>
  <li><b>FAISS</b> – Vector database for similarity search.</li>
  <li><b>FastEmbed</b> – Embeddings model (<code>BAAI/bge-large-en-v1.5</code>) for semantic retrieval.</li>
  <li><b>Groq LLM</b> – For answer synthesis and summarization.</li>
  <li><b>LangSmith</b> – Optional tracing and monitoring of LLM interactions.</li>
</ul>

<hr>

<h2>📂 Workflow</h2>
<ol>
  <li><b>Load CSV</b> – Import customer sentiment dataset with reviews and metadata.</li>
  <li><b>Chunk Reviews</b> – Split review text into overlapping chunks for embedding.</li>
  <li><b>Embed &amp; Store</b> – Convert text chunks into vector embeddings and index in FAISS.</li>
  <li><b>Query RAG</b> – Perform similarity search to retrieve the top <i>k</i> relevant reviews.</li>
  <li><b>Answer Generation</b> – Send retrieved reviews to Groq LLM to generate a concise answer.</li>
  <li><b>Final Output</b> – Receive an executive-style summary without metadata leakage.</li>
</ol>

<hr>

<h2>📊 Example Use Case</h2>
<p><b>Business Scenario:</b><br>
A company wants to understand customer sentiment across different platforms (Twitter, Facebook, etc.).  
They ask:</p>

<blockquote>
“Which sources have the highest proportion of positive reviews?”
</blockquote>

<ul>
  <li><b>Retrieved Context:</b> A set of customer reviews from different sources (Twitter, Reddit, etc.).</li>
  <li><b>System Output:</b> 
    <i>“Most positive reviews are concentrated on Twitter and Instagram, where customers frequently highlight ease of use and product reliability. Other sources such as forums contain more mixed feedback.”</i>
  </li>
</ul>

<hr>

<h2>🔐 Environment Variables</h2>
<p>Create a <code>.env</code> file and include:</p>
<ul>
  <li><code>GROQ_API_KEY</code> → Groq LLM API key</li>
</ul>

<hr>

<h2>📈 Potential Extensions</h2>
<ul>
  <li>✅ Extend to multi-lingual review analysis.</li>
  <li>✅ Add visualization dashboards for sentiment distribution by source, time, or geography.</li>
  <li>✅ Integrate with real-time streams (e.g., Twitter API) for live sentiment monitoring.</li>
  <li>✅ Deploy as a web app via <b>Streamlit</b> or <b>FastAPI</b>.</li>
</ul>

<hr>
