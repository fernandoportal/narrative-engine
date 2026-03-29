# Narrative Onboarding Guide

## Purpose

Guide new users through their first steps in Narrative Engine, ensuring they have their own copy of the repository and understand the basic workflow.

## Use This Skill When

- The user wants to start a new story or use the narrative engine for the first time.
- The user asks how to onboard.
- The user invokes the onboarding prompt.

## Behavior Rules

- Be conversational but concise.
- Ask one question at a time and wait for a response.
- Guide the user step-by-step.
- Start by ensuring they have their own repository fork.

## Step-by-Step Flow

### Step 1: Welcome & Account Check
Say: "Welcome to Narrative Engine! Before we start writing, let's make sure you have your own workspace."
Ask: "Do you already have a GitHub account?"
- If **Yes**, proceed to Step 2.
- If **No**, say: "Please go to [GitHub.com](https://github.com) and create a free account. Let me know when you're done!" and wait.

### Step 2: Repository Forking
Say: "Great! Since this is a template system, the best way to start is by creating a 'Fork' of this repository."
Explain: "A fork is your own personal copy of the project where you can safely save your story ideas and track all your changes. It's the recommended way to use Narrative Engine for your own projects."
Ask: "Please go to the Narrative Engine repository in your browser and click the 'Fork' button (or 'Use this template' if available). Have you created your fork and opened it here?"
- Wait for the user to confirm.

### Step 3: Story Logline
Say: "Perfect! Now we can start writing. Open `story/logline.md`."
Ask: "What is your story about in one sentence?"
- Once provided, refine it lightly and tell them to replace the content in `story/logline.md` with the new logline.

### Step 4: Protagonist Profile
Say: "Every good story needs a strong protagonist."
Ask: "Who is your main character? Give me their name, age, one key trait, and a core problem they are facing."
- Once provided, generate a short profile and instruct them to save it in `characters/protagonist.md`.

### Step 5: Simple Structure
Say: "Let's define a basic structure."
Ask: "What is the beginning situation, the midpoint that changes everything, and a powerful ending?"
- Once provided, format it as opening/midpoint/ending beats and instruct them to add this to `structure/beat-sheet.md`.

### Step 6: First Scene Draft
Say: "Now for the fun part: let's write your first scene."
Ask: "Where does your story begin (setting and time)?"
- Generate a short Fountain syntax scene and instruct them to save it in `screenplay/selected-scenes/opening.fountain`.

### Step 7: Wrapping Up
Say: "Congratulations! You now have a working story system with a logline, protagonist, structure, and your first scene. You can continue expanding your story module by module. Remember to ask me to 'save my narrative changes' whenever you want to version your progress!"
