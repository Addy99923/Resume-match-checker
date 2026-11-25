# Resume and Job Match Checker

This is a small browser tool for comparing the text of a resume with a job description. I wanted a quick way to see which words from a job post are also present in a resume, and which ones I may have missed.

## How to use it

1. Open `index.html` in a browser.
2. Paste resume text into the first box.
3. Paste the job description into the second box.
4. Select **Analyze match** to see the percentage and the matched/missing terms.
5. Use **Clear** to start again.

## What is happening in the code

The JavaScript converts the text to lowercase, collects terms from the job description and checks whether each term appears in the resume text. A small list of common technical terms is grouped in `categories`, and common filler words are kept in `stopWords` so they are not counted as useful matches.

## Built with

HTML, CSS and plain JavaScript. There is no server or database; the comparison happens in the browser.

## Important limitation

The percentage is only a basic keyword-overlap estimate. It is not an ATS score and it cannot understand whether a skill is used in the right context, recognise every synonym or judge the quality of someone's experience. For example, mentioning a tool once is not the same as having practical experience with it. Review the result manually and never add a skill to a resume just to increase the percentage.

## Ideas for a next version

- Improve phrase matching so related terms are not counted as unrelated words.
- Let users add their own keywords.
- Highlight matched words in the pasted text.
- Add a few sample inputs so the tool is easier to try.
