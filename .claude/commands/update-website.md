# Update Personal Website

Update Jingbiao Mei's academic homepage at meijingbiao.github.io with new publications and/or CV changes.

## Workflow

### Step 1: Check for new publications

Fetch the Google Scholar page to find new papers:
- URL: https://scholar.google.com/citations?user=31bT80wAAAAJ
- Use WebFetch to extract all publication titles, authors, venues, and years
- Compare against existing files in `_publications/` to identify new papers

### Step 2: Add new publications

For each new paper not already in `_publications/`:

1. Create `_publications/YYYY-short-name.md` with this frontmatter:
```yaml
---
title: "Full Paper Title"
collection: publications
category: conferences  # or preprints or patents
permalink: /publication/YYYY-short-name
date: YYYY-MM-DD
venue: 'Venue Name Year'
paperurl: 'https://arxiv.org/abs/XXXX.XXXXX'  # if available
citation: 'Authors with <b>J. Mei</b> bolded. &quot;Title.&quot; <i>Venue</i>.'
---

Brief 1-2 sentence description of the paper.

[Paper](url) \| [Code](url)  # if available
```

2. Determine the category:
   - `conferences` for accepted papers at named venues (NeurIPS, ACL, EMNLP, ICLR, NAACL, etc.)
   - `preprints` for arXiv papers not yet accepted
   - `patents` for EP/CN patents

3. Always bold Jingbiao's name in citation: `<b>J. Mei</b>`
4. Use `*` after names for equal contribution where applicable

### Step 3: Update the News section

Add entries for newly accepted papers to the News section in `_pages/about.md`:
```markdown
- **[Mon YYYY]** Paper accepted at **VENUE YEAR**: *Paper Title*.
```
Keep news in reverse chronological order. Only add news for papers accepted at venues, not for arXiv preprints (unless they are significant).

### Step 4: Update CV if user provides a new one

If the user provides a new CV (PDF or docx):
- Read the CV to extract any new work experience, education, academic service, or skills
- Update `_pages/cv.md` with new entries
- Update `_pages/about.md` Work Experience section if new positions are added
- Update `_data/cv.json` if structural data changed
- If the CV contains a new photo, extract it and replace `images/profile.png`

### Step 5: Update portfolio/projects if needed

If user has new GitHub repos to showcase:
- Check https://github.com/JingbiaoMei for new non-fork repos
- Exclude repos that correspond to published papers (paper code repos)
- Create `_portfolio/portfolio-N-short-name.md` for genuinely new projects

### Step 6: Commit and push

```bash
git add -A
git commit -m "Update website: add new publications / update CV"
git push origin master
```

## Important Notes

- Email is `jingbiaomei@gmail.com` (Gmail, NOT Cambridge email)
- Bill Byrne's page: https://sites.google.com/view/bill-byrne/home/
- Blog: https://jingbiao.me/
- Publication categories in `_config.yml`: conferences, preprints, patents
- Site deploys automatically on push to master via GitHub Pages

## Arguments

$ARGUMENTS - Optional: path to a new CV file (PDF or docx), or "publications-only" to skip CV update
