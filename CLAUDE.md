# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is Tony Siu's GitHub profile repository (Tony363/Tony363). The main file is README.md which serves as the GitHub profile display when visitors view the profile at github.com/Tony363.

## Project Structure

- `README.md` - GitHub profile README that displays on the main profile page
- `.qodo/` - Qodo AI configuration directory (currently empty)
- `.git/` - Git version control directory

## Common Development Tasks

### Updating the Profile README

The README.md uses various GitHub profile enhancement tools and badges:
- GitHub Profile Trophy (github-profile-trophy.vercel.app)
- GitHub Readme Stats (github-readme-stats.vercel.app)
- GitHub Streak Stats (github-readme-streak-stats.herokuapp.com)
- Social media badges and icons from shields.io
- Language/tool icons from devicons and vectorlogo repositories

### Key Profile Sections

1. **Header**: Name, title, and professional description
2. **Trophy Display**: GitHub achievements and milestones
3. **Current Work**: Active projects and learning goals
4. **Contact Information**: Email and social media links
5. **Skills/Technologies**: Programming languages and tools expertise
6. **GitHub Statistics**: Contribution stats and streak counter

## Design Principles

- **Compactness**: Optimize vertical space usage to reduce scrolling
- **Visual Hierarchy**: Clear sections with appropriate spacing
- **Responsiveness**: Works well on different screen sizes
- **Professional Appearance**: Clean, organized layout that highlights key information

## Working with Profile Badges and Stats

When modifying stats cards or badges, common parameters include:
- `theme`: Color theme for stats cards (e.g., dark, radical, tokyonight)
- `show_icons`: Display icons on stats cards
- `hide_border`: Remove borders from cards
- `layout`: Compact or default layout options
- `row` and `column`: Control trophy display grid

## Best Practices

1. Test README changes by previewing in GitHub or using a local Markdown viewer
2. Ensure all external image links and badges are functional
3. Keep the profile concise and focused on key achievements and skills
4. Regularly update current projects and learning goals
5. Maintain consistent formatting and alignment throughout

## External Dependencies

This profile relies on several external services:
- Vercel-hosted stats generators (may have rate limits)
- GitHub's CDN for social media icons
- Various icon repositories for technology badges

When these services are down or rate-limited, some images may not display properly.