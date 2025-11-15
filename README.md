# yufix-maintenance-ai-ops
# YuFix – One-Person Property Maintenance AI Ops

YuFix is an autonomous AI maintenance triage assistant for tenants, landlords and short-term rental hosts.

When something goes wrong – a slow leak, a strange noise, a burning-smell outlet – people don’t know:
- Is this **safe**?
- Can I **fix it myself**?
- Or do I need to **call a professional**?

YuFix turns a rough description into a clear decision and action plan.

---

## 🧠 What YuFix does

1. **User reports a problem**  
   The user types a short description (and can add a photo).

2. **YuFix asks clarifying questions**  
   A unified Gemma prompt returns 4–6 targeted questions.  
   The UI shows them one by one and collects answers.

3. **Autonomous triage**  
   With the description + Q&A, YuFix infers:
   - risk level (1–5),
   - difficulty (1–5).

   It then decides:
   - ✅ **Safe DIY**  
   - ❌ **STOP & Call a Pro**

4. **Action plan**  
   - For **DIY**: YuFix generates tools, clear numbered steps, and a safety note.  
   - For **PRO**: YuFix generates a structured brief (likely causes, urgency, what not to do, information/photos for the technician).

---

## 🧩 Why this can scale as a one-person “AI ops” company

- The same agent handles:
  - question asking,
  - triage (risk / difficulty),
  - and the final plan.
- Most tickets can be handled end-to-end without human intervention.  
- Humans (plumbers, electricians, ops) only step in on high-risk or advanced cases.  
- Adding more properties or tenants mostly means **more API calls**, not more staff.

---

## 🛠 Tech stack & partner tools

**Used in this prototype**

- **Gemma on Google AI Studio** – reasoning engine and unified YuFix prompt.  
- **Google AI Studio App** – host of the interactive front-end for the diagnostic flow.  
- **Lovable** – landing page / marketing front-end to explain YuFix and link to the live demo.

**Planned next steps**

- **Qdrant** – vector database to store Reddit threads and manuals, so agents can retrieve similar past cases and improve answers.  
- **n8n** – automation layer to connect YuFix to email, WhatsApp and property-management systems and route professional jobs.  
- **ElevenLabs** – voice layer to read DIY instructions out loud so users can keep their hands free while fixing things.

---

## 🚀 Demo

- **Live demo (AI Studio app):** _add link here_  
- **Landing page (Lovable):** _add link here_

---

## 🔮 Roadmap

- Add Qdrant-backed retrieval over real-world DIY forums and manuals.
- Use n8n to send YuFix PRO briefs directly to partner plumbers/electricians.
- Add optional voice walkthrough via ElevenLabs.
- Integrate with property-management tools for automatic ticket logging and status updates.
