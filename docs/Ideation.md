# **RealityCheck**

## **1. Vision & Mission**

**Vision**: Empower individuals with schizophrenia to navigate their perceptions safely and confidently using AI.

**Mission**: Build an AI-assisted mobile application that helps users distinguish between hallucinations and reality using real-time audio-visual and cognitive assistance, while providing therapeutic tools, support, and monitoring.


### Core Symptoms to Address

---

#### **Hallucinations**

Hallucinations are perceptions in the absence of an external stimulus — meaning the person experiences something that isn't actually present. They can affect any of the five senses and are a core symptom of schizophrenia.

---

#####  Auditory Hallucinations *(Most common in schizophrenia)*

Hearing voices or sounds that are not actually present. Voices may:

- Talk directly to the person  
- Talk about the person in third person  
- Command or threaten *(command hallucinations)*  
- Argue among themselves  
- Be distressing or, less commonly, comforting depending on tone and content  

---

#####  Visual Hallucinations

Seeing people, shapes, shadows, or lights that aren't there. May include:

- Faces or full figures (sometimes familiar, sometimes unknown)  
- Distorted environments (e.g., walls moving, colors shifting)  
- People appearing and disappearing  

---

#####  Optional Subclassifications (Advanced Insight for App Logic)

- **Mood-congruent vs. mood-incongruent hallucinations**  
  _e.g., a depressed person hearing a voice saying “you’re worthless”_  
- **Interactive vs. Passive hallucinations**  
  _Are the voices engaging directly with the user or just passively present?_  

---

#### **Delusions**

---

#####  *Fregoli Delusion*  
The belief that different people are actually a single person who is changing appearance or in disguise. Often includes paranoia (e.g., "They’re following me in different forms").

---

#####  *Capgras Delusion*  
The belief that someone familiar has been replaced by an imposter. This often affects trust and emotional connection.

---

#####  General Misidentification / Misperception  
Sometimes individuals may see someone with a vaguely similar face, posture, or walk and mistakenly believe it's someone they know — even without forming a full-blown delusion.

---

## **2. Key Features & Ideas**

### **Core Features (AI-Assisted Reality Validation)**

- **Voice Validation (Mic Input)**:  
  Detect external sounds to differentiate between internal auditory hallucinations and real voices using NLP + Audio Signal Processing.

- **Visual Reality Check (Camera Input)**:  
  Use object/person detection (YOLOv8, MobileNet, etc.) to validate whether detected visual inputs exist in the real world.

### **Additional Features**

- **Thought Logging & Journal Assistant**:  
  Users can speak or type thoughts. AI identifies delusional patterns or irrational thoughts using NLP sentiment + psycholinguistic analysis.

- **Crisis Detection & SOS**:  
  Anomaly detection using usage pattern, tone in voice, or language in journal. If triggered, it can alert caregivers or mental health professionals.

- **AI Companion**:  
  A friendly AI chatbot trained on CBT (Cognitive Behavioral Therapy) techniques to guide users through thought restructuring or grounding exercises.

- **Daily Reality Anchor**:  
  Personalized cues to keep users grounded (e.g., time-based reminders, affirmations, or reminders of known truths like "You are in your room right now").

- **Mood and Symptom Tracker**:  
  Track symptoms over time via self-reporting and passive behavior monitoring.

- **Medication & Routine Reminder**:  
  Ensure adherence to medication or appointments.

- **Offline Mode**:  
  Key functionality available without internet access for emergencies.
- **Misidentification Insight Tool** (for Fregoli-like Symptoms)
  Helps users recognize and reflect on moments of delusional misidentification.

  Gentle self-check questions triggered via journal entries or daily prompts

  Logs and identifies patterns where users mistake strangers for familiar people

  Offers grounding support and AI-guided reality testing exercises

  Optional alerts for caregivers if frequent misidentification patterns are detected


---

## **3. AI & Tech Stack**

| Feature                | Tools & Techniques                                                     |
| ---------------------- | ---------------------------------------------------------------------- |
| Voice Reality Check    | MFCC + Spectrogram + Deep Learning Classifier (e.g., CNN)              |
| Visual Reality Check   | MobileNet / YOLOv8 + AR overlay to show what’s real                    |
| NLP Thought Analysis   | Transformers (DistilBERT / RoBERTa) fine-tuned on psychiatric datasets |
| Chatbot                | OpenAI GPT / LLM trained with CBT dialogue datasets                    |
| Mood Detection         | Sentiment + Voice Emotion Recognition                                  |
| Backend                | Firebase / Supabase / AWS                                              |
| App Framework          | React Native / Flutter                                                 |
| Local Model Processing | TensorFlow Lite / Core ML                                              |

---

## **4. Roadmap**

### **Phase 1: Research & Discovery**

- Conduct interviews with psychiatrists, therapists, and individuals with schizophrenia.
- Review existing apps & clinical studies.
- Finalize core problem statements and user personas.

### **Phase 2: Prototyping & Validation**

- Create wireframes & low-fidelity UI.
- Build MVP with:
  - Audio Validation Module
  - Visual Detection Module
  - Basic journaling
- Perform small-group testing with feedback.

### **Phase 3: AI Model Training & Integration**

- Collect safe, anonymized data (voice samples, journaling texts).
- Train lightweight models optimized for edge devices.
- Integrate AI with front-end and test latency, accuracy.

### **Phase 4: Security, Ethics, and Privacy**

- Work with legal & ethical consultants to ensure HIPAA/GDPR compliance.
- Implement encrypted local storage, secure authentication.
- Build in user consent workflows.

### **Phase 5: Expansion & Deployment**

- Add CBT AI Companion, mood tracking, and SOS.
- Partner with clinics or universities for trials.
- Launch on app stores with pilot campaigns.

---

## **5. Key Considerations**

### **Ethical & Clinical**

- Avoid replacing professional diagnosis.
- Always include a disclaimer: “This is a supportive tool, not a diagnostic one.”
- Include safety nets like direct contact with professionals.

### **Technical**

- Ensure ultra-low-latency for real-time checks.
- Make the models lightweight and power-efficient.
- Keep the interface minimal and non-triggering.

### **Accessibility**

- Voice-driven UI for people who may not want to interact visually.
- Multilingual support.
- Emergency button always accessible.

---

## **6. Future Possibilities**

- **AR Glasses Integration**: For hands-free visual validation.
- **Wearable Integration**: Smartwatches for vitals tracking during anxiety spikes.
- **Therapist Dashboard**: A portal for mental health professionals to view anonymized patterns (with user consent).
- **Community Support**: Anonymous chat rooms moderated by professionals.

---

## **7. Sample Use Case**

> **User**: Hears voices again. Opens app.  
> **Mic**: Detects no external sound. Displays “This voice was not detected by the mic.”  
> **User**: Sees a figure across the room. Opens camera.  
> **Camera**: No person detected.  
> **App**: Gently responds: “We didn’t see anyone. Would you like to do a grounding exercise?”

---
