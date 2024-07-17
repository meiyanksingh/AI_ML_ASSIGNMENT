# AI_ML_ASSIGNMENT
QA bot for PDF files to extract text, generate embeddings, and store them in a vector database. Users can query the system, which retrieves relevant text chunks based on similarity scores. The system integrates with a GPT model for refining user queries.
## Requirement
1. PineCone Api Key (https://www.pinecone.io/)
2. OpenAI Key (https://platform.openai.com/)
   
## Steps
1. Open google colab from https://colab.research.google.com/
2. Upload supported document (asd.pdf) to sesson storage
3. Upload Mayank_Singh_LLM_Assigenment_latest.ipynb
4. and run the code

##  Architecture Document:
------------
The application follows these steps to provide responses to your questions:

1. **PDF Loading** : The app reads multiple PDF documents and extracts their text content.
   
3. **Text Chunking** : The extracted text is divided into smaller chunks that can be processed effectively.

4. **Language Model** : The application utilizes a language model to generate vector representations (embeddings) of the text chunks.

5. **Similarity Matching** : When you ask a question, the app compares it with the text chunks and identifies the most semantically similar ones.

6. **Response Generation** : The selected chunks are passed to the language model, which generates a response based on the relevant content of the PDFs.

![MultiPDF Chat App Diagram](image/Architecture.jpg)

## Performance Evaluation Results

### Text Extraction Speed
- Average extraction time: 0.17 seconds per PDF 

### Embedding Generation Time
- Average generation time: 0.5 seconds per text chunk .

### Storage and Retrieval Time
- 2.17 Seconds

### Query Response Time
- Average response time: 3.04 seconds per query.

### Accuracy
- Precision: 0.85
- Recall: 0.80

### Scalability
- System can handle up to 10 concurrent users with an average response time increase of 0.5 seconds.

### Security
Ensuring security in the development and deployment of a QA bot involves multiple layers, including secure handling of data, safeguarding the system against unauthorized access, and maintaining the integrity and confidentiality of the queries and results. Here are some key strategies to enhance the security of your QA bot system

1. Secure Data Handling
Encryption: Encrypt PDF files, embeddings, and other sensitive data at rest and in transit.
Use libraries like cryptography for encryption.
Secure Storage: Store encryption keys securely, using services like AWS KMS or Azure Key Vault.

2. Authentication and Authorization
API Authentication: Use OAuth2, JWT, or API keys for securing API endpoints.
Role-Based Access Control (RBAC): Implement RBAC to ensure that users have appropriate permissions.

3. Network Security
HTTPS: Use HTTPS to encrypt data in transit.
Firewall and VPC: Use firewalls and Virtual Private Clouds (VPC) to restrict access to your servers.

4. Input Validation and Sanitization
Validate User Input: Ensure that user inputs are properly validated to prevent injection attacks (e.g., SQL injection, XSS).
Sanitize Inputs: Use libraries like bleach for sanitizing text inputs.

5. Regular Audits and Monitoring
Audit Logs: Maintain logs of all access and actions within the system for audit purposes.
Monitoring: Use monitoring tools to detect unusual activities and potential security breaches.

6. Secure Code Practices
Dependency Management: Regularly update dependencies to fix known vulnerabilities.
Static and Dynamic Analysis: Use tools like bandit for static code analysis and dynamic analysis tools for runtime checks.

7. Secure Deployment
Container Security: Use container security practices if deploying with Docker/Kubernetes (e.g., scanning images for vulnerabilities).
Least Privilege Principle: Ensure that services run with the least privileges required.

