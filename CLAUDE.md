# meijingbiao.github.io - Jingbiao Mei's Academic Homepage

## Site Overview
Jekyll-based academic personal website using the AcademicPages template (forked from Minimal Mistakes). Hosted on GitHub Pages at https://meijingbiao.github.io/.

## Key Files to Edit

| What | Where |
|------|-------|
| Site config, sidebar info, author links | `_config.yml` |
| Homepage (bio, news, education, experience) | `_pages/about.md` |
| Full CV page | `_pages/cv.md` |
| Navigation menu | `_data/navigation.yml` |
| CV data (JSON, used by cv-json layout) | `_data/cv.json` |
| Profile photo | `images/profile.png` |

## Content Collections

### Publications (`_publications/`)
One markdown file per paper. Naming: `YYYY-short-name.md`. Frontmatter fields:
- `title`, `collection: publications`, `category` (conferences/preprints/patents), `permalink`, `date`, `venue`, `paperurl`, `citation`
- `citation` field uses `<b>J. Mei</b>` to bold the author's name

### Projects/Portfolio (`_portfolio/`)
One markdown file per project. Naming: `portfolio-N-short-name.md`. Frontmatter: `title`, `excerpt`, `collection: portfolio`.

## Publication Categories (defined in `_config.yml`)
- `conferences` - Conference papers (NeurIPS, ACL, EMNLP, ICLR, NAACL, DAC, etc.)
- `preprints` - arXiv preprints
- `patents` - EP/CN patents

## Author Info
- **Name**: Jingbiao Mei
- **Email**: jingbiaomei@gmail.com (use Gmail, not Cambridge email)
- **Google Scholar**: https://scholar.google.com/citations?user=31bT80wAAAAJ
- **GitHub**: JingbiaoMei
- **Supervisor**: Prof. Bill Byrne (https://sites.google.com/view/bill-byrne/home/)
- **Blog**: https://jingbiao.me/

## Deployment
Push to `master` branch triggers GitHub Pages build automatically. No local Jekyll build needed.
