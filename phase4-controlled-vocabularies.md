# Phase 4 Controlled Vocabularies

**Version**: 2.0
**Date**: 2025-10-11
**Purpose**: Taxonomy-guided extraction for RQ1, RQ2, and RQ3

---

## RQ1: RAG Techniques and Architectures

**Research Question**: What RAG techniques and architectures are being investigated for IT service desk applications?

### Taxonomy Structure

#### 1. Dense Retrieval Methods
Techniques using neural embeddings for semantic similarity

**Specific Techniques**:
- `DPR (Dense Passage Retrieval)` - Facebook's dual-encoder architecture
- `ANCE (Approximate Nearest Neighbor Negative Contrastive Estimation)` - Hard negative mining
- `ColBERT` - Late interaction with contextualized embeddings
- `Sentence-BERT / SentenceTransformers` - Sentence-level embeddings
- `E5 / BGE embeddings` - Modern open-source embedding models
- `OpenAI embeddings` - Proprietary embedding APIs
- `Contriever` - Unsupervised dense retrieval
- `Dense retrieval (unspecified)` - Generic dense methods without specific model

#### 2. Sparse Retrieval Methods
Traditional keyword-based and statistical methods

**Specific Techniques**:
- `BM25` - Best Match 25 probabilistic ranking
- `TF-IDF` - Term frequency-inverse document frequency
- `Elasticsearch` - Full-text search engine
- `Boolean search` - Exact keyword matching
- `N-gram matching` - Character or token n-grams
- `Sparse retrieval (unspecified)` - Generic sparse methods

#### 3. Hybrid Retrieval
Combining dense and sparse methods

**Specific Techniques**:
- `Dense + BM25 hybrid` - Combining neural and keyword scores
- `SPLADE` - Sparse lexical and expansion model
- `Weighted fusion` - Score combination strategies (RRF, linear combination)
- `Cascaded retrieval` - Sparse first-stage, dense second-stage
- `Parallel hybrid` - Simultaneous sparse and dense retrieval
- `Hybrid retrieval (unspecified)` - Generic hybrid approaches

#### 4. Query Enhancement
Techniques to improve query representation

**Specific Techniques**:
- `Query reformulation` - Rewriting queries for better retrieval
- `Query expansion` - Adding related terms to original query
- `HyDE (Hypothetical Document Embeddings)` - Generating hypothetical answers
- `Query decomposition` - Breaking complex queries into sub-queries
- `Few-shot query generation` - Using LLM to generate better queries
- `Intent classification` - Understanding query purpose before retrieval
- `Entity extraction from queries` - Identifying key entities for retrieval

#### 5. Reranking Methods
Post-retrieval scoring and filtering

**Specific Techniques**:
- `Cross-encoder reranking` - Full attention between query and document
- `LLM-based reranking` - Using language models to rescore
- `MonoT5 / RankT5` - T5-based reranking models
- `Learned-to-rank` - Machine learning ranking models
- `Diversity reranking` - Maximizing result diversity
- `Contextual reranking` - Using conversation history for scoring
- `Relevance filtering` - Threshold-based filtering

#### 6. Context Enhancement
Advanced retrieval patterns and context manipulation

**Specific Techniques**:
- `Multi-hop retrieval` - Iterative retrieval following document chains
- `Recursive retrieval` - Hierarchical document navigation
- `Parent-child chunking` - Retrieving chunks with surrounding context
- `Graph-based retrieval` - Knowledge graph traversal
- `Temporal context` - Time-aware retrieval
- `Conversation history integration` - Multi-turn context management
- `Document summarization for context` - Compressing retrieved content

#### 7. Advanced RAG Architectures
Novel RAG system designs

**Specific Techniques**:
- `Self-RAG` - Self-reflective retrieval decisions
- `Corrective RAG (CRAG)` - Self-correction with web search fallback
- `Adaptive RAG` - Dynamic retrieval strategy selection
- `RAPTOR` - Recursive abstractive processing with tree-organized retrieval
- `FLARE` - Forward-looking active retrieval
- `Interleaved retrieval-generation` - Alternating retrieval and generation
- `Retrieval-on-demand` - Citation-driven retrieval

#### 8. Fine-tuning and Optimization
Model adaptation techniques

**Specific Techniques**:
- `Retriever fine-tuning` - Domain-specific embedding training
- `Instruction-tuned retrieval` - Task-specific retrieval training
- `RLHF for retrieval` - Reinforcement learning from human feedback
- `Distillation` - Compressing large retrievers to smaller models
- `Parameter-efficient fine-tuning (LoRA/Adapters)` - Efficient model adaptation
- `Domain adaptation` - Adapting pre-trained models to ITSM domain

