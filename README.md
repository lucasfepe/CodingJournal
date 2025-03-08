# Luke's Coding Chronicle  

This journal is where I document my coding journey—what I'm working on, what worked, and the challenges I encountered along the way.  

## What to Expect  
- 🛠 **Projects & Tasks** – What I'm currently working on  
- 🔍 **Challenges** – Issues and roadblocks I faced  
- 💡 **Solutions & Insights** – Steps I took and lessons learned  

Whether it's debugging a tricky issue, learning a new framework, or optimizing code, this space will serve as both a personal reference and a way to track my progress.  

Let’s code, learn, and grow! 🚀  

---

## 📅 March 8, 2025  

### 🚀 **Portfolio Website**  

#### 🔧 What I Worked On  
Last night, I was refining the **project card expansion and collapse animations**. With **Amazon Q's** input and some tweaks, I got it looking pretty good.  

#### 🛑 The Challenge  
There is still a small issue—when I click to expand the card, sometimes the scrollbar for the cards section appears unexpectedly.  

#### 🤔 Root Cause  
After some thinking, I realized this might be due to the **50ms delay** that allows the portal to lift the card to the root before moving it. During this short period:  
- A **placeholder card** is created to prevent layout shifts.  
- The **original card is lifted** to the root for expansion.  
- However, for a brief moment, there are **two cards for the same card in the section**, which could be causing the scrollbar to appear.  

#### 💡 Potential Solution  
To fix this, I plan to **remove the 50ms delay** and see if:  
- The **portal setup and card movement** happen quickly enough before the animation starts.  
- This eliminates the temporary duplicate card issue.  

If that doesn’t work, I'll explore alternative approaches to ensure a **smooth expansion effect**.  