# Meeting Transcript Analysis - Advanced System Prompt

A comprehensive prompt engineering resource for automated meeting documentation and analysis.

## 📋 Table of Contents

- [Prompt Engineering Analysis](#-prompt-engineering-analysis)
- [The Complete System Prompt](#-the-complete-system-prompt)
- [Practical Implementation Guide](#-practical-implementation-guide)
- [Prompt Variations & Extensions](#-prompt-variations--extensions)
- [Example Usage](#-example-usage)
- [Troubleshooting & Tips](#-troubleshooting--tips)
- [Integration Strategies](#-integration-strategies)

---

## 🔍 Prompt Engineering Analysis

### What Makes This Prompt Exceptionally Effective

This prompt demonstrates advanced prompt engineering principles that result in consistent, high-quality outputs:

#### **1. Crystal Clear Objective**
```
"Systematically analyze the provided meeting transcript to produce professional, 
accurate, and structured meeting documentation."
```

**Why This Works:**
- Defines specific scope (meeting transcripts)
- Sets quality standards (professional, accurate, structured)
- Establishes clear output expectation (documentation)

#### **2. Sequential Task Breakdown**
The prompt uses a logical 5-step workflow:
1. **Cleanup** → Raw transcript processing
2. **Identification** → Speaker standardization  
3. **Summary** → High-level synthesis
4. **Extraction** → Actionable items
5. **Formatting** → Structured output

**Prompt Engineering Principle:** Complex tasks broken into manageable, sequential steps produce more reliable results.

#### **3. Explicit Output Structure**
```markdown
Meeting Overview
Key Discussions
Decisions Made
Action Items (Table format)
Additional Notes
```

**Why This Works:**
- Eliminates ambiguity about expected format
- Ensures consistency across different inputs
- Makes output immediately usable for stakeholders

#### **4. Professional Context Awareness**
- Tone guidelines specify "professional, objective, and concise"
- Output optimized for "executives and stakeholders"
- Formatting designed for easy scanning

#### **5. Error Handling & Edge Cases**
- Instructions for unidentified speakers
- Protocol for unclear ownership
- Guidelines for missing deadlines
- Handling of overlapping topics

### Prompt Engineering Best Practices Demonstrated

✅ **Specificity over Ambiguity**: Each instruction is precise and actionable  
✅ **Context Setting**: Establishes professional business context  
✅ **Format Specification**: Exact markdown structure required  
✅ **Quality Standards**: Clear criteria for acceptable output  
✅ **Edge Case Handling**: Instructions for common problems  
✅ **Consistent Structure**: Repeatable format for any meeting type  

---

## 📝 The Complete System Prompt

### Copy-Paste Ready Version

```
System Prompt: Advanced Meeting Transcript Analysis and Note Generation

Objective:
Systematically analyze the provided meeting transcript to produce professional, accurate, and structured meeting documentation. Ensure the output is clear, consistent, and actionable for stakeholders by applying best practices in summarization, action item extraction, and formatting.

Instructions:

1. Transcript Cleanup and Normalization:
   • Correct all grammar, spelling, and transcription errors while preserving the speaker's intent and tone.
   • Remove filler words, informal expressions, and irrelevant small talk unless it contributes to understanding key decisions or action items.
   • Organize the conversation strictly in chronological order, ensuring logical narrative flow.
   • Where multiple overlapping topics are discussed, ensure they are segmented and labeled for clarity.

2. Participant Identification:
   • Use first names and initials of last names (e.g., "Amyn P.") to identify all speakers consistently throughout the output.
   • If a speaker is not explicitly named, use "Unidentified Speaker".

3. Summary Generation:
   Provide a concise executive summary that includes:
   • Purpose of the meeting (why it was held).
   • Key discussion points (main topics discussed).
   • Decisions made (explicit agreements, approvals, or directions given).
   • Final conclusions or agreed outcomes (what was confirmed or next steps finalized).

4. Action Items Extraction:
   • Extract all actionable items from the transcript.
   • Assign clear ownership using participants' names.
   • If ownership is unclear or not stated, label as "Unassigned".
   • Include deadlines if explicitly mentioned; if deadlines are implied but not stated, mark as "No deadline provided".
   • Ensure each action is phrased as a clear, task-oriented statement (e.g., "Finalize project scope", not "Discussion about project scope").

5. Structured Meeting Notes Output:
   Present the output in the following fixed structure using markdown headers:

   ## Meeting Overview
   One clear paragraph summarizing the meeting's purpose, agenda, and high-level context.

   ## Key Discussions
   1. [Topic 1]
      • [Critical insight or perspective]
      • [Decision or outcome]
   2. [Topic 2]
      • [Critical insight or perspective]
      • [Decision or outcome]

   ## Decisions Made
   • [Decision 1 with responsible person if applicable]
   • [Decision 2 with responsible person if applicable]

   ## Action Items
   | Task | Owner | Deadline |
   |------|-------|----------|
   | [Specific task] | [Name] | [Date or "No deadline provided"] |

   ## Additional Notes
   • [Side discussions, concerns, or follow-up items]

Tone and Style Guidelines:
• Use a professional, objective, and concise tone.
• Avoid informal language unless it is directly quoted and essential to context.
• Ensure the output is easy to scan by executives and stakeholders.
• Use consistent formatting, indentation, and labeling for ease of review.

Input Template:
[Insert or attach transcript here. Ensure timestamps, speaker names, and context are preserved.]
```

---

## 🛠️ Practical Implementation Guide

### Platform-Specific Usage

#### **ChatGPT/Claude/GPT-4**
```
1. Copy the system prompt above
2. Start new conversation
3. Paste system prompt as first message
4. Follow with your transcript
5. AI will automatically apply the structure
```

#### **API Integration (OpenAI/Anthropic)**
```python
# Example API call structure
{
    "model": "gpt-4",
    "messages": [
        {
            "role": "system",
            "content": "[Full system prompt above]"
        },
        {
            "role": "user", 
            "content": "[Meeting transcript]"
        }
    ],
    "temperature": 0.1,  # Lower for more consistent formatting
    "max_tokens": 2000   # Adjust based on meeting length
}
```

### Input Preparation Tips

#### **Optimal Transcript Format**
```
[Timestamp] Speaker Name: Content
[10:00 AM] John Smith: Let's start with the quarterly review...
[10:02 AM] Sarah Johnson: I have concerns about the timeline...
```

#### **Minimum Required Information**
- Speaker identification (names or roles)
- Chronological flow of conversation
- Complete sentences (not fragmented)

#### **What to Include**
✅ All substantive discussion points  
✅ Decisions and agreements  
✅ Action items and assignments  
✅ Deadlines and timeframes  
✅ Questions and concerns raised  

#### **What to Exclude**
❌ Pre-meeting small talk  
❌ Technical difficulties discussions  
❌ Sidebar conversations unrelated to agenda  
❌ Excessive filler words and false starts  

---

## 🔄 Prompt Variations & Extensions

### Simplified Version (Casual Meetings)

```
Analyze this meeting transcript and provide:

1. **Summary**: What was discussed and decided
2. **Action Items**: Who needs to do what by when
3. **Key Points**: Important details to remember

Format as simple bullet points. Keep it concise and actionable.

[Insert transcript]
```

### Enhanced Version (Board Meetings/Legal)

```
System Prompt: Executive Board Meeting Analysis with Legal Compliance

Objective: 
Analyze board meeting transcripts with attention to governance, compliance, and fiduciary responsibilities.

Additional Requirements:
• Flag any governance issues or compliance concerns
• Note voting records and dissenting opinions
• Highlight regulatory or legal implications
• Identify conflicts of interest discussions
• Ensure confidential information is appropriately marked

[Rest of original prompt structure]
```

### Industry-Specific Adaptations

#### **Healthcare/Medical**
- Add HIPAA compliance considerations
- Include clinical decision tracking
- Note patient safety discussions

#### **Legal/Compliance**
- Track regulatory requirements mentioned
- Note legal risks or exposures discussed  
- Highlight compliance deadlines

#### **Technical/Engineering**
- Include technical specifications discussed
- Track testing and validation requirements
- Note technical debt or infrastructure needs

### Meeting Type Variations

#### **Daily Standups**
```
Quick standup analysis:
• What was accomplished yesterday
• What's planned for today  
• Any blockers or concerns
• Action items or help needed

[Insert transcript]
```

#### **Project Reviews**
```
Project review analysis focusing on:
• Project status and milestones
• Budget and resource updates
• Risk assessment and mitigation
• Scope changes or approvals
• Next phase planning

[Insert transcript]  
```

---

## 💡 Example Usage

### Sample Input Transcript
```
[9:00 AM] Sarah Chen: Good morning everyone. Let's start with our quarterly planning meeting. We have three main topics today: budget allocation, the new product launch timeline, and team restructuring.

[9:02 AM] Mike Rodriguez: Thanks Sarah. On the budget front, we're looking at a 15% increase in our marketing spend for Q4. The board approved this last week.

[9:04 AM] Jennifer Walsh: That's great news. For the product launch, I'm concerned about the timeline. Engineering is behind on the API development. We might need to push the launch from November to December.

[9:06 AM] Sarah Chen: That's a significant delay. Mike, can you work with Jennifer to see if we can reallocate some resources to get back on track?

[9:07 AM] Mike Rodriguez: Absolutely. I'll meet with the engineering team this week and report back by Friday.

[9:08 AM] Sarah Chen: Perfect. For team restructuring, we're creating a new Customer Success role. Jennifer, can you draft the job description?

[9:10 AM] Jennifer Walsh: Sure, I'll have that ready by next Tuesday.
```

### Expected Output
```markdown
## Meeting Overview

Quarterly planning meeting covering budget allocation, product launch timeline, and team restructuring. The team addressed resource allocation challenges and established clear action items for moving forward with Q4 initiatives.

## Key Discussions

1. **Budget Allocation for Q4**
   • 15% increase in marketing spend approved by board
   • Additional resources available for strategic initiatives

2. **Product Launch Timeline Concerns**  
   • Engineering behind schedule on API development
   • Potential delay from November to December launch
   • Need for resource reallocation to get back on track

3. **Team Restructuring Initiative**
   • Decision to create new Customer Success role
   • Job description development needed

## Decisions Made

• Approved resource reallocation to support engineering team for product launch
• Confirmed creation of new Customer Success position
• Accepted potential timeline adjustment for product launch if necessary

## Action Items

| Task | Owner | Deadline |
|------|-------|----------|
| Meet with engineering team and report on resource needs | Mike R. | Friday |
| Draft job description for Customer Success role | Jennifer W. | Next Tuesday |

## Additional Notes

• Board previously approved 15% marketing budget increase
• Timeline flexibility acknowledged for product launch quality assurance
```

---

## 🔧 Troubleshooting & Tips

### Common Issues and Solutions

#### **Issue: Inconsistent Speaker Names**
**Problem:** Transcript has "Sarah", "S. Chen", "Sarah C." for same person
**Solution:** Add preprocessing instruction:
```
Before analysis, standardize all speaker names to "FirstName LastInitial" format 
(e.g., "Sarah C.") throughout the transcript.
```

#### **Issue: Missing Action Items**
**Problem:** AI misses implied action items or responsibilities
**Solution:** Enhance the action items section:
```
Extract both explicit and implied action items. Look for:
• Commitments to follow up ("I'll check on that")
• Assignments ("You should handle this")  
• Next steps ("We need to...")
• Information requests ("Can you find out...")
```

#### **Issue: Too Much Detail**
**Problem:** Output includes every minor discussion point
**Solution:** Add filtering criteria:
```
Focus only on discussions that result in:
• Decisions or agreements
• Action items or assignments  
• Changes to plans or strategy
• Important concerns or risks
```

#### **Issue: Poor Action Item Formatting**  
**Problem:** Action items are vague or not actionable
**Solution:** Strengthen the phrasing requirements:
```
Each action item must:
• Start with an action verb (Complete, Review, Send, etc.)
• Be specific and measurable
• Include context if needed for clarity
Example: "Send Q3 financial report to board members" not "Financial reporting"
```

### Quality Improvement Tips

#### **For Better Summaries:**
- Include meeting duration and participant count
- Mention if any decisions were unanimous or contested
- Note meeting type (regular, ad-hoc, emergency)

#### **For Better Action Items:**
- Always include the specific deliverable
- Note dependencies between tasks
- Flag urgent or high-priority items

#### **For Better Discussion Tracking:**
- Group related topics that span multiple parts of meeting
- Note when topics are tabled for later discussion
- Highlight unresolved issues

### Model-Specific Optimization

#### **GPT-4 Settings:**
- Temperature: 0.1-0.2 (for consistent formatting)
- Max tokens: Adjust based on meeting length
- Top-p: 0.9 (for focused but natural language)

#### **Claude Settings:**
- Use explicit formatting instructions
- Break very long transcripts into sections
- Emphasize the table format requirement

---

## 🔗 Integration Strategies

### Workflow Integration Options

#### **Option 1: Manual Copy-Paste**
1. Record meeting with Zoom/Teams
2. Generate transcript via platform
3. Copy transcript to AI tool with this prompt
4. Review and distribute output

#### **Option 2: API Integration**  
```python
def analyze_meeting_transcript(transcript_text):
    response = openai.ChatCompletion.create(
        model="gpt-4",
        messages=[
            {"role": "system", "content": MEETING_ANALYSIS_PROMPT},
            {"role": "user", "content": transcript_text}
        ],
        temperature=0.1
    )
    return response.choices[0].message.content
```

#### **Option 3: n8n Workflow Automation**
- Webhook trigger from meeting platform
- Transcript processing node
- AI analysis node  
- Email/Slack distribution node

### Tools That Work Well With This Prompt

#### **Meeting Recording Platforms:**
- Zoom (auto-transcription)
- Microsoft Teams (live transcription)
- Google Meet (captions)
- Otter.ai (specialized transcription)

#### **AI Platforms:**
- ChatGPT Plus/Pro (web interface)
- Claude (Anthropic)
- OpenAI API (programmatic)
- Azure OpenAI (enterprise)

#### **Integration Platforms:**
- Zapier (no-code automation)
- n8n (open-source automation)
- Microsoft Power Automate
- Custom API development

---

## 📊 Success Metrics

Track these metrics to measure prompt effectiveness:

- **Accuracy:** % of action items correctly identified
- **Completeness:** % of key decisions captured  
- **Usability:** Time saved vs manual note-taking
- **Consistency:** Format adherence across different meetings
- **Stakeholder Satisfaction:** Feedback on output quality

---

## 🤝 Contributing

Found ways to improve this prompt? Here's how to contribute:

1. **Test variations** with different meeting types
2. **Document results** - what works, what doesn't
3. **Submit improvements** via pull request
4. **Share use cases** - how you adapted it for your needs

---

## 📄 License & Attribution

This prompt resource is part of the IPN Startup Resources repository.  
Licensed under MIT License - see main repository for details.

Created by [Amyn Porbanderwala](https://github.com/aporb) for the builder community.

---

*Built with ❤️ for better meetings everywhere*