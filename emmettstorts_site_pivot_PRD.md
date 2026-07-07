# PRD: emmettstorts.com — Pivot to a Build-in-Public Portfolio

| Field | Value |
|---|---|
| Owner | Emmett Storts |
| Status | Draft for build |
| Version | 1.0 |
| Stack | Jekyll + GitHub Pages, DNS on AWS Route 53 |
| Copy authorship | Emmett writes all copy. This PRD gives specs and voice, not finished copy. |

---

## 1. Overview and problem

The site currently reads as a freelance data-scientist storefront. That framing now works against the goal. Emmett is seeking a full-time product and experimentation data-science role at a mid-size, product-led company, and building ClickFrame and related projects on the side. The site needs to reposition around that goal and become the hub of a build-in-public strategy.

This is two jobs in one release. First, strip the freelance framing and reposition the copy. Second, add the infrastructure build-in-public requires: a writing feed and individual project pages that can show depth over time.

### The strategic model this site implements

Three ideas govern every decision below.

1. **Hub and spoke.** The site is the hub, the one property Emmett owns outright, where the canonical version of every project and post lives. Medium, LinkedIn, and Towards Data Science are spokes that point attention back to the hub. Rationale: Towards Data Science, the field's largest publication, left Medium in early 2025 specifically to protect its domain authority and search visibility after Medium redirected its custom domain. Owning the canonical copy is the lesson at the individual level too.
2. **Progressive disclosure funnel.** Resume, LinkedIn, and website are not redundant. They are tuned to escalating levels of a hiring manager's attention. The resume is the trailer (a seconds-long scan). LinkedIn is the standardized profile where recruiters search (the discovery front door). The website is the director's cut for the person already interested and checking whether Emmett can do the work in practice.
3. **Content is the top of a relationship funnel, not the referral itself.** Publishing generates pageviews. Referrals come from the one-to-one conversations that pageviews start. The site's job is to make a reader want that conversation and to make booking one frictionless. Rationale: referrals are a small share of applicants but a large share of hires, and referred candidates are several times more likely to get an offer than cold applicants, but that payoff sits on the far side of a conversation.

---

## 2. Goals and non-goals

### Goals
- Reposition all copy from freelance-for-hire to full-time-seeking, full-stack data scientist who builds in public.
- Lead with the differentiator: end-to-end ownership of a whole data function, with a causal-inference and experimentation specialty.
- Stand up a writing feed and project pages so depth can accumulate over time.
- Make the resume downloadable in one click and the intro call one click to book.
- Preserve third-party credibility (Toptal) reframed as validation, not a freelance pitch.
- Make the site legible to search and to link-preview cards so the spokes work.

### Non-goals
- No redesign of the visual system or structure. Structure is confirmed correct.
- No paid tooling, backend, or database. Stay static on GitHub Pages.
- No freelance service pages, rate cards, or "work with me on your project" flows.
- No gated content. Nothing sits behind an email form.

---

## 3. Success metrics

Attribution for a personal site is inherently fuzzy, so treat these as directional, not precise.

**Leading indicators**
- Intro calls booked through the CTA.
- Resume downloads.
- Click-through from a LinkedIn or Towards Data Science post to the site.
- Returning visitors to the writing feed (a proxy for a following forming).

**Lagging indicators**
- Interviews or referrals where the person references the site or a specific post or project.
- Offers.

Recommend adding privacy-friendly analytics (for example Plausible or GA4) so these are measurable. Flagged as an open question in section 12.

---

## 4. Audience and personas

**Primary: the hiring manager or recruiter at a mid-size, product-led company (roughly 150 to 1,500 people).** Skims first, goes deep only if interested. Wants evidence that Emmett can own problems end to end and reason causally, not a list of tools. This reader governs the default framing of every page.

**Secondary: the Denver data community and startup peers.** Meetup and Colorado Startups contacts who might read a post, start a conversation, and become a referral path. The writing feed serves this reader most.

**Tertiary: ClickFrame-adjacent contacts.** Founders and creators who find Emmett through the product. Lower priority for this site; ClickFrame's own properties serve them.

Design rule when audiences conflict: the hiring manager wins. In particular, ClickFrame is presented as proof Emmett can build and think, not as a startup he is scaling.

---

## 5. Positioning and messaging

### Core positioning statement (internal, not for the page)
Full-stack data scientist with eight years across the full data stack, from ETL pipelines and causal inference to production ML, who owns a data function end to end and is currently building in public. Open to full-time product and experimentation roles.

### The one differentiator to lead with
End-to-end ownership plus causal rigor. Most data scientists predict what will happen. Emmett's applied-economics background means he can explain why and then build the system that acts on it. Every top-of-page message should ladder up to this.

### Before and after framing

| Element | Freelance framing (remove) | New framing (write toward) |
|---|---|---|
| Identity | Freelance data scientist for hire | Full-stack data scientist, open to full-time |
| Value proposition | Services I offer to clients | Problems I own end to end, with a causal edge |
| Proof | Deliverables for clients | Shipped systems, quantified outcomes, work shown in public |
| Call to action | Discuss your project or engagement | Book a 30-minute intro call |
| ClickFrame | A venture or product for sale | Evidence I can build and reason, shown as it develops |
| Toptal | Reason to hire me for contract work | Third-party validation of skill |

### Copy cues to delete on sight
Any instance of: rates or pricing, "services," "hire me for your project," "available for contract or freelance," "let's work together on your engagement," client-deliverable language, or an outdated seniority or tenure claim (for example "five years" or "data analyst"). The current LinkedIn cache still shows some of this older framing, so assume the site does too.

---

## 6. Voice and tone (you are writing the copy, so this is the spec that matters most)

Write in Emmett's own voice, which is direct, specific, and evidence-first. The rules below are the contract.

**Do**
- Lead with a specific, quantified outcome, then the mechanism behind it. Show the "why," not just the "what."
- Use concrete numbers and named results wherever the resume already has them (for example an engagement lift, a cost reduction, an experiment count).
- Prefer plain, senior, confident language. State what you did and what happened.
- Use analogies and mental models in longer writing where they clarify a hard idea. Keep them out of tight page copy like the hero.
- Show reasoning, not only the finished artifact. That is the point of building in public.
- Write in first person.

**Do not**
- Open with adjective soup ("passionate, detail-oriented data scientist").
- Use buzzword stacks with no evidence attached.
- Use em dashes. Break the thought into separate sentences instead. This is a hard rule for all site copy.
- Hedge or undersell. No "I have some experience with."
- Frame anything as a service or a sales pitch.

**Voice illustration (pattern only, not your copy).** Weak: "Experienced in A/B testing and experimentation." Strong pattern: "Ran 23 experiments at Product Hunt. One informed a redesign that lifted engagement 18 percent. I care about which lever moved the metric, not just the lift." Notice the shape: result first, mechanism second, no em dash. Reproduce that shape in your own words for each claim.

---

## 7. Information architecture

Keep the existing top-level structure. Add two things: a writing index and a projects system.

```
/                 Home (hero, positioning, featured projects, selected experience, CTA)
/about            About (narrative, full-stack story, causal edge, Toptal validation)
/projects         Projects index (grid or list of all projects)
/projects/:slug   Individual project detail page  [NEW]
/writing          Writing index (reverse-chronological feed of posts)  [NEW]
/writing/:slug    Individual post  [NEW, standard Jekyll _posts]
/resume           Optional dedicated resume view, or a download button in nav and footer
Global            Nav and footer with LinkedIn, GitHub, Email, Resume download, CTA
```

Cross-linking is the build-in-public mechanic. A project page links to related posts, and a post links back to the project it is about. This is how an in-progress project shows momentum.

---

## 8. Section-by-section requirements

For each section: purpose, what it must communicate, proof to include, and what to avoid. You write the words.

### 8.1 Home hero
- **Purpose:** In one scan, make a hiring manager understand who you are and that you are available.
- **Must communicate:** full-stack data scientist, end-to-end ownership, causal and experimentation specialty, open to full-time.
- **Include:** a single sharp positioning line and a short supporting line. The primary CTA button (book a call) and a visible resume-download affordance.
- **Avoid:** freelance language, tool lists, vague adjectives.

### 8.2 About
- **Purpose:** The narrative version of the resume for the interested reader.
- **Must communicate:** the arc across WEC, Product Hunt, Medimap, and The Daily Wire as a story of owning whole data functions on small teams. The applied-economics "why not just what" thread. The builder's habit of shipping tools teams use.
- **Include:** the Toptal validation, framed as an outside party screened you (see 9.4). A short, honest line about building in public and ClickFrame, framed as evidence of range, not a competing venture.
- **Avoid:** anything that reads as a pitch for contract work.

### 8.3 Selected experience (on home or about)
- **Purpose:** Fast credibility through named companies and quantified outcomes.
- **Must communicate:** breadth (pipelines, experimentation, production ML) and impact.
- **Include:** three to five bullets, each result-first, drawn from the resume's strongest numbers.
- **Avoid:** responsibilities-style phrasing. Lead with outcomes.

### 8.4 Featured projects (on home)
- **Purpose:** Route the reader into the depth that lives on project pages.
- **Must communicate:** that you build real, deployed things.
- **Include:** two or three project cards linking to full project pages. ClickFrame is the flagship. Each card is one line of what it is plus one line of the interesting technical or measurement angle.
- **Avoid:** presenting ClickFrame as a startup you are growing.

### 8.5 Contact and CTA (see section 9 for functional detail)
- **Purpose:** Convert interest into a conversation with the least friction.
- **Must communicate:** an easy way to start a 30-minute conversation, plus email as a fallback.

---

## 9. Functional requirements

### 9.1 Resume download
- Commit the resume PDF into the repo, for example `/assets/resume/Emmett_Storts_Resume.pdf`.
- Add a clear "Download resume (PDF)" control in the nav and the footer, and near the hero.
- Use the HTML `download` attribute so it saves rather than opens in some browsers.
- **One source of truth.** The hosted PDF and the version you email must be the same file. Update in one place.
- **No form gate.** One click, no email capture.
- Nice to have: a dated filename or a small "updated [Month Year]" label so it reads as current.

### 9.2 Primary CTA: book a 30-minute call
- Replace the existing freelance CTA with a "Book a 30-minute intro call" action.
- Link to: `https://calendar.proton.me/bookings#m4lAEuGuIdGxJsiI4WlZYEDlgOZtu4QfnctbcAcRwVU=`
- Copy intent: an intro or opportunity conversation, not a project inquiry.
- Keep email as a lower-friction fallback directly beside it.
- **Verify:** confirm the Proton booking link opens or embeds cleanly across browsers. Booking widgets can be inconsistent.

### 9.3 Contact links
- LinkedIn: existing profile URL.
- GitHub: existing profile URL.
- Email: update everywhere to `emmett.storts@protonmail.com`. Confirm no typo before shipping.

