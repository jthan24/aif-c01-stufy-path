# aif-c01-stufy-path



# **AWS Certified AI Practitioner (AIF-C01) Execution Plan**

An intensive, 7-day preparation schedule and tracking framework designed to achieve readiness for the AIF-C01 examination.

---

# **Plan Overview & Domain Weightings**

| Domain | Exam Weight | Focus Area |
| :---- | :---- | :---- |
| **Domain 1: Fundamentals of AI and ML** | 20% | AI/ML concepts, learning paradigms, pipeline phases |
| **Domain 2: Fundamentals of Generative AI** | 24% | LLMs, FM selection, RAG, Fine-tuning, Prompting |
| **Domain 3: Applications of Foundation Models** | 28% | Bedrock, SageMaker, Model evaluation, Cost optimization |
| **Domain 4: Guidelines for Responsible AI** | 14% | Safety, security, bias, transparency, governance |
| **Domain 5: Security, Compliance, and Governance** | 14% | Data protection, IAM, regulatory compliance, monitoring |

---

# **Day 1: AI/ML Fundamentals & Core Cloud Prerequisites**

* **Target Domain:** Domain 1: Fundamentals of AI and ML (20%)  
* **Primary AWS Services:** Amazon SageMaker (Overview), AWS Cloudtrail, Amazon CloudWatch

## **90-Minute Execution Schedule**

| Time Allocation | Focus Area | Key Deliverables & Actions |
| :---- | :---- | :---- |
| **00:00 – 00:25** | **Core Concepts** | Review Supervised, Unsupervised, and Reinforcement Learning; Overfitting vs. Underfitting; Training/Validation/Test splits. |
| **00:25 – 00:50** | **ML Lifecycle** | Deep dive into Problem Formulation, Data Prep, Model Training, Tuning, Deployment, and Continuous Monitoring. |
| **00:50 – 01:15** | **AWS ML Infrastructure** | Study high-level architecture of Amazon SageMaker (Studio, Notebooks, Autopilot, Model Registry). |
| **01:15 – 01:30** | **Knowledge Check** | Complete 10 domain-specific practice questions and log all missed items in the Error Log below. |

## **Resources & Hands-on Workshops**

