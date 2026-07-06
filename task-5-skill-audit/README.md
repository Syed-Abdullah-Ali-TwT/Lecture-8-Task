# Task 5 - Auditing a Skill Before Trusting It

## Skill I audited

The PDF skill from the official skills directory (the one Claude uses whenever it reads, creates, or edits PDF files).

## What it actually does

It's basically a cheat sheet telling Claude which tools to reach for depending on the PDF task, pulling text or tables out, merging or splitting pages, rotating, adding watermarks, filling out forms, password protecting files, or running OCR on scanned pages. It's not something running in the background on its own, more like a reference guide Claude reads when a PDF job comes up.

## What I checked

- Does it call out to any external server? No, everything runs locally through Python libraries (pypdf, pdfplumber, reportlab) and command line tools, no network calls anywhere in it.
- Does it deal with credentials or logins? No, nothing like that shows up anywhere.
- Does it send my data anywhere I wouldn't expect? No, it only touches the specific files I give it or ask it to make, nothing gets sent out on its own.

## My verdict

Safe to enable. It only works with files I hand it directly, doesn't need any login, and never touches the internet. Nothing in it could quietly leak data or do something outside what I actually asked for.
