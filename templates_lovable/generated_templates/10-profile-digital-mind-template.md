# Profile/Digital Mind Page Template - Technical Specification

**Page Type:** Public Profile Page
**URL Pattern:** `/{username}` or `/mind/{username}`
**Priority:** High
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## Page Overview

**Purpose:** Public-facing page for individual Digital Minds where users can learn about and interact with AI clones.

**Key Goals:**
- Showcase the Digital Mind's expertise and personality
- Enable immediate interaction (chat/voice/video)
- Build trust through social proof
- Drive conversions (try demo, sign up)
- SEO-friendly for discoverability

---

## Page Structure

### Block 01: Minimal Header
```
┌─────────────────────────────────────┐
│ [Delphi Logo]           [Try Free]  │
└─────────────────────────────────────┘
```

**Logo:**
- Link: `/` (homepage)
- Size: 100px × 28px

**CTA Button:**
- Text: "Create Your Own" or "Try Free"
- Link: `/signup`
- Style: Primary button, small

**Minimal:** No main navigation, keep focus on Digital Mind

---

### Block 02: Hero Section / Profile Header

```
┌─────────────────────────────────────┐
│                                     │
│     ┌────────────────┐              │
│     │                │              │
│     │  [Large Photo/ │              │
│     │   Avatar       │              │
│     │   200×200]     │              │
│     │                │              │
│     └────────────────┘              │
│                                     │
│  [Name]                             │
│  [Title/Expertise]                  │
│                                     │
│  [Short bio - 2-3 lines]            │
│                                     │
│  [Topics: Tag Tag Tag]              │
│                                     │
│  [Start Conversation Button]        │
│                                     │
│  🎤 Voice available  |  📹 Video available │
│                                     │
└─────────────────────────────────────┘
```

**Mobile:** Center-aligned, stacked
**Desktop:** Center or left-aligned with chat widget on right

---

### Profile Elements

**Profile Photo:**
- Size Mobile: 150px × 150px
- Size Desktop: 200px × 200px
- Border-radius: 50% (circle) or 16px (rounded square)
- Border: 4px solid #F3F4F6
- Shadow: 0 4px 6px rgba(0,0,0,0.1)
- Position: Center
- Alt text: "{Name}'s Digital Mind"

**Name:**
- Text: "Dr. Mark Hyman" (example)
- Font size Mobile: 28px / 34px
- Font size Desktop: 36px / 44px
- Font weight: 700
- Margin: 16px 0 4px
- Text align: Center (mobile), Left (desktop optional)

**Title/Expertise:**
- Text: "Functional Medicine Pioneer & Health Expert"
- Font size: 16px / 22px (mobile), 18px / 26px (desktop)
- Color: Primary color (#6366F1)
- Font weight: 500
- Margin-bottom: 16px

**Bio:**
- Text: "Helping you unlock optimal health through functional medicine, nutrition, and lifestyle. 30+ years of experience, 15 bestselling books, host of The Doctor's Farmacy podcast."
- Font size: 16px / 24px
- Color: Secondary text (#6B7280)
- Max-width: 600px
- Margin: 0 auto (mobile), 0 (desktop)
- Lines: 3-4 max

**Topic Tags:**
- Display: Flex, flex-wrap, justify center (mobile) or left (desktop)
- Gap: 8px
- Margin: 20px 0

**Tag Styling:**
- Background: #F3F4F6
- Color: #4B5563
- Padding: 6px 14px
- Border-radius: 16px
- Font size: 13px
- Font weight: 500

**Example Tags:** Nutrition, Longevity, Functional Medicine, Wellness

---

**Primary CTA Button:**
- Text: "Start Conversation" or "Talk to {Name}"
- Width Mobile: Full width (with 20px margin)
- Width Desktop: Auto (padding 24px 64px)
- Height: 56px
- Background: Primary color (#6366F1)
- Color: White
- Font size: 18px
- Font weight: 600
- Border-radius: 12px
- Margin-top: 24px
- Icon: Chat bubble (optional)
- Hover: Darken 10%, lift

**Capabilities Bar:**
- Display: Flex, gap 16px
- Font size: 14px
- Color: #6B7280
- Icons: 24px × 24px
- Text: "Voice available", "Video available"
- Position: Below CTA button
- Margin-top: 16px

**Container:**
- Background: White or light gradient
- Padding Mobile: 40px 20px
- Padding Desktop: 60px 40px
- Text align: Center (mobile)

---

### Block 03: Interactive Chat Widget (Primary Feature)

#### Mobile (Full-width below hero)
```
┌─────────────────────────────────────┐
│  [Chat Interface]                   │
│                                     │
│  ┌───────────────────────────────┐  │
│  │ Hi! Ask me anything about     │  │
│  │ functional medicine...        │  │
│  └───────────────────────────────┘  │
│                                     │
│  • How can I improve my gut health? │
│  • What supplements do you recommend?│
│  • Tell me about your approach      │
│                                     │
│  ┌───────────────────────────────┐  │
│  │ Type your message...      [→] │  │
│  └───────────────────────────────┘  │
│                                     │
│  [🎤 Voice] [📹 Video]              │
│                                     │
└─────────────────────────────────────┘
```

#### Desktop (Side-by-side or Modal)
**Option A: Fixed Right Panel**
```
┌────────────────┬───────────────────────┐
│                │                       │
│  [Profile      │  [Chat Widget]        │
│   Content]     │                       │
│                │  Chat interface       │
│                │  full height          │
│                │                       │
└────────────────┴───────────────────────┘
```

**Option B: Floating Modal**
- Click "Start Conversation" → Opens modal
- Size: 400px × 600px
- Position: Center or bottom-right
- Z-index: 1000

---

### Chat Widget Components

**Greeting Message:**
- Avatar: Small version (40px)
- Text: "Hi! I'm {Name}'s Digital Mind. Ask me anything about {topic}."
- Background: #F9FAFB
- Border-radius: 12px
- Padding: 12px 16px
- Max-width: 80%

**Suggested Questions:**
- Display: List of clickable pills
- Count: 3-5 questions
- Background: White
- Border: 1px solid #E5E7EB
- Padding: 10px 16px
- Border-radius: 20px
- Font size: 14px
- Margin: 8px 0
- Click: Populate input, send message

**Examples:**
- "How can I improve my gut health?"
- "What's your morning routine?"
- "Tell me about functional medicine"
- "What supplements do you recommend?"

**Message Display Area:**
- Height: 400px (mobile), 500px (desktop)
- Overflow-y: auto
- Padding: 16px
- Background: #FFFFFF
- Scroll to bottom on new message

**User Message Bubble:**
- Background: Primary color (#6366F1)
- Color: White
- Padding: 10px 14px
- Border-radius: 16px 16px 4px 16px
- Align: Right
- Max-width: 75%
- Font size: 15px / 20px
- Margin: 8px 0

**AI Response Bubble:**
- Background: #F3F4F6
- Color: Primary text
- Padding: 10px 14px
- Border-radius: 16px 16px 16px 4px
- Align: Left
- Max-width: 75%
- Font size: 15px / 20px
- Margin: 8px 0
- Avatar: Small (32px) to the left

**Typing Indicator:**
- Show: When AI is "thinking"
- Animation: Bouncing dots
- Text: "{Name} is typing..."
- Duration: 1-3 seconds

**Input Bar:**
- Height: 52px
- Border: 1px solid #E5E7EB
- Border-radius: 26px (fully rounded)
- Padding: 12px 48px 12px 16px (space for send button)
- Font size: 15px
- Placeholder: "Type your message..."
- Background: White

**Send Button:**
- Position: Absolute right 8px
- Size: 36px × 36px
- Background: Primary color
- Icon: Arrow or paper plane
- Border-radius: 50%
- Color: White
- Hover: Darken 10%
- Disabled: If input empty

**Voice/Video Buttons:**
- Display: Flex, gap 12px
- Position: Below input
- Margin-top: 12px
- Height: 40px
- Border: 1px solid #E5E7EB
- Border-radius: 20px
- Padding: 0 16px
- Font size: 14px
- Icon + Text
- Hover: Background #F9FAFB
- Click: Open voice/video interface

---

### Block 04: About Section (Extended Bio)

```
┌─────────────────────────────────────┐
│  [H2: About {Name}]                 │
│                                     │
│  [Longer bio paragraphs - 3-4]      │
│                                     │
│  [Credentials/Achievements list]    │
│                                     │
└─────────────────────────────────────┘
```

**H2:** "About Dr. Mark Hyman"
- Font size: 28px / 36px
- Font weight: 700
- Margin-bottom: 20px

**Bio Text:**
- Font size: 16px / 26px
- Color: Primary text
- Paragraphs: 3-4
- Max-width: 700px
- Margin: 0 auto (mobile), 0 (desktop)

**Credentials:**
- Display: List with checkmarks or bullets
- Font size: 15px / 22px
- Examples:
  - ✓ 30+ years in functional medicine
  - ✓ 15 New York Times bestselling books
  - ✓ Host of The Doctor's Farmacy podcast
  - ✓ Medical Director at Cleveland Clinic
  - ✓ Founder of The UltraWellness Center

**Container:**
- Background: #F9FAFB or White
- Padding: 60px 20px (mobile), 80px 40px (desktop)
- Max-width: 1100px
- Margin: 0 auto

---

### Block 05: Sample Conversations / FAQs

```
┌─────────────────────────────────────┐
│  [H2: Common Questions]             │
│                                     │
│  [Accordion Item 1] ▼               │
│  Q: How can I improve my gut health?│
│  A: [Expanded answer]               │
│                                     │
│  [Accordion Item 2] ▼               │
│  ...                                │
│                                     │
└─────────────────────────────────────┘
```

**Purpose:**
- Show examples of conversations
- SEO-friendly (indexable Q&A content)
- Build trust in AI responses

**Accordion:**
- Question: Font size 16px, weight 600
- Answer: Font size 15px / 22px, color secondary
- Expand: Smooth animation
- Max items: 5-8

**Questions (Examples):**
1. "What's the best diet for longevity?"
2. "How do I know if I have leaky gut?"
3. "What supplements should I take daily?"
4. "How can I improve my energy levels?"

---

### Block 06: Social Proof / Testimonials

```
┌─────────────────────────────────────┐
│  [H3: What People Are Saying]       │
│                                     │
│  ┌─────────────────────────────┐   │
│  │ ⭐⭐⭐⭐⭐                     │   │
│  │ "This is like having Dr.    │   │
│  │  Hyman on speed dial..."    │   │
│  │ - Sarah M.                  │   │
│  └─────────────────────────────┘   │
│  ...                                │
└─────────────────────────────────────┘
```

**Testimonial Card:**
- Rating: 5 stars
- Quote: 2-3 sentences
- Name: Initials or first name only
- Background: White
- Border: 1px solid #E5E7EB
- Padding: 24px
- Border-radius: 12px

**Grid:** 1-2 cards mobile, 3 cards desktop

---

### Block 07: Stats/Metrics (Optional)

```
┌─────────────────────────────────────┐
│  ┌──────────┬──────────┬──────────┐ │
│  │  10,000+ │   4.9    │  500+    │ │
│  │Conversations│ Rating │  Topics  │ │
│  └──────────┴──────────┴──────────┘ │
└─────────────────────────────────────┘
```

**Metrics:**
- Conversations held
- Average rating
- Topics covered
- Response time

**Styling:**
- Large number: 36px, weight 700, primary text
- Label: 14px, secondary text
- Center aligned
- Grid: 3 columns (stack on mobile)

---

### Block 08: CTA Banner

```
┌─────────────────────────────────────┐
│  [H3: Create Your Own Digital Mind] │
│  [Subtitle text]                    │
│  [Get Started Free Button]          │
└─────────────────────────────────────┘
```

**Purpose:** Convert visitors to users

**Background:** Gradient (#6366F1 to #4F46E5)
**Color:** White
**Padding:** 60px 20px (mobile), 80px 40px (desktop)
**Text align:** Center

---

### Block 09: Minimal Footer

```
┌─────────────────────────────────────┐
│  Powered by [Delphi]                │
│  [Create Your Own] · [Privacy]      │
└─────────────────────────────────────┘
```

**Minimal footer:**
- Text align: Center
- Font size: 14px
- Color: Secondary text
- Links: Underline on hover
- Padding: 32px 20px

---

## Chat Functionality

### Message Flow
1. User types message or clicks suggested question
2. Message appears in chat (right-aligned)
3. Show typing indicator (1-2 seconds)
4. AI response appears (left-aligned)
5. Scroll to bottom automatically

### AI Response Generation
- **Latency:** Aim for <2 seconds
- **Streaming:** Optional (type letter-by-letter)
- **Length:** 2-5 sentences typically
- **Tone:** Match Digital Mind's personality
- **Context:** Remember conversation history

### Voice Interaction (Optional)
- Click "Voice" button
- Microphone access request
- User speaks
- Transcribe to text (Speech-to-Text)
- Send to AI
- AI responds with voice (Text-to-Speech)
- Voice cloning matches real person

### Video Interaction (Optional)
- Click "Video" button
- Opens video player
- Animated avatar or video of AI
- Lip-sync with voice response
- Eye contact, gestures

---

## Guest vs Authenticated Users

### Guest (Not signed in)
- Can chat: Limited (e.g., 5 messages)
- After limit: Show modal "Sign up to continue"
- CTA: "Create free account"
- No chat history saved

### Authenticated
- Unlimited messages (within plan limits)
- Chat history saved
- Can save favorite responses
- Access to voice/video (if available)

---

## SEO Optimization

**Title:** "{Name} | AI Digital Mind on Delphi"
**Example:** "Dr. Mark Hyman | AI Health Expert on Delphi"

**Description:** "{Bio first sentence}. Chat with {Name}'s AI digital mind for personalized advice on {topics}."

**Canonical:** `https://www.delphi.ai/{username}`

**Structured Data:**
```json
{
  "@type": "Person",
  "name": "Dr. Mark Hyman",
  "jobTitle": "Functional Medicine Pioneer",
  "description": "Bio text...",
  "url": "https://www.delphi.ai/dr-mark-hyman",
  "sameAs": [
    "https://twitter.com/...",
    "https://linkedin.com/..."
  ]
}
```

**Open Graph:**
- og:title: {Name} - AI Digital Mind
- og:description: {Bio}
- og:image: {Profile photo}
- og:type: profile

**FAQ Schema:** For Q&A accordion section

---

## Accessibility

- Chat interface keyboard accessible (Tab, Enter)
- Screen reader announcements for new messages
- Alt text on profile photo
- ARIA live region for chat messages
- Focus management in modal (if used)
- Color contrast WCAG AA compliant

---

## Mobile Considerations

- Chat full-screen or prominent on mobile
- Large touch targets (48px min)
- Swipe to close modal (if applicable)
- Input auto-focus when chat opens
- Keyboard pushes chat up (avoid covering input)
- Voice/Video buttons accessible on mobile

---

## Performance

- Lazy load chat widget (on interaction)
- Lazy load images below fold
- WebSocket for real-time chat (optional)
- Optimistic UI (show message immediately)
- Cache AI responses for common questions
- Prefetch suggested questions

---

## Analytics

**Events to Track:**
- Page view: Profile page
- Interaction: Start conversation
- Message sent: User message count
- Suggested question clicked
- Voice/Video button clicked
- Sign up CTA clicked
- Bounce: No interaction
- Conversation length: Message count
- Rating: Thumbs up/down on responses (optional)

---

**End of Profile/Digital Mind Page Template**