* **Official Documentation:** [Amazon Bedrock Developer Experience](https://aws.amazon.com/bedrock/) and [Amazon SageMaker Overview](https://aws.amazon.com/sagemaker/).  
* **Hands-on Workshop:** [Amazon Bedrock Fundamentals Workshop](https://catalog.workshops.aws/amazon-bedrock/en-US) for Generative AI Development.

---

# **Day 2: Generative AI Architecture & Model Selection**

* **Target Domain:** Domain 2: Fundamentals of Generative AI (24%)  
* **Primary AWS Services:** Amazon Bedrock Foundation Models (Claude, Titan, Llama), SageMaker JumpStart

## **90-Minute Execution Schedule**

| Time Allocation | Focus Area | Key Deliverables & Actions |
| :---- | :---- | :---- |
| **00:00 – 00:25** | **GenAI Architecture** | Master Foundation Models (FMs), Transformers, Self-Attention mechanisms, and Tokens. |
| **00:25 – 00:50** | **Model Selection Matrix** | Evaluate tradeoffs between latency, throughput, model size, context window, and modality. |
| **00:50 – 01:15** | **Bedrock vs. SageMaker** | Contrast managed FMs (Amazon Bedrock) with customizable model hosting (SageMaker JumpStart). |
| **01:15 – 01:30** | **Knowledge Check** | Complete 10 domain-specific practice questions; log errors. |

## **Resources & Hands-on Workshops**

* **Official Documentation:** [Amazon Bedrock Knowledge Bases](https://aws.amazon.com/bedrock/knowledge-bases/) and [Building GraphRAG Applications](https://aws.amazon.com/blogs/machine-learning/build-graphrag-applications-using-amazon-bedrock-knowledge-bases/).  
* **Hands-on Workshop:** [Building Agentic AI Platform Workshop](https://catalog.us-east-1.prod.workshops.aws/workshops/3f49be39-c62b-40a2-975b-be9bf626526a).

---

# **Day 3: Prompt Engineering & Model Customization**

* **Target Domain:** Domain 2: Fundamentals of Generative AI (24%) & Domain 3: Applications of FMs (28%)  
* **Primary AWS Services:** Amazon Bedrock (Playground, Custom Models), SageMaker Model Training

## **90-Minute Execution Schedule**

| Time Allocation | Focus Area | Key Deliverables & Actions |
| :---- | :---- | :---- |
| **00:00 – 00:25** | **Prompt Techniques** | Study Zero-shot, Few-shot, Chain-of-Thought (CoT), System Prompts, and Hyperparameters (Temperature, Top-P, Top-K). |
| **00:25 – 00:50** | **Customization Strategies** | Compare In-Context Learning, Retrieval-Augmented Generation (RAG), Domain Adaptation, and Fine-Tuning (LoRA/PEFT). |
| **00:50 – 01:15** | **RAG Infrastructure** | Review Vector Embeddings, Knowledge Bases for Amazon Bedrock, and OpenSearch Service Vector Engine. |
| **01:15 – 01:30** | **Knowledge Check** | Complete 10 domain-specific practice questions; log errors. |

## **Resources & Hands-on Workshops**

* **Official Documentation:** [Amazon Bedrock Overview & Prompting](https://aws.amazon.com/bedrock/).  
* **Hands-on Workshop:** [Practical AI Implementation Workshop](https://aws.amazon.com/training/).

## **Terms**

Prompt: *“explica esto para un dev backend: Técnicas documentadas en Training Jobs: SFT, DPO, RLVR, RLAIF, PPO (Nova), CPT.*”

1\. CPT (Continual Pre-Training)

* ¿Qué es en IA?: Preentrenamiento continuo. El modelo lee millones de documentos de texto plano sin un formato de pregunta/respuesta para aprender jerga, idiomas o dominios específicos.  
* Analogía Backend: Poblar una base de datos nueva con un dump masivo de producción.  
* Explicación: Imagina que heredas un sistema bancario con su propio framework propietario. Antes de escribir APIs, necesitas que tu entorno conozca todas las librerías y diccionarios del banco. CPT no le enseña al modelo a responder comandos; solo le da el "contexto crudo" y el vocabulario técnico (por ejemplo, aprender leyes médicas o código de programación) para que el modelo "sepa de qué habla" el sistema.

2\. SFT (Supervised Fine-Tuning)

* ¿Qué es en IA?: Ajuste fino supervisado. Se entrena al modelo con pares estructurados de Input (instrucción) y Output (respuesta ideal).  
* Analogía Backend: Escribir las primeras pruebas de integración (Integration Tests) basadas en requerimientos.  
* Explicación: Aquí es donde transformas el modelo de un "lector de documentos masivo" a un asistente funcional (API). Le pasas un dataset estructurado como un JSON: {"prompt": "Genera un script de Docker", "completion": "FROM node:..."}. El modelo aprende el formato "Request-Response" que esperas en producción.

3\. DPO (Direct Preference Optimization)

* ¿Qué es en IA?: Optimización directa de preferencias. El modelo recibe un prompt y dos respuestas posibles: una "buena" (aceptada) y una "mala" (rechazada), y ajusta sus pesos directamente matemáticamente para elegir la buena.  
* Analogía Backend: Pruebas A/B en producción con flag de aprobación automática.  
* Explicación: En lugar de entrenar a otro modelo para que evalue lo que está bien (como en PPO), usas un dataset de preferencias. Es como si en tus logs guardaras: Request A \-\> Response Ganadora (200 OK) y Request A \-\> Response Perdedora (500 Error / Lenta). El modelo ajusta sus parámetros internos directamente para "asemejarse" a las respuestas ganadoras y alejarse de las perdedoras, sin intermediarios. Es muy eficiente en recursos de cómputo.

4\. PPO (Nova)

* ¿Qué es en IA?: Proximal Policy Optimization (en la arquitectura Nova de Amazon/Bedrock). Es un algoritmo clásico de Aprendizaje por Refuerzo (RLHF) que usa un modelo secundario (Reward Model) que actúa como "juez" para dar una puntuación a las respuestas.  
* Analogía Backend: Un pipeline con un Linter estricto y un módulo de QA automatizado en tiempo de ejecución.  
* Explicación: El modelo genera una respuesta. Un segundo microservicio (el Reward Model) la evalúa y le asigna un score (ej. de 0 a 10). Si el score es bajo, el modelo se "castiga" y recalcula; si es alto, se premia. El apellido Nova implica que está optimizado para la infraestructura cloud de AWS, manejando la sincronización de estos dos modelos en paralelo de manera distribuida (sharding de memoria, optimización de red) para que el pipeline de entrenamiento no sufra cuellos de botella de infraestructura.

5\. RLVR (Reinforcement Learning from Verifiable Rewards)

* ¿Qué es en IA?: Aprendizaje por refuerzo a partir de recompensas verificables. En lugar de que un humano o un modelo "juez" diga si la respuesta es buena, se usa un entorno de ejecución real (un compilador, un validador matemático) para verificarla.  
* Analogía Backend: Un pipeline de CI/CD que corre npm test o ejecuta código en un Sandbox.  
* Explicación: Muy usado para modelos de código (Coding LLMs) o matemáticas. El modelo genera un script de Python para resolver un problema. El Training Job ejecuta el script en un contenedor aislado (Sandbox). ¿El script arrojó el output correcto y pasó los asserts unitarios? Recompensa positiva. ¿Dio un SyntaxError? Recompensa negativa. No hay subjetividad: el código funciona o no funciona.

6\. RLAIF (Reinforcement Learning from AI Feedback)

* ¿Qué es en IA?: Aprendizaje por refuerzo a partir del feedback de otra IA. Es igual a RLHF (human feedback), pero reemplazando los evaluadores humanos por un modelo más grande y potente (como GPT-4 o Claude) para etiquetar qué respuesta es mejor.  
* Analogía Backend: Usar herramientas de análisis estático avanzadas (SaaS) como SonarQube para auditar tu código automáticamente.  
* Explicación: Escalar humanos para que digan qué respuesta es mejor es costoso y lento (no escala horizontalmente). En RLAIF, creas un cluster de "LLMs Jueces" con un prompt estricto de evaluación. Estos jueces procesan millones de respuestas por segundo, generando logs de recompensa que alimentan el entrenamiento de tu modelo base. Automatización de QA a escala masiva.

---

Resumen del ciclo de vida para un Dev:

1. CPT: Creas la base de conocimiento cruda del sistema.  
2. SFT: Defines el contrato de la API (Input/Output).  
3. DPO / PPO: Refinas las respuestas para que la experiencia de usuario sea óptima basándote en logs de éxito/error.  
4. RLVR: Validás que las respuestas técnicas (código/números) compilen y pasen los tests unitarios.  
5. RLAIF: Automatizas la etapa de QA usando arquitecturas distribuidas de IA evaluando a IA.

---

# **Day 4: Managed AI Services & Application Integration**

* **Target Domain:** Domain 3: Applications of Foundation Models (28%)  
* **Primary AWS Services:** Amazon Q, Comprehend, Rekognition, Polly, Transcribe, Kendra, Textract

## **90-Minute Execution Schedule**

| Time Allocation | Focus Area | Key Deliverables & Actions |
| :---- | :---- | :---- |
| **00:00 – 00:30** | **Amazon Q Suite** | Differentiate Amazon Q Business, Amazon Q Developer, and Amazon Q Apps setup and use cases. |
| **00:30 – 00:55** | **Vision & Text Services** | Review Rekognition (image/video), Textract (document extraction), Transcribe (audio-to-text), Polly (text-to-audio). |
| **00:55 – 01:15** | **NLP & Search** | Study Comprehend (sentiment/entities) and Kendra (enterprise search). |
| **01:15 – 01:30** | **Knowledge Check** | Complete 10 domain-specific practice questions; log errors. |

## **Resources & Hands-on Workshops**

* **Official Documentation:** [Amazon Bedrock Agents Overview](https://aws.amazon.com/bedrock/agents/) and [Amazon Q Developer Overview](https://aws.amazon.com/q/developer/).  
* **Hands-on Workshop:** [Building Agentic AI Workflows Workshop](https://catalog.us-east-1.prod.workshops.aws/workshops/3f49be39-c62b-40a2-975b-be9bf626526a).

---

# **Day 5: Responsible AI, Bias, & Safety Guardrails**

* **Target Domain:** Domain 4: Guidelines for Responsible AI (14%)  
* **Primary AWS Services:** Guardrails for Amazon Bedrock, SageMaker Clarify, SageMaker Model Monitor

## **90-Minute Execution Schedule**

| Time Allocation | Focus Area | Key Deliverables & Actions |
| :---- | :---- | :---- |
| **00:00 – 00:25** | **Responsible AI Pillars** | Master concepts of Fairness, Transparency, Explainability, Robustness, Privacy, and Governance. |
| **00:25 – 00:50** | **Bedrock Guardrails** | Configure content filters, denied topics, word filters, PII masking, and contextual grounding checks. |
| **00:50 – 01:15** | **Bias & Explainability** | Learn SageMaker Clarify for pre/post-training bias detection and Feature Attribution (SHAP values). |
| **01:15 – 01:30** | **Knowledge Check** | Complete 10 domain-specific practice questions; log errors. |

## **Resources & Hands-on Workshops**

* **Official Documentation:** [Amazon SageMaker AI Overview](https://aws.amazon.com/sagemaker/).  
* **Hands-on Workshop:** [Amazon SageMaker Getting Started Labs](https://aws.amazon.com/sagemaker/getting-started/).

---

# **Day 6: Security, Compliance, Monitoring, & Cost**

* **Target Domain:** Domain 5: Security, Compliance, and Governance (14%) & Cost Management  
* **Primary AWS Services:** AWS KMS, IAM, AWS Artifact, CloudWatch, Cost Explorer, AWS Budgets

## **90-Minute Execution Schedule**

| Time Allocation | Focus Area | Key Deliverables & Actions |
| :---- | :---- | :---- |
| **00:00 – 00:25** | **Data Security & IAM** | Review Data Encryption (at rest and in transit), KMS key management, IAM roles/policies for Bedrock & SageMaker. |
| **00:25 – 00:50** | **Governance & Audit** | Study CloudTrail integration for API logging, AWS Artifact for compliance reporting, and Macie for sensitive data discovery. |
| **00:50 – 01:15** | **Cost Optimization** | Analyze pricing models: Bedrock Provisioned Throughput vs. On-Demand, SageMaker Spot Instances, and Budget Alerts. |
| **01:15 – 01:30** | **Knowledge Check** | Complete 10 domain-specific practice questions; log errors. |

## **Resources & Hands-on Workshops**

* **Official Documentation:** [Amazon Bedrock Guardrails Feature Guide](https://aws.amazon.com/bedrock/guardrails/).  
* **Hands-on Workshop:** [Responsible AI Guardrails Architecture](https://hidekazu-konishi.com/entry/responsible_ai_guardrails_architecture_on_aws.html).

---

# **Day 7: Full Practice Exam & Targeted Remediation**

* **Target Domain:** All Domains (1–5)  
* **Primary AWS Services:** Comprehensive Coverage

## **90-Minute Execution Schedule**

| Time Allocation | Focus Area | Key Deliverables & Actions |
| :---- | :---- | :---- |
| **00:00 – 00:50** | **Full Practice Exam** | Complete a timed 50-question simulated exam covering all 5 domains under strict testing conditions. |
| **00:50 – 01:15** | **Error Log Deep Dive** | Systematically review every missed question, categorize core underlying concepts, and log remedies. |
| **01:15 – 01:30** | **Final Review** | Re-read high-yield service summaries and key architectural patterns for weak areas identified. |

## **Resources & Hands-on Workshops**

* **Official Documentation:** [AWS Certified AI Practitioner Guide](https://aws.amazon.com/certification/certified-ai-practitioner/).  
* **Hands-on Workshop:** [AWS Training & Skill Builder Labs](https://aws.amazon.com/training/).

---

# **Pending links to do**

[https\://catalog.workshops.aws/amazon-bedrock/en-US/30-inference-apis](https://catalog.workshops.aws/amazon-bedrock/en-US/30-inference-apis)  
[https\://github.com/aws-samples/amazon-bedrock-workshop](https://github.com/aws-samples/amazon-bedrock-workshop)   
[https\://catalog.us-east-1.prod.workshops.aws/workshops/3f49be39-c62b-40a2-975b-be9bf626526a/en-US\#what-will-i-build](https://catalog.us-east-1.prod.workshops.aws/workshops/3f49be39-c62b-40a2-975b-be9bf626526a/en-US#what-will-i-build)   
[https\://skillbuilder.aws/learning-plan/3NRN71QZR2/exam-prep-plan-aws-certified-ai-practitioner-aifc01--english/FBV4STG94B](https://skillbuilder.aws/learning-plan/3NRN71QZR2/exam-prep-plan-aws-certified-ai-practitioner-aifc01--english/FBV4STG94B)   
[https\://skillbuilder.aws/learning-plan/G8ENMJ5QBE/aws-artificial-intelligence-practitioner-learning-plan/SU2A1EJM1A](https://skillbuilder.aws/learning-plan/G8ENMJ5QBE/aws-artificial-intelligence-practitioner-learning-plan/SU2A1EJM1A)   
[https\://catalog.workshops.aws/mlops-from-idea-to-production/en-US/06-lab-06](https://catalog.workshops.aws/mlops-from-idea-to-production/en-US/06-lab-06) 

# 

# **Error Log Template**

Use this log daily to capture incorrect practice answers, clarify misconceptions, and identify high-priority review topics prior to exam day.

| Date | Question Domain | Targeted AWS Service / Concept | Root Cause of Error | Correct Principle & Key Takeaway | Follow-Up Status |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Date | Domain 2 | Amazon Bedrock Guardrails | Confused PII Masking with CloudWatch logging | Guardrails mask PII directly within model output; CloudWatch logs call metadata. | Complete |
| Date | Domain 3 | SageMaker Clarify | Thought Clarify was only for model hosting | Clarify provides pre-training and post-training bias metrics \+ SHAP explainability. | Pending |
| Date |  |  |  |  |  |
| Date |  |  |  |  |  |
| Date |  |  |  |  |  |
| Date |  |  |  |  |  |
