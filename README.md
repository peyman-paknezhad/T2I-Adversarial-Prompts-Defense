# T2I-Adversarial-Prompts-Defense
### Exploring adversarial prompt attacks and defenses on text-to-image diffusion models, featuring advanced generation techniques and a novel Flan-T5-based correction mechanism to enhance robustness
---

# **Adversarial Prompt Generation for Text-to-Image Models with Defense Strategies Using Language Models**

## **Abstract**
This project explores adversarial attacks on text-to-image models by generating minimal prompt perturbations that cause significant changes in model outputs. Inspired by the work *"A Pilot Study of Query-Free Adversarial Attack against Stable Diffusion"* by **Haomin Zhuang**, **Yihua Zhang**, and **Sijia Liu**, this implementation incorporates adversarial prompt generation techniques like **Greedy Search**, **Genetic Algorithm**, and **PGD (Projected Gradient Descent)**. Additionally, it extends the original methodology with **Particle Swarm Optimization (PSO)**, **Simulated Annealing**, and **Bayesian Optimization**. To mitigate such attacks, a novel defense mechanism is proposed using **Flan-T5** to correct adversarial prompts, ensuring semantic clarity and alignment with the original intent ( I'm unsure whether this adversarial method is truly novel or if it's already been explored. It just occurred to me, so let me know if others have worked on this before).

---

## **Objectives**
1. **Adversarial Prompt Generation**:
   - Generate minimal, five-character perturbations to text prompts that significantly alter image generation outputs.
   - Extend the set of adversarial generation methods by incorporating advanced optimization techniques.
2. **Policy for Adversarial Perturbations**:
   - Based on the referenced paper:
     - Perturbations are limited to five characters.
     - Only printable ASCII characters are allowed.
     - Prompts must remain syntactically valid and contextually coherent.
3. **Adversarial Prompt Correction**:
   - Introduce Flan-T5 as a method to reverse adversarial perturbations, restoring prompt interpretability.
4. **Evaluation**:
   - Assess the effectiveness of adversarial prompts and corrections using CLIP similarity scores and visual inspection.

---

## **Contributions**
### **Derived from Existing Work**:
- Implementation of **Greedy Search**, **Genetic Algorithm**, and **PGD** for query-free adversarial prompt generation, as outlined in *"A Pilot Study of Query-Free Adversarial Attack against Stable Diffusion"*.

### **Novel Extensions**:
- Introduced **PSO**, **Simulated Annealing**, and **Bayesian Optimization** for adversarial prompt crafting, offering diverse approaches to adversarial generation.
- Developed a **Flan-T5-based correction mechanism**, which effectively restores adversarial prompts to a readable and meaningful form.

### **Exploration of Defenses**:
- While the referenced work focuses on adversarial attacks, this project investigates defenses using prompt correction methods, providing a starting point for mitigating such attacks.

---

## **Methodology**
### **Adversarial Prompt Generation**
1. **Existing Techniques**:
   - **Greedy Search**: Iteratively modifies characters to minimize cosine similarity with the original text embeddings.
   - **Genetic Algorithm**: Utilizes population-based evolutionary techniques to optimize adversarial prompts.
   - **PGD (Projected Gradient Descent)**: Adapts gradient-based optimization to craft minimal, targeted perturbations.

2. **Extended Techniques**:
   - **Particle Swarm Optimization (PSO)**: Leverages swarm intelligence to identify effective adversarial perturbations.
   - **Simulated Annealing**: Balances exploration and exploitation in a probabilistic search process.
   - **Bayesian Optimization**: Employs Gaussian Processes to efficiently explore the search space for impactful perturbations.

### **Policy for Adversarial Prompts**
- Perturbations are constrained to:
  - Five characters.
  - Printable ASCII symbols.
  - Grammatically and contextually valid constructs.

### **Adversarial Prompt Correction**
- Uses **Flan-T5** to clean adversarial prompts.
- Ensures semantic integrity while reversing adversarial effects.

### **Evaluation**
1. **Image Generation**:
   - Visualize adversarial impacts using Stable Diffusion.
2. **CLIP Similarity**:
   - Measure the similarity between the original prompt and the generated adversarial image.
3. **Prompt Correction**:
   - Validate the restored prompts using visual and semantic evaluations.

---

## **Results**
- **Adversarial Prompt Generation**:
   - Gradient-based methods (e.g., PGD) proved highly effective for precise perturbations.
   - Probabilistic and heuristic methods (e.g., PSO, Genetic Algorithm) generated diverse and effective adversarial prompts.
- **Adversarial Prompt Correction**:
   - Flan-T5 effectively reversed adversarial perturbations, maintaining high alignment with the original prompt.
- **Evaluation Metrics**:
   - CLIP similarity scores provided quantitative evidence of adversarial impact and correction effectiveness.

---


