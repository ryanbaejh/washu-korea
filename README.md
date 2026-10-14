# WashU Korean Community Website

## Data and Feature Requirements Outline

**Status: Draft for team review.** The features and information below are proposals to confirm before designing the database. They do not describe features that have already been built.

## 1. Purpose

The website will serve as a centralized resource for the Korean community at Washington University in St. Louis. It will organize information currently scattered across group chats, social media, club pages, and personal connections.

This outline explains what information the website may store, why it is needed, and what people should be able to do with it. Technical architecture and database design will be documented separately after the team agrees on the requirements.

| Area | Information organized | Features supported |
| --- | --- | --- |
| Accounts and profiles | Identity, contact details, WashU affiliation, profile preferences | Sign in, participate, edit a profile |
| Permissions | Account roles and management access | Control who can view, publish, and manage content |
| Forum | Boards, posts, tags, comments, attachments | Discussions, questions, announcements, information sharing |
| Events | Schedules, locations, organizers, registration links | Discover upcoming events and browse past events |
| Clubs | Descriptions, contacts, leadership, links, photos | Find organizations and learn how to join |
| People directory | Optional profile details and interests | Find community members |
| Alumni connections | Optional professional details and contact preferences | Find alumni and potential mentors |
| Gallery | Albums, photos, captions, event associations | Preserve and browse community memories |
| Administration | Content status, account status, management permissions | Maintain information and moderate participation |

## 2. User Accounts and Profiles

**Purpose:** Give members an identity on the website so they can participate in community features.

**Information we may store:**

- Name and display name or username.
- Email address and sign-in information. Passwords, if used, must never be stored as readable text.
- Profile picture and short biography.
- Relationship to WashU: undergraduate student, graduate student, alumni, faculty/staff, or other.
- Graduation year and major or program.
- Clubs or organizations the person chooses to list.
- Account creation date and account status, such as active or disabled.
- Choices about profile visibility and directory participation.

**Features:** Create an account, log in and out, edit a profile, upload a profile picture, publish posts and comments, and view profiles according to their visibility settings.

**To confirm:** Which fields are required, who can register, whether a WashU email is required, and how alumni or other community members can join. Account information should not automatically become public profile information.

## 3. Account Permissions

**Purpose:** Define who can participate in and manage each part of the website.

**Information we may store:** Each account's role, account status, and any permission to manage a particular club or its events.

| Proposed role | Possible abilities |
| --- | --- |
| Member | Create posts and comments, edit or delete their own content, and browse permitted resources |
| Admin | Moderate posts and comments, pin posts, lock discussions, and manage events, club information, and gallery content |
| Top admin / super admin | Create, rename, reorder, hide, or archive boards; assign or remove administrative access |
| Authorized club representative, if included | Manage their designated club's page and events |

The team should confirm the boundaries of each role. Board management and role assignment are proposed as top-admin responsibilities.

## 4. Forum Boards

**Purpose:** Organize community discussions into boards (게시판), similar to 네이버 카페.

Possible boards include 공지사항, 자유게시판, 질문게시판, 취업 / 커리어, 대학생활, 대학원, 맛집 / 생활정보, 중고거래, 이벤트, and 동문 게시판. These are examples, not a final board list.

**Information we may store:** Board name, description, display order, creator, visibility, active or archived status, and who may view or publish posts.

**Features:** Browse posts by board. Top admins can create, rename, describe, reorder, hide, and archive boards as community needs change—for example, adding a new-student board for a particular year.

## 5. Forum Posts

**Purpose:** Let members and administrators publish discussions, questions, resources, and announcements.

**Information we may store:**

- Title, main content, author, and board.
- Publication and last-edited dates.
- Attached images or files and associated tags.
- Whether the post is pinned, comments are allowed, or the post is hidden or deleted.

**Features:** Members can create, edit, and delete their own posts; add attachments and tags; search for posts; and filter by board or tag. Admins can pin posts, lock comments, move posts between boards, and hide or remove inappropriate content.

## 6. Tags

**Purpose:** Describe a post's topics in addition to the board where it belongs.

For example, a post titled “2027 Summer Software Engineering Internship List” could belong to 취업 / 커리어 and use the tags “Internship,” “Software Engineering,” and “Summer 2027.”

**Information we may store:** Tag name and, optionally, a description or display color/icon.

**Features:** Add tags to posts, select a tag to find related posts, and filter search results by tag.

**To confirm:** Whether members can create tags or must choose from tags maintained by admins.

## 7. Comments and Discussions

**Purpose:** Support conversations beneath forum posts.

**Information we may store:** Comment text, author, associated post, publication and last-edited dates, and hidden or deleted status.

**Features:** Add comments, edit or delete one's own comments, and let admins moderate comments. Replies to individual comments are a possible later feature; they would also identify which comment is being answered.

## 8. Events

**Purpose:** Provide a central place to find cultural events, club activities, career events, alumni gatherings, student meetups, and relevant university events.

**Information we may store:**

- Event name and description.
- Date, start and end times, and location or online meeting link.
- Organizer, related club, and contact information.
- Event image or poster and external registration link.
- Related announcement or forum post.
- Status, such as upcoming, completed, or cancelled.

**Features:** Browse upcoming and past events, view details, follow registration links, and find related announcements. Admins or authorized club representatives could create and update events.

**To confirm:** Whether members can submit events for approval and whether registration stays on external services. Collecting RSVPs or attendance on this website would be an additional requirement.

## 9. Clubs and Organizations

