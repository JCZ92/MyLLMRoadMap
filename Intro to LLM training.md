## Pre-training 
- Foundation model with pre-trained weights establishing baseline capabilities
- Employs self-supervised learning paradigms with masked language modeling (BERT-style) or next-token prediction objectives (GPT-style)
- Utilizes extensive corpora derived from web-scale text, literature, and scholarly publications
- Establishes general linguistic competencies and factual knowledge acquisition
- Necessitates substantial computational resources and distributed training infrastructures

## Fine-tuning
- Leverages curated, high-fidelity annotated datasets with human oversight
- Requires significantly less data compared to pre-training
- Focuses on optimizing model performance for specific tasks or domains
- Utilizes parameter-efficient transfer learning methodologies such as Low-Rank Adaptation (LoRA)
- Creates either multi-task generalist models or domain-specific specialist implementations

## RLHF (Reinforcement Learning from Human Feedback)
- Implements Proximal Policy Optimization (PPO) to constrain policy divergence
- Incorporates human evaluation through comparative assessment of model-generated outputs
- Uses learned reward models as preference proxies for scalable training
- Requires careful monitoring to prevent reward hacking and overoptimization
- Balances safety and helpfulness in model responses
- May evolve toward RLAIF (Reinforcement Learning from AI Feedback)

Alignment = Fine-tuning + RLHF
