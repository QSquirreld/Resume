## Практический опыт (Pet Projects)

### ⚙️ End-to-End система анализа речи для постинсультной реабилитации  
[GitHub: Speech-Therapy-Rehab](https://github.com/QSquirreld/Speech-Therapy-Rehab)

- Разработал прототип ML-приложения для мониторинга моторной афазии: ASR (Whisper) → сегментация → вычисление количественных речевых метрик (speech rate, средняя длина фразы, паузы, onset latency).
- Реализовал модульную архитектуру анализа речи и пайплайн обработки аудио до структурированных признаков.
- Подготовил основу для клинической интерпретации динамики показателей речи.
- **Стек:** Python, Whisper, librosa/parselmouth, NLP-постобработка.

---

### ⚙️ Retrieval-Augmented QA система (Vector DB + RAG)  
[GitHub: Weaviate-QA-n-RAG](https://github.com/QSquirreld/Weaviate-QA-n-RAG)

- Построил end-to-end QA-систему на базе bi-encoder ранжирования и векторной БД (semantic + hybrid retrieval).
- Реализовал интеграцию embedding-моделей, near-vector и hybrid поиска, extractive QA и генеративного RAG.
- Оценивал качество через Recall@k, MRR, MAP, nDCG, F1/EM.
- **Стек:** PyTorch, Hugging Face, Weaviate, LLM-generation.

---

### ⚙️ ReAct-агенты с инструментами (Local LLM + Web Search)  
[GitHub: ReAct-Agent-with-Qwen-and-DuckDuckGo](https://github.com/QSquirreld/ReAct-Agent-with-Qwen-and-DuckDuckGo)  
[GitHub: LangChain-Agents-jsonParser-ReAct-with-local-LLM](https://github.com/QSquirreld/LangChain-Agents-jsonParser-ReAct-with-local-LLM)

- Реализовал tool-using LLM-агентов (ReAct) с вызовом внешних инструментов (web search) и многошаговым reasoning.
- Настроил локальный запуск LLM (GGUF + llama-cpp-python), внедрил строгий JSON-парсинг через LangChain OutputParser.
- Реализовал обработку parsing failures и fallback-логики на уровне executor.
- **Стек:** LangChain, local LLM inference, prompt engineering.

---

### ⚙️ Семантическое ранжирование для русскоязычного QA  
[GitHub: Semantic-Ranking-on-Russian-QA-Data](https://github.com/QSquirreld/Semantic-Ranking-on-Russian-QA-Data)

- Обучил и дообучил bi-encoder модели (RuBERT / multilingual E5) для retrieval-задачи.
- Реализовал negative sampling и полноценную систему оценки similarity и ranking-метрик (Pearson/Spearman, Recall@k, MRR, MAP, nDCG).
- Достиг улучшения корреляции cosine-similarity с ~0.76 до ~0.87 после fine-tuning.
- **Стек:** Transformers, PyTorch, ranking evaluation.

---

### ⚙️ NLP-пайплайн: классификация тональности + генерация ответа  
[GitHub: Sentiment-Analysys-and-Text-Generation](https://github.com/QSquirreld/Sentiment-Analysys-and-Text-Generation)

- Разработал end-to-end систему: классификация тональности (3 класса, accuracy ~0.82) → генерация стилизованного ответа через instruction LLM.
- Использовал Hugging Face Trainer, early stopping, confusion matrix, ROUGE и semantic similarity для оценки.
- Реализовал prompt-конструкции и постобработку LLM-вывода (regex extraction).