#### 9. Vector Database and Indexing
Infrastructure and storage strategies

**Specific Techniques**:
- `FAISS (Facebook AI Similarity Search)` - Efficient vector search
- `Pinecone` - Managed vector database
- `Weaviate` - Vector search engine
- `Milvus` - Open-source vector database
- `ChromaDB` - Embedding database
- `Qdrant` - Vector similarity search engine
- `HNSW (Hierarchical Navigable Small World)` - Graph-based indexing
- `IVF (Inverted File Index)` - Clustering-based indexing
- `Approximate Nearest Neighbor (ANN)` - General ANN algorithms

---

## RQ2: IT Service Desk Applications

**Research Question**: What are the specific IT service desk applications and use cases where RAG is being applied?

### Taxonomy Structure (ITIL-Aligned)

#### 1. Incident Management
Managing service disruptions and restoring normal operation

**Specific Applications**:
- `Ticket classification` - Categorizing incidents by type, priority, urgency
- `Ticket routing` - Assigning tickets to appropriate resolver groups
- `Automated incident diagnosis` - Identifying root causes from symptoms
- `Resolution recommendation` - Suggesting solutions based on historical data
- `Similar incident matching` - Finding past incidents with same symptoms
- `Incident escalation support` - Identifying when to escalate
- `Major incident detection` - Recognizing high-impact incidents
- `Incident closure automation` - Auto-closing resolved incidents

#### 2. Knowledge Management
Creating, maintaining, and retrieving organizational knowledge

**Specific Applications**:
- `Knowledge base search` - Finding relevant KB articles
- `Solution retrieval` - Retrieving documented solutions
- `Knowledge article recommendation` - Suggesting relevant articles to agents
- `Automated documentation generation` - Creating KB articles from tickets
- `Knowledge gap identification` - Detecting missing documentation
- `FAQ matching` - Matching queries to frequently asked questions
- `Knowledge validation` - Verifying accuracy of knowledge articles
- `Context-aware knowledge delivery` - Providing relevant knowledge at right time

#### 3. Request Fulfillment
Handling service requests and standard changes

**Specific Applications**:
- `Service catalog navigation` - Helping users find services
- `Request routing` - Directing requests to fulfillment teams
- `Standard request automation` - Auto-fulfilling common requests
- `Request clarification` - Gathering missing information
- `Approval workflow support` - Assisting with approval decisions
- `Service request recommendation` - Suggesting services based on user needs

#### 4. Problem Management
Identifying and managing root causes of incidents

**Specific Applications**:
- `Root cause analysis` - Identifying underlying problems
- `Problem pattern detection` - Finding recurring incident patterns
- `Known error matching` - Linking incidents to known problems
- `Trend analysis` - Identifying emerging problems from incident data
- `Workaround retrieval` - Finding temporary solutions
- `Problem investigation support` - Assisting problem managers

#### 5. Self-Service and Virtual Agents
Enabling users to resolve issues independently

**Specific Applications**:
- `Chatbot / virtual agent` - Conversational self-service interface
- `Automated FAQ responses` - Answering common questions
- `Guided troubleshooting` - Step-by-step problem resolution
- `Password reset automation` - Self-service password management
- `Status inquiry` - Checking ticket/service status
- `Service information retrieval` - Getting information about IT services
- `How-to guidance` - Providing instructions for common tasks
- `User intent understanding` - Interpreting what users are asking for

#### 6. Multi-Channel and Communication
Managing interactions across different channels

**Specific Applications**:
- `Email ticket processing` - Extracting information from emails
- `Chat support` - Real-time text-based support
- `Voice/call transcription analysis` - Processing spoken interactions
- `Multi-channel context preservation` - Maintaining context across channels
- `Communication template generation` - Creating standardized responses
- `Sentiment analysis` - Understanding user frustration levels
- `Language translation` - Supporting multiple languages

#### 7. Service Desk Analytics and Insights
Using data to improve service desk operations

**Specific Applications**:
- `Ticket analytics` - Analyzing ticket patterns and trends
- `Agent performance support` - Providing insights to improve agent work
- `SLA monitoring and prediction` - Predicting SLA breaches
- `Customer satisfaction analysis` - Understanding user feedback
- `Workload forecasting` - Predicting future ticket volumes
- `Quality assurance` - Reviewing agent responses for quality

#### 8. Configuration and Asset Management
Managing IT assets and configuration items