### 9.4 Toptal badge
- Keep it, reframe its job. It is now third-party validation of skill, not a freelance CTA. Social proof lowers a hiring manager's perceived risk because an outside party already screened you.
- Placement: near your experience or in the footer, presented as a credential (for example a short line noting you were vetted in Toptal's top three percent), not as a "work with me" hook.
- Remove any surrounding copy that ties it to hiring you for freelance.

---

## 10. New infrastructure: writing feed and project pages

### 10.1 Writing feed
- Use standard Jekyll `_posts`, or a `_writing` collection if you prefer a distinct URL space.
- **Index page** at `/writing`: reverse-chronological list. Each item shows title, date, a one-line summary, and tags.
- **Post front matter:** `title`, `date`, `excerpt` or `description`, `tags`, and an optional `canonical_url` field for when a post originates here and is syndicated.
- **RSS or Atom feed** via the `jekyll-feed` plugin so followers can subscribe. This matters for building an audience.
- **First posts to seed** (from our plan): the causal YouTube thumbnail writeup (methodology version) and a ClickFrame architecture or disaster-recovery post.

### 10.2 Project pages
- Use a Jekyll `_projects` collection so each project is a markdown file with structured front matter.
- **Front matter per project:** `title`, `slug`, `status` (live, in progress, or archived), `role`, `stack` (list), `links` (live, repo, writeup), `summary`, optional `hero_image`, `date` or `last_updated`.
- **Index page** at `/projects`: a grid or list of project cards. Cards show title, status, one-line summary, and stack tags.
- **Detail page template** with these sections: Problem, Approach, What I built, Outcome or impact, Stack, Links. For in-progress work, add a Status line and a "Latest updates" area that links to related writing posts.
- **Cross-link** each project to its related posts and each post back to its project.

### 10.3 Proposed initial project set (confirm and prioritize)
- **ClickFrame** (flagship, status: in progress or live). Framed as a data product: the attribution and measurement pipeline, the Cloudflare and Supabase architecture, Stripe, GA4 and BigQuery, CI/CD, and the disaster-recovery work. Skills-evidence framing per section 5.
- **Library RAG Search (destiny-rag)** (live MVP). Pinecone hybrid search, OpenAI embeddings, GPT-4o-mini, a real stakeholder.
- **Causal YouTube thumbnail study** (in progress). Placeholder page now, filled in as the analysis and writeup land.
- **Colorado Catholic Business Directory** (live). Streamlit, data ingestion and cleaning, used at monthly meetings.
- **Selected work as case studies (optional):** Product Hunt experimentation, Daily Wire dbt and Snowflake overhaul and LTV model, Medimap cost reduction, WEC ML projects. Decide whether these become project pages or stay as resume bullets.

### 10.4 Reusable components (Jekyll includes)
Build these once and reuse: project card, post card, CTA block, resume-download button, Toptal badge, contact links.

---

## 11. SEO and discoverability

The hub only reinforces LinkedIn discovery if it is legible to search and to link previews.

- **Per-page titles and meta descriptions** with target keywords: product data scientist, experimentation, causal inference, full-stack data scientist, Denver.
- **Open Graph and Twitter Card meta on every page and post** (title, description, image) so links shared on LinkedIn and Towards Data Science render as clean cards. This directly affects click-through from the spokes.
- **Canonical tags.** Every page self-canonical. When you syndicate a post to Medium or Towards Data Science, set the canonical on the syndicated copy back to your site so you do not cannibalize your own ranking. This is the own-your-canonical mechanic.
- **Sitemap and robots** via `jekyll-sitemap`.
- Semantic HTML, mobile responsive, fast load (static already helps).

---

## 12. Open questions and assumptions

**Assumptions**
- Existing sections match the standard structure in section 7. If your section names differ, map these requirements onto them, or share the current copy and this can be rewritten in place.
- ClickFrame is a featured project, framed as skills-evidence, not a dedicated startup landing page.
- Domain and DNS need no change (already on Route 53).

**Open questions**
1. Analytics: do you want privacy-friendly analytics (Plausible) or GA4 to measure the success metrics in section 3?
2. Project set: confirm the initial lineup in 10.3 and which employment work becomes case-study pages versus resume-only.
3. Writing URL space: `_posts` at `/writing`, or a dedicated `_writing` collection?
4. Do you want a dedicated `/resume` page in addition to the PDF download, or is the download sufficient?

---

## 13. Phasing and rollout

Sequenced so the pressing problem is fixed first.

**Phase 1: reposition and fix (highest priority).** Rewrite copy on existing pages per sections 5, 6, and 8. Ship the functional changes: resume download (9.1), CTA and booking (9.2), email update (9.3), Toptal reframe (9.4). This removes the freelance framing that is actively hurting the job hunt.

**Phase 2: project pages.** Stand up the `_projects` collection, the index, the detail template, and the reusable components (10.2, 10.4). Build the initial project set (10.3), ClickFrame first.

**Phase 3: writing feed and syndication.** Stand up `/writing`, RSS, and Open Graph and canonical setup (10.1, 11). Publish the first two posts. Establish the syndication workflow to LinkedIn and Towards Data Science.

---

## 14. Definition of done

- [ ] No freelance, rate, or service language remains anywhere on the site.
- [ ] Hero communicates full-stack, causal edge, and open to full-time in one scan.
- [ ] Resume downloads in one click, no gate, single source of truth.
- [ ] Primary CTA books a 30-minute call via the Proton link, with email beside it.
- [ ] Email reads `emmett.storts@protonmail.com` everywhere, verified.
- [ ] Toptal badge present and reframed as validation.
- [ ] `/projects` index and at least the ClickFrame project page are live.
- [ ] `/writing` index and RSS are live with at least one post.
- [ ] Open Graph and canonical tags present on all pages and posts.
- [ ] Every page passes a mobile and link-preview check.
