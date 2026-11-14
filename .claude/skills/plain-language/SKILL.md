---
name: plain-language
description: Writing rules for Perigee, based on Simplified Technical English (ASD-STE100), the controlled language of aviation documents. Use for all text. This includes chat replies, documents, code comments, commit messages, error messages and user interface text.
---

# Plain language rules

These rules follow the principles of ASD-STE100 Simplified Technical English.
They are a summary. They are not the full standard.
Apply them to each text that you write in this project.

## Sentences

- Write one topic in each sentence.
- An instruction has 20 words or less.
- A description has 25 words or less.
- A paragraph has 6 sentences or less.
- Use the active voice. Write "The scheduler starts the download." Do not write "The download is started by the scheduler."
- Use simple tenses: present, past and future.
- Write an instruction as a command. Start with the verb: "Run the tests."
- Write one instruction in each sentence. An exception is two actions that occur at the same time.
- If there is a condition, write the condition first: "If the build fails, read the log."
- Keep the articles "the" and "a". Do not write in telegram style.

## Words

- Use one word for one meaning. Use one meaning for each word.
- Use the same term for the same thing each time. Do not change the term for variety.
- Use a common, short word when it has the same meaning. Write "use", not "utilise". Write "start", not "initiate".
- Use the simple form of a verb. Write "to save the file", not "the saving of the file".
- Do not put more than three nouns in a row.
- Technical names are permitted: `rustfmt`, "Tauri command", "orbital element".
- Write numbers as digits. Write the unit after each number.
- Write times with the time zone.

## Text that is not permitted

- Emojis.
- Em dashes and en dashes. Use a period, a comma, a colon or parentheses.
- Exclamation marks.
- Idioms, metaphors and jokes.
- Praise for the reader or for the question.
- Filler at the start or the end of a reply. Examples: "Great question", "I hope this helps", "Let me know if".
- Marketing words. Examples: "seamless", "robust", "powerful", "blazing fast", "leverage", "delve", "elevate".
- Words that make a statement weak without a reason. Examples: "basically", "simply", "just", "really", "quite".
- Rhetorical questions.
- The pattern "It is not X, it is Y". Write what the thing is.
- Groups of three items when there are only two things to say.

## Structure

- Give the answer or the result first. Give the reasons after it.
- Use a numbered list for steps that have a sequence.
- Use a bullet list for items that have no sequence.
- Use a table to compare items.
- Write headings in sentence case. A heading is a short noun phrase.
- Use bold text only for a term that the reader must find quickly.
- Put commands, file names and code in code format.

## Uncertainty

- If you do not know a fact, write "I do not know" or "Not verified".
- Write the uncertainty one time, at the place where it applies.

## Commit messages and comments

- Commit title: imperative, 60 characters or less, no period. Example: "Add CelesTrak provider".
- A code comment gives the reason for the code. It does not repeat the code.

## User interface text

- A label is a noun or a short noun phrase: "Next launch".
- A button is a verb: "Refresh".
- An error message tells the user what occurred and what to do.
- Show the age of data: "Data from 14:05 UTC".

## Examples

| Do not write | Write |
| --- | --- |
| "Great question! Let's dive into how channels work." | "A channel moves values from one task to a different task." |
| "The app seamlessly leverages a robust caching layer." | "The app saves each response in a local cache." |
| "It's worth noting that the request might potentially fail." | "The request can fail." |
| "Simply run the command and you're good to go!" | "Run the command." |
| "The cache is not just storage, it is the single source of truth." | "The frontend reads all data from the cache." |

## Check before you send

1. Is each sentence in the word limit?
2. Is there an emoji, an em dash or an exclamation mark? Remove it.
3. Is the first sentence the answer?
4. Can you remove a sentence and lose no information? Remove it.