**Specific Applications**:
- `CMDB query` - Retrieving configuration item information
- `Asset information retrieval` - Finding asset details
- `Impact analysis` - Determining impact of changes or incidents
- `Relationship mapping` - Understanding CI dependencies
- `Asset recommendation` - Suggesting appropriate hardware/software

---

## RQ3: Implementation Challenges and Limitations

**Research Question**: What are the challenges and limitations in implementing RAG systems for IT service desks?

### Taxonomy Structure

#### 1. Performance and Scalability
System performance and capacity challenges

**Specific Challenges**:
- `Real-time response latency` - Slow retrieval/generation causing delays
- `Large-scale indexing` - Difficulty indexing millions of documents
- `Query throughput limitations` - Cannot handle concurrent queries
- `Vector database performance` - Slow similarity search at scale
- `Memory constraints` - Insufficient RAM for embeddings/models
- `Compute resource requirements` - High GPU/CPU demands
- `Scaling to enterprise volume` - Cannot handle production workloads
- `Cold start problems` - Slow initial query processing

#### 2. Retrieval Quality and Relevance
Accuracy and precision of retrieved information

**Specific Challenges**:
- `Low retrieval precision` - Too many irrelevant results
- `Low retrieval recall` - Missing relevant documents
- `Semantic mismatch` - Embeddings fail to capture meaning
- `Out-of-domain queries` - Poor performance on unfamiliar topics
- `Ambiguous query handling` - Difficulty with vague questions
- `Context window limitations` - Cannot retrieve enough context
- `Ranking accuracy` - Relevant documents ranked too low
- `Noise in retrieved content` - Irrelevant information in results

#### 3. Generation Quality and Accuracy
LLM output quality issues

**Specific Challenges**:
- `Hallucination` - LLM generates false information
- `Factual inconsistency` - Generated text contradicts retrieved content
- `Citation/attribution problems` - Cannot track information sources
- `Answer completeness` - Incomplete or partial responses
- `Technical inaccuracy` - Wrong technical details in responses
- `Verbosity or brevity issues` - Responses too long or too short
- `Tone and style inconsistency` - Inappropriate communication style
- `Multi-turn conversation coherence` - Losing context in dialogues

#### 4. Data Quality and Availability
Issues with underlying data sources

**Specific Challenges**:
- `Insufficient training data` - Not enough data for fine-tuning
- `Data quality problems` - Noisy, incorrect, or outdated information
- `Incomplete knowledge bases` - Missing critical information
- `Data silos` - Information scattered across systems
- `Unstructured data handling` - Difficulty processing diverse formats
- `Data labeling requirements` - Need for annotated training data
- `Sensitive data handling` - PII in tickets/documents
- `Data versioning` - Managing changing knowledge over time

#### 5. Integration and Deployment
Technical integration challenges

**Specific Challenges**:
- `Legacy system integration` - Connecting to old ITSM platforms
- `API compatibility` - Interfacing with existing tools
- `Authentication and authorization` - Complex access control
- `Workflow integration` - Fitting into existing processes
- `Multi-system data aggregation` - Pulling data from multiple sources
- `Deployment complexity` - Difficult to deploy and maintain
- `Version management` - Managing model and component updates
- `Monitoring and observability` - Lack of visibility into system behavior

#### 6. Domain Adaptation and Customization
Adapting general RAG to ITSM context

**Specific Challenges**:
- `Domain-specific terminology` - Technical jargon not understood
- `Organization-specific knowledge` - Unique policies/procedures
- `Fine-tuning requirements` - Need to adapt models to domain
- `Lack of pre-trained ITSM models` - No domain-specific models available
- `Customization complexity` - Difficult to tailor to specific needs
- `Transfer learning limitations` - General models don't transfer well
- `Multi-tenant customization` - Different needs per customer/department

#### 7. Security, Privacy, and Compliance
Regulatory and security concerns

**Specific Challenges**:
- `Data privacy concerns` - PII exposure risks
- `Security vulnerabilities` - Prompt injection, data leakage
- `Compliance requirements` - GDPR, HIPAA, SOC2 compliance
- `Access control` - Ensuring users only see authorized information
- `Audit trail requirements` - Tracking who accessed what
- `Data residency` - Geographic data storage requirements
- `Intellectual property concerns` - Protecting proprietary information
- `Model security` - Protecting model weights and parameters

#### 8. Cost and Resource Constraints
Economic and resource limitations

