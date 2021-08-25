# Contributing to this project

## 🔰 Getting started

### Before you begin:

-  This site is powered by [Hugo](https://https://gohugo.io/) and [TailwindCSS](https://tailwindcss.com/). Also TailwindCSS requires Node.js.
-  Have you read the [code of conduct](CODE_OF_CONDUCT.md)?
-  The contents (i.e syllabi) are written in Markdown files. So, if you want to contribute to content, you need to have idea of how Markdown works. You don't know anything about programming, but you do know about Markdown, you are good to go.
-  You also need to know about Git and Pull Requests. If you don't know about these, you can still help us and contribute through [Issues](#issues).

### Prerequisites

You've decided to contribute, that's great! To contribute to the documentation, you need a few tools.

Contributing to the project requires a GitHub account. If you don't have an account, follow the instructions for the [GitHub account setup](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account) to setup one.

### Download

This is for those who want to contribute through pull request.

If you only want to contribute to content, you can go ahead without having to install or setup anything. [Read more.](#using-github-web-editor)

If you want to contribute to website's source code or both source code and content, then install the following tools:

-  Git
-  Visual Studio Code or any other code editor
-  GoLang
-  Hugo `0.86.0+`
-  Node.js `v14.0+` (for TailwindCSS)
-  TailwindCSS `v2.2+`

### Ready to make a change? Fork the repo.

Go ahead. Fork the repo and start making changes.

### Make your update:

Make your changes to the file(s) you'd like to update.

Are you making changes to the source code? You'll need Hugo, TailwindCSS and Node.js to run the site locally.

### Submit your PR & get it reviewed

Once you submit your PR, others from the community will review it with you. The first thing you're going to want to do is a [self review](#self-review).

After that, we may have questions, check back on your PR to keep up with the conversation.

Did you have an issue, like a merge conflict? Check out this [git tutorial](https://lab.github.com/githubtraining/managing-merge-conflicts) on how to resolve merge conflicts and other issues.

### Your PR is merged!

Congratulations! The whole Syllabus Nepal community thanks you. ✨

Once your PR is merged, you will be proudly listed as a contributor in the contributor chart.

### Keep contributing as you use Syllabus Nepal

Now that you're a part of the Syllabus Nepal's community, you can keep participating and contributing in many ways.

## Types of contributions

You can contribute to the Syllabus Nepal's content and site in several ways.

### 🪲 Issues

Issues are used to track tasks that contributors can help with.

If you've found something in the content or the website that

-  should be updated, or
-  is missing or needed to be added on top,
-  and, you don't want to go trough hassle of messing around with source code or the pain of creating pull request

search open issues to see if someone else has reported the same thing. If it's something new, [open an issue using a template](https://github.com/syllabusnepal/syllabusnepal/issues/new/choose). We'll use the issue to have a conversation about the problem you want to fix.

### 🎏 Pull requests

A pull request is an another way to suggest changes in our project.

If you are someone who knows programming and about how SSGs, especially Hugo, works, you can contribute through pull request.

When we merge those changes, they should be deployed to the live site within 24 hours. It's usually deployed in few minutes.

To learn more about opening a pull request in this repo, see [Opening a pull request](#opening-a-pull-request) below.

## Starting with an issue

You can browse existing issues to find something that needs help!

### Labels

Labels can help you find an issue you'd like to help with.

-  The [`content` label]() is for problems or updates in the content. These will usually require some knowledge of Markdown.
-  The [`engineering` label]() is for problems or updates in the website. These will usually require some knowledge of HTML/CSS and Hugo to fix it.

## Opening a pull request

You can use the GitHub user interface ✏️ for some small changes, like fixing a typo or updating a readme. You can also fork the repo and then clone it locally, to view changes and run your tests on your machine.

### Fork and Clone

Assuming you have got everything installed, you can go ahead and fork this repository, and then clone it to your computer, and start tinkering in whatever you would like to. When you have added meaningful changes to either source code or content, create a pull request.

### Using GitHub Web Editor

**Disclaimer:** Use of web editor requires confidence about the changes you're about to make. Because the Web Editor can't compile/build/run anything, you won't be able to compile the changes and check the preview. You will need to wait until your pull request is reviewed and merged.

Navigate to home page of this repository. While you are there, press <kbd>.</kbd> (period/full-stop key) on your keyboard. You will get an online code editor based on Visual Studio Code.

**Note:** This shortcut key works for any other public or private repository, except archived repository. Only requirement is you need to be logged in to GitHub.

After that you can make changes to content (.md files) or add new contents. Additionally, you can make changes to source code, if you're confident enough.

## How to add content (syllabuses)?

The syllabi are in `/content` folder. It is structured in the following order:

`/content/<college|board|university_short_name>/<subject_short_name>/<subject_code>.md`

In each folder, you will find, `_index.md` file, which is for the main page of that college/board/university or subject. It only contains front matter with two properties.

```c
---
Title: " "
short_title: " "
---
```

For example, you need to add syllabus of `CSC 110 - C Programming` for `Tribhuvan University (TU)`, do the following:

**Note 1:** To ease the process, Step 1 and 2 has been already done for many universities/board. You can skip to step 3.

**Note 2:** The sentences starting with `//` are not to be copied in the `*.md` files. Remove those lines in your actual files.

**Note 3:** You can always refers to existing published `*.md` files, if you have trouble at any point.

1. Create a folder named `tu` in `/content`. Don't create new folder if one already exists there.
2. If you have created a new folder for university/board, add a `_index.md` file in that folder. In the `_index.md`, add these lines:

```c
---
Title: " "
// Full name of university/board. If abbreviated name is more recognized, use that.
// Tribhuvan University, not TU
// S.E.E, not Secondary Education Examination
short_title: " "
// Short abbreviated name of university/board. If the name is already used, try/create another meaningful name.
---
```

3. Create a folder inside the folder of college/university/board. In our example, it's `tu`. Create a folder inside the folder `tu` and name it `csc`. The name of these folder will always be the first abbreviated letters in the subject code.
   <br/>
   Now it should look like this:

```shell
content
|--tu
|  |-- csc
|  |-- _index.md
:  :
```

4. Add `_index.md` to `csc` folder. Add these lines to it:

```c
---
Title: " "
// Full name of the subject, not the faculty or stream. If full name is not available, use the regular short name.
// Computer Scienec for CSC, not CSIT or Computer Science and Information Technology
// If 'CSC' doesn't have full name, use 'CSC' itself.

short_title: " "
// The regular short name used in the subject code.
// 'CSC' for our example.
---
```

5. Since our subject was `CSC 110 - C Programming`, we wi;; know create a file named `110.md`. The name of fie will be the numeric code of the subject. This file contains the main content i.e. syllabus of the subject `CSC 110 - C Programming`. <br/>Now the file/folder structure will look something like this:

```shell
content
|--tu
|  |-- csc
|  |   |-- _index.md
|  |   |-- 110.md
|  |   :
|  |-- _index.md
:  :   :
```

6. Add these lines to the `110.md`:

```C
---
Title: "C Programming"
// Full name of the subject, without the subject code.
// 'C Programming'  in our case.
short_title: "CSC 110"
// The full subject code.
// CSC 110 in our case.
Level: "Bachelor"
// Level for which this subject is taught.
Program: "B.Sc. CSIT"
// Program/Faculty in which this subject is taught. Short form is recommended.
Year: "I"
// Year in which this subject is taught.
Semester: "I"
// Semester in which this subject is taught.
Credits: 3
// Credit hour of the subject
Full_Mark: 100
// Full Mark of the subject
Passing_Mark: 32
// Passing Mark of the subject
Date: "2021/08/24 10:45AM"
// Date on which the content was originally created.
Last_Updated: "2021/08/24 11:00PM"
// Date on which recent changes are made.
---
// Now add the content/syllabus, below this line.
```

7. Now, when you're done adding the content, commit the changes and create a pull request. <br/>Add proper commit message. <br/>Eg: `Added CSC 110 in TU`. <br/>This will be enough. No need to make it wordy.
   <br/>(You can refer to this guide, on [how to create pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).)

8. Hurray! 🎉🎉 You have done it. <br/>Now, you need to wait patiently for us to review the changes and merge it to main website.

## Reviewing

We will review every single PR. The purpose of reviews is to create the best content we can for people who use GitHub.

💚 Reviews are always respectful, acknowledging that everyone did the best possible job with the knowledge they had at the time.

💚 Reviews discuss content, not the person who created it.

💚 Reviews are constructive and start conversation around feedback.

### Self review

You should always review your own PR first.

For content changes, make sure that you/r:

-  [ ] Confirm that the changes meet the user experience and goals outlined in the content design plan (if there is one).
-  [ ] Review the content for grammatical accuracy.
-  [ ] Changes are not vague or redundant.

### Suggested changes

We may ask for changes to be made before a PR can be merged, either using [suggested changes](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/incorporating-feedback-in-your-pull-request) or pull request comments. You can apply suggested changes directly through the UI. You can make any other changes in your fork, then commit them to your branch.

As you update your PR and apply changes, mark each conversation as [resolved](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/commenting-on-a-pull-request#resolving-conversations).
