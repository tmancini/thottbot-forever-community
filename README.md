# Thottbot Forever community

Player notes, screenshots, corrections and helpful votes for Thottbot Forever.

Open the relevant record page and choose **Add a note, screenshot, or correction**. Keep the record ID and game build in your issue. Describe your own observation, its location, and any uncertainty. Drag screenshots into the GitHub text box before submitting. Use the thumbs-up reaction on an issue to mark it helpful.

Submissions require GitHub sign-in. A maintainer adds the `approved` label to posts suitable for display. Approval publishes the post's author, text, screenshots, build and vote count in `posts.json`. Data corrections require a separate source review before changing game records.

## Maintainer refresh

The private site repository contains `scripts/sync_community.py`. Run it with `--output /path/to/this/repository/posts.json`, review the exported file, then commit and push this repository. The site reads this static file when a visitor chooses **Check for approved posts**. Copy the same JSON into the site repository's `dist/data/community.json` and rebuild to include it in the next deployed snapshot.

Only issues labelled `approved` are exported. Issues closed as `not_planned` are excluded. The exporter makes at most four GitHub API requests and currently accepts at most 99 approved posts, failing visibly rather than silently truncating at 100. No scheduled job or paid service is enabled.
