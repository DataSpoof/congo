# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A self-contained web development MCQ quiz application built with vanilla HTML, CSS, and JavaScript. The quiz presents 5 multiple-choice questions about web development fundamentals and displays a final score with personalized feedback.

## How to Run

Simply open `quiz.html` in any web browser. No build process, server, or dependencies required.

## Project Structure

The entire application is in a single file: `quiz.html`

**Structure:**
- `<head>`: Embedded CSS with styling for the quiz container, questions, options, and results display
- `<body>`: 
  - `#quiz` div: Contains all 5 questions with radio button options
  - `#result` div: Hidden initially, displays score and feedback after submission
- `<script>`: 
  - `submitQuiz()`: Collects answers, calculates score, shows results
  - `resetQuiz()`: Clears selections and resets UI for retaking

## Modifying the Quiz

**To add/change questions:**
- Duplicate a `.question-group` block in the quiz div
- Update the question text, add new options with unique `name` attributes
- In the JavaScript, add corresponding answer checking logic in `submitQuiz()`

**To update feedback messages:**
- Edit the `messages` object in `submitQuiz()` function to change score-based feedback

**To change styling:**
- All CSS is in the `<style>` tag; modify colors, fonts, layout as needed
- Key classes: `.container`, `.question-group`, `.options`, `.option`, `#result`