**Purpose:** Help users discover Korean or Korea-related WashU organizations, including cultural, professional, academic, religious, and social groups.

**Information we may store:**

- Full name, abbreviation, logo, description, and photos.
- Contact email, website, and social media links.
- Current leadership or designated contact people.
- Active or inactive status.
- Meeting details and instructions for joining, if provided.
- Associated events.

**Features:** Browse the club directory, open club profiles, find contacts and joining information, and see club events and photos.

**To confirm:** Whether site admins maintain all pages or designated club representatives manage their own pages. Listing a club on a person's profile does not necessarily mean the website manages official club membership.

## 10. People Directory

**Purpose:** Help community members find and connect with one another using the profile details people choose to share.

**Information we may display:** Name, picture, student/alumni status, graduation year, major or program, biography, interests, clubs, career field, and selected contact or social links.

**Features:** Browse profiles and search or filter by name, graduation year, major, affiliation, club, or career field.

**To confirm:** Whether directory participation is optional, which details are visible to visitors versus signed-in members, and whether directory entries require an account. Reuse profile information where possible so people do not need to maintain duplicate profiles.

## 11. Alumni Connections

**Purpose:** Help students discover alumni who choose to share professional information or offer guidance.

**Information we may store for participating alumni:**

- Name, graduation year, and degree or major.
- Industry, current job/company, location, and short biography.
- Areas where they are willing to help, such as career advice, internships, resume review, graduate school, or general mentoring.
- Whether they are currently open to contact and their preferred contact method.

**Features:** Find alumni by industry, major, graduation year, company, location, or mentoring interests, and use the contact options they choose to share.

Participation and contact availability should be opt-in. Alumni information could extend an existing community profile.

**To confirm:** Whether this belongs in the first release and whether contact uses external links or a future website messaging feature. Direct messaging and formal mentor matching are not yet agreed requirements.

## 12. Photo Gallery

**Purpose:** Preserve photos from community activities in browsable albums.

**Album information:** Title, description, event/date, cover photo, and creator. Example albums include a Chuseok festival, KSA barbecue, or welcome event.

**Photo information:** Image, caption, upload date, uploader, and display order within the album.

**Features:** Browse albums and photos; allow authorized contributors to create albums, upload photos, edit captions, and remove content.

**Possible later features:** Link albums to events, tag clubs or people, and add likes or reactions.

**To confirm:** Who can upload, whether uploads need approval, who can view albums, and how people request removal of a photo featuring them.

## 13. Announcements and Community Resources

**Purpose:** Make important information easy to find alongside general discussions.

Examples include organization announcements, deadlines, campus information, new-student guides, housing and transportation information, international-student resources, academic resources, and career resources.

**Information we may store:** Post title, content, author, publication and update dates, relevant links or attachments, board, tags, and pinned status—the same information used for forum posts.

**Features:** Publish announcements in designated boards, pin important information, and locate resources through boards, tags, and search. A separate announcement system is not currently required.

## 14. Search

**Purpose:** Help people find information as the website grows.

**Features:** Search posts, tags, events, clubs, and—if included—people and alumni. Relevant filters may include content type, board, tag, date, club, graduation year, major, and industry.

Search results must follow the same visibility choices as the underlying content. Private account details and hidden directory information should not appear in results.

## 15. Administrative Tools

**Purpose:** Let authorized people maintain the community's information without needing a developer for routine updates.

**Features may include:**

- Accounts: disable accounts and manage roles within the administrator's permissions.
- Forum: manage boards, moderate posts and comments, pin posts, and lock discussions.
- Events: create, edit, cancel, or remove listings.
- Clubs: add organizations and update information, contacts, and images.
- Gallery: create albums, upload photos, and remove content.
- People and alumni: hide inappropriate profiles and, if the team chooses, verify student or alumni affiliation.

**Information supporting these features:** Account roles and status, content visibility and status, and any affiliation verification status the team decides to use.

## 16. Decisions for Team Review

Before database design begins, confirm these questions and record the agreed answers.

| Area | Questions to resolve |
| --- | --- |
| Accounts | Who can register? Is a WashU email required? How can alumni join? Which profile fields are required? |
| Visibility | Which sections can visitors see? Which require login? Which profile fields can each audience see? |
| Directory | Is participation optional? Does every listed person need an account? |
| Alumni | Is networking part of the first release? How do alumni opt into contact, and what contact methods are supported? |
| Forum | What are the initial boards? Who can view and post in each? Who creates tags? Are comment replies needed at launch? |
| Permissions | What can members, admins, top admins, and club representatives each manage? |
| Events | Who can publish or submit events? Is approval required? Will registration remain external? |
| Clubs | Who maintains club pages? What information should every organization provide? |
| Gallery | Who can upload and view photos? Is approval required? Should albums connect to events? How are removal requests handled? |
| Content removal | What happens when someone deletes an account, post, comment, or profile? What information, if any, should remain? |
| Launch scope | Which areas are essential for the first release, and which can wait? |

## 17. Possible First-Release Scope

**Proposed initial scope, pending team agreement:**

- Accounts and basic profiles.
- Forum boards, posts, comments, and tags.
- Announcements and community resources through forum posts.
- Event listings.
- Club directory.
- Photo albums and gallery.
- Administrative controls needed to manage these areas.
- Search for the content included at launch.

**Possible later additions:** People directory, alumni directory and mentoring connections, replies to comments, photo tagging, and reactions.

For every approved feature, the team should agree on the information it needs and who can create, view, edit, or remove that information. Those decisions will guide the later database design.