**Specific Challenges**:
- `High operational costs` - Expensive API calls or compute
- `Infrastructure costs` - Expensive hardware requirements
- `Model hosting costs` - Cloud hosting expenses
- `Budget constraints` - Limited funding for implementation
- `Skill gap` - Lack of expertise to implement/maintain
- `Time to implementation` - Long development cycles
- `ROI uncertainty` - Unclear business value
- `Maintenance burden` - High ongoing operational overhead

#### 9. Evaluation and Validation
Difficulty measuring and validating performance

**Specific Challenges**:
- `Lack of evaluation metrics` - No standard quality measures
- `Difficulty in ground truth creation` - Hard to create test sets
- `Subjective quality assessment` - Hard to measure user satisfaction
- `A/B testing complexity` - Difficult to compare systems
- `Benchmark dataset unavailability` - No public ITSM datasets
- `Human evaluation costs` - Expensive expert review requirements
- `Confidence calibration` - Uncertainty estimation problems
- `Long-term performance monitoring` - Tracking quality over time

#### 10. User Adoption and Trust
Human factors and organizational challenges

**Specific Challenges**:
- `User trust issues` - Agents/users don't trust AI responses
- `Resistance to change` - Reluctance to adopt new tools
- `Training requirements` - Need to train agents on new system
- `Explainability demands` - Users need to understand reasoning
- `Inconsistent user experience` - Variable quality across interactions
- `Over-reliance concerns` - Users accepting wrong answers
- `Cultural barriers` - Organizational resistance to AI
- `Change management complexity` - Difficult organizational rollout

---

## Usage Guidelines for Phase 4 Classification

### 1. Multi-Label Classification
- Papers can have MULTIPLE techniques, applications, and challenges
- Extract ALL relevant items from each paper
- Don't force papers into single categories

### 2. Confidence Scoring
- Rate confidence for each extracted item: 0.0 - 1.0
- 0.9-1.0: Explicitly stated, central focus
- 0.7-0.89: Clearly discussed, supporting evidence
- 0.5-0.69: Mentioned or implied, limited detail
- 0.3-0.49: Tangential reference, unclear
- 0.0-0.29: Speculative inference, weak evidence

### 3. Handling Edge Cases

**When technique is not in taxonomy**:
- Use closest matching parent category + note: `Dense retrieval (unspecified) - Paper mentions "neural semantic search"`
- Add to "other_techniques" field for later review

**When application is not ITSM-specific**:
- If general AI/NLP application: Extract but mark `itsm_specific: false`
- Focus on service desk context even if implicit

**When no challenges discussed**:
- Leave challenges empty - don't infer or assume
- Mark `challenges_discussed: false`

### 4. Coverage Scores
Rate how well paper addresses each RQ (0.0-1.0):
- RQ1 coverage: 0.0 (no techniques) to 1.0 (comprehensive technique discussion)
- RQ2 coverage: 0.0 (no ITSM context) to 1.0 (detailed service desk application)
- RQ3 coverage: 0.0 (no challenges) to 1.0 (thorough limitation analysis)

### 5. Primary Category Assignment
Select ONE primary category per RQ:
- **RQ1 Primary**: Which technique category is most prominent?
- **RQ2 Primary**: Which ITSM process area is primary focus?
- **RQ3 Primary**: Which challenge category is most emphasized?

---

## Validation Checklist

Before finalizing extraction, verify:
- [ ] All extracted items match controlled vocabulary terms (exact string match)
- [ ] Confidence scores are provided for each item
- [ ] Coverage scores provided for RQ1, RQ2, RQ3
- [ ] Primary categories assigned for each RQ
- [ ] At least one item extracted for RQ1 (all papers should mention RAG techniques)
- [ ] RQ2 items are ITSM-related (not generic AI applications)
- [ ] No placeholder text like "not specified" or "N/A"
- [ ] "Other" items have explanatory notes

---

## Examples

### Example 1: Comprehensive ITSM Paper

**Paper**: "Hybrid Retrieval-Augmented Generation for IT Helpdesk Ticket Routing with Real-time Constraints"

**RQ1 Extraction**:
```json
{
  "rq1_techniques": {
    "techniques_identified": [
      {
        "technique": "Dense + BM25 hybrid",
        "confidence": 0.95,
        "evidence": "Paper proposes hybrid system combining SBERT and BM25"
      },
      {
        "technique": "Cross-encoder reranking",
        "confidence": 0.88,
        "evidence": "Uses MiniLM cross-encoder for final ranking"
      },
      {
        "technique": "FAISS (Facebook AI Similarity Search)",
        "confidence": 0.92,
        "evidence": "FAISS used for efficient vector indexing"
      }
    ],
    "primary_category": "Hybrid Retrieval",
    "coverage_score": 0.93
  }
}
```

