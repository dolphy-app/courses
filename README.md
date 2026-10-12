<p align="center">
  <img src=".github/logo.svg" width="72" alt="Dolphy logo">
</p>

<h1 align="center">Dolphy courses</h1>

<p align="center">
  <b>Open courses that check your answers by running them.</b><br>
  Lessons are plain Markdown, exercises are graded automatically.
</p>

<p align="center">
  <a href="https://github.com/dolphy-app/courses/actions/workflows/validate.yml"><img src="https://github.com/dolphy-app/courses/actions/workflows/validate.yml/badge.svg?branch=main" alt="Course validation status"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-CC%20BY--NC%204.0-lightgrey" alt="CC BY-NC 4.0 license"></a>
</p>

<p align="center">
  <a href="#courses">Courses</a> ·
  <a href="#add-a-course-to-dolphy">Add to Dolphy</a> ·
  <a href="CONTRIBUTING.md">Contribute a course</a> ·
  <a href="https://github.com/dolphy-app/dolphy">Dolphy app</a>
</p>

The course library for [Dolphy](https://github.com/dolphy-app/dolphy), the desktop app that plans your study as a graph of lessons and schedules reviews with spaced repetition. Each course is a folder of Markdown and JSON files, so you can read it in any editor, keep it in Git and improve it with a pull request.

## Courses

| Course                   | Language | What you get                                                                                                                                 |
| ------------------------ | -------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| [JavaScript](javascript) | Russian  | The JavaScript language from variables to async, generators and modules: 93 lessons and over 800 exercises, every one checked automatically. |

## Add a course to Dolphy

1. In Dolphy, open **Courses → Add from Git**.
2. Paste `https://github.com/dolphy-app/courses` and confirm. The branch field can stay empty.
3. Start learning. Update the course later from **Settings → Library → Repositories**.

The JavaScript course uses two exercise types that ship with the app: multiple choice and code that is checked by running tests.

## Contribute

Found a mistake, or want to write a course? See [CONTRIBUTING.md](CONTRIBUTING.md) for the format, the exercise types and how to validate your course locally.

## License

[CC BY-NC 4.0](LICENSE). The JavaScript course is derived from a non-commercial tutorial; see [NOTICE](NOTICE).