**RQ2 Extraction**:
```json
{
  "rq2_applications": {
    "applications_identified": [
      {
        "application": "Ticket routing",
        "confidence": 0.98,
        "evidence": "Primary use case - automated routing to resolver groups"
      },
      {
        "application": "Similar incident matching",
        "confidence": 0.85,
        "evidence": "Used to find historical similar tickets"
      }
    ],
    "primary_category": "Incident Management",
    "itsm_specific": true,
    "coverage_score": 0.90
  }
}
```

**RQ3 Extraction**:
```json
{
  "rq3_challenges": {
    "challenges_identified": [
      {
        "challenge": "Real-time response latency",
        "confidence": 0.95,
        "evidence": "Paper focuses on <100ms response time requirement"
      },
      {
        "challenge": "Low retrieval recall",
        "confidence": 0.78,
        "evidence": "Reports difficulty finding all relevant historical tickets"
      }
    ],
    "primary_category": "Performance and Scalability",
    "challenges_discussed": true,
    "coverage_score": 0.82
  }
}
```

### Example 2: General RAG Paper (Minimal ITSM Context)

**Paper**: "Self-RAG: Learning to Retrieve, Generate and Critique through Self-Reflection"

**RQ1 Extraction**:
```json
{
  "rq1_techniques": {
    "techniques_identified": [
      {
        "technique": "Self-RAG",
        "confidence": 0.99,
        "evidence": "Core contribution - self-reflective RAG architecture"
      },
      {
        "technique": "LLM-based reranking",
        "confidence": 0.85,
        "evidence": "Uses critic model to filter retrieved passages"
      }
    ],
    "primary_category": "Advanced RAG Architectures",
    "coverage_score": 0.95
  }
}
```

**RQ2 Extraction**:
```json
{
  "rq2_applications": {
    "applications_identified": [
      {
        "application": "Knowledge base search",
        "confidence": 0.45,
        "evidence": "Mentions potential for enterprise knowledge retrieval in discussion"
      }
    ],
    "primary_category": "Knowledge Management",
    "itsm_specific": false,
    "coverage_score": 0.30
  }
}
```

**RQ3 Extraction**:
```json
{
  "rq3_challenges": {
    "challenges_identified": [
      {
        "challenge": "Hallucination",
        "confidence": 0.92,
        "evidence": "Paper addresses reducing hallucination through self-reflection"
      },
      {
        "challenge": "Citation/attribution problems",
        "confidence": 0.80,
        "evidence": "Discusses tracking which passages contributed to generation"
      }
    ],
    "primary_category": "Generation Quality and Accuracy",
    "challenges_discussed": true,
    "coverage_score": 0.75
  }
}
```

---

## Revision History

| Version | Date | Changes |
|---------|------|---------|
| 2.0.1 | 2025-10-12 | Added common term variations based on test extraction results to improve vocabulary compliance |
| 2.0 | 2025-10-11 | Complete redesign with controlled vocabularies for RQ1-3 only (dropped RQ4) |
| 1.0 | 2024-08-XX | Initial version with 4-category classification |

---

## Version 2.0.1 Vocabulary Additions (2025-10-12)

Based on initial test extractions, the following commonly-extracted terms were added to improve vocabulary compliance:

**RQ1 Additions**:
- "Dense Retrieval" (capitalized variation)
- "Semantic search" (common LLM term for dense retrieval)
- "Vector similarity search" (descriptive variant)
- "Sparse Retrieval" (capitalized variation)
- "Keyword search" (common term for sparse methods)
- "Lexical search" (formal term for keyword-based retrieval)

**RQ2 Additions**:
- "Knowledge Management" (general category term)
- "Question answering" (generic application term)
- "Question Answering System (QAS)" (formal system name)
- "IT Service Management (ITSM)" (general ITSM term)
- "Service desk automation" (broad application category)
- "Help desk support" (alternative terminology)

**RQ3 Additions**:
- "Retrieval Quality (RQ)" (abbreviated form)
- "Retrieval quality" (lowercase variant)
- "Search relevance" (alternative phrasing)
- "Result ranking issues" (descriptive variant)
- "Data Quality (DQ)" (abbreviated form)
- "Data quality" (lowercase variant)
- "Poor data quality" (descriptive variant)
- "Knowledge base quality" (specific context)

These additions improve vocabulary coverage from 60-83% to expected 90%+ without compromising taxonomy structure.
