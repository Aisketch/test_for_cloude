# TEMPLATE 4.1: NAVIGATION & HEADER COMPONENTS

## 📋 PURPOSE
This template defines reusable navigation and header components including main navigation, mobile menus, sticky headers, breadcrumbs, and mega menus for consistent site-wide navigation.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Create Navigation & Header Components based on the following specification:

## COMPONENT LIBRARY OVERVIEW

Component Set: Navigation & Header
Design System: [Reference to Template 1.2]
Framework: React + TypeScript
Styling: Tailwind CSS with semantic tokens

Components to Create:
1. Main Navigation (Desktop)
2. Mobile Navigation
3. Sticky Header
4. Mega Menu (if applicable)
5. Breadcrumbs
6. User Menu/Profile Dropdown
7. Language Switcher
8. Search Header (if applicable)

---

## COMPONENT 4.1.1: MAIN NAVIGATION (Desktop)

### Component Props

```typescript
interface MainNavigationProps {
  logo: {
    src: string;
    alt: string;
    width: number;
    height: number;
    href: string;
  };
  navItems: NavItem[];
  rightItems?: ReactNode;
  transparent?: boolean;
  sticky?: boolean;
  currentPath?: string;
}

interface NavItem {
  label: string;
  href: string;
  submenu?: SubMenuItem[];
  megaMenu?: MegaMenuConfig;
  badge?: string;
  icon?: string;
}
```

### Visual Design

Layout Type: [Horizontal / Split / Centered]
Background: _______________
Background (Scrolled): _______________ (if different)
Border: [Bottom border / None / Shadow]

Height:
- Desktop: _______________ (e.g., 72px)
- Tablet: _______________

Logo Configuration:
- Position: [Left / Center]
- Size: _______________ (e.g., h-8 or h-10)
- Click Action: [Navigate to home]
- Hover Effect: [None / Opacity / Scale]

Navigation Items Layout:
- Position: [Center / Right of logo / Split]
- Spacing: _______________ (e.g., gap-8)
- Alignment: [Center / Top / Bottom]

### Navigation Item Styling

Text Style:
- Font Size: _______________
- Font Weight: _______________
- Color (Default): _______________ (semantic token)
- Color (Hover): _______________
- Color (Active): _______________

Active Indicator:
- Type: [Underline / Background / Border / Bold / Color only]
- Style: _______________
- Transition: _______________

Hover Effect:
- Type: [Color change / Underline / Background / Scale]
- Transition Duration: _______________ (e.g., 200ms)
- Easing: _______________

Dropdown Indicator:
- Show: [Yes/No]
- Icon: _______________ (e.g., ChevronDown)
- Size: _______________
- Animation: [Rotate on open / None]

### Right Side Items

Components to Include:
- [ ] Language Switcher
      Position: _______________
      Style: _______________

- [ ] Search Icon/Button
      Icon: _______________
      Action: [Open search modal / Navigate to search]

- [ ] Dark Mode Toggle
      Style: _______________
      Position: _______________

- [ ] Login Button
      Text: _______________
      Style: [Ghost / Outline / Text link]
      Size: _______________

- [ ] Sign Up Button (CTA)
      Text: _______________
      Style: [Primary button]
      Size: _______________
      Icon: _______________ (optional)

- [ ] User Avatar (Logged In)
      Size: _______________
      Click Action: [Open dropdown menu]

Spacing Between Items: _______________

### Dropdown Submenu Behavior

Trigger: [Hover / Click / Both]
Open Delay: _______________ (if hover)
Close Delay: _______________ (if hover)

Dropdown Styling:
- Background: _______________
- Border: _______________
- Shadow: _______________
- Border Radius: _______________
- Padding: _______________
- Min Width: _______________

Dropdown Items:
- Font Size: _______________
- Padding: _______________
- Hover Background: _______________
- Icon: [Show/Hide]
- Icon Position: [Left/Right]
- Icon Size: _______________

Dividers: [Yes/No]
Divider Style: _______________

### States & Interactions

Loading State: [Skeleton / Shimmer / None]
Error State: [Show notification / Log only]
Disabled State: _______________

Keyboard Navigation:
- Tab Order: [Left to right]
- Arrow Keys: [Navigate submenu]
- Escape Key: [Close submenu]
- Enter/Space: [Activate link]

Focus Indicators:
- Style: _______________
- Color: _______________
- Offset: _______________

### Responsive Breakpoint

Show Desktop Nav: [lg: and above / md: and above]
Hide Mobile Nav: [Same breakpoint]

---

## COMPONENT 4.1.2: MOBILE NAVIGATION

### Component Props

```typescript
interface MobileNavigationProps {
  logo: LogoConfig;
  navItems: NavItem[];
  isOpen: boolean;
  onToggle: () => void;
  rightItems?: ReactNode;
}
```

### Mobile Header Layout

Mobile Header Height: _______________ (e.g., 64px)
Mobile Header Background: _______________
Border: _______________

Logo Size (Mobile): _______________

Hamburger Button:
- Position: [Left / Right]
- Icon: [Menu / Custom]
- Size: _______________ (e.g., 24px)
- Color: _______________
- Active State: [X icon / Animated transform]
- Animation: [Rotate / Morph / Fade]

Right Side Items (Mobile):
[Same as desktop right items, adjust size]

### Mobile Menu Panel

Panel Type: [Slide-out / Full screen / Overlay]
Slide Direction: [Right to left / Left to right / Top to bottom]

Panel Styling:
- Background: _______________
- Width: [Full screen / 80% / 320px / 400px]
- Height: [Full screen / Auto]
- Padding: _______________

Overlay:
- Show: [Yes/No]
- Color: _______________
- Opacity: _______________
- Close on Click: [Yes/No]

Animation:
- Type: [Slide / Fade / Scale]
- Duration: _______________ (e.g., 300ms)
- Easing: _______________

### Mobile Menu Content

Menu Header:
- Show Logo: [Yes/No]
- Show Close Button: [Yes/No]
- Close Button Position: [Top right / Top left]
- Height: _______________

Navigation Items Layout:
- Layout: [Vertical list / Stacked]
- Spacing: _______________
- Alignment: [Left / Center]

Menu Item Styling:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Padding: _______________
- Border: [Between items / None]
- Hover Background: _______________

Submenu Behavior:
- Type: [Accordion / Nested panel / Modal]
- Indicator: [Plus/Minus / Chevron / Arrow]
- Animation: [Expand / Slide]
- Nested Items Styling: _______________

Menu Footer:
- Show: [Yes/No]
- Content: [CTA buttons / User info / Social links / Contact]
- Styling: _______________

CTA Buttons (Mobile Menu):
- Login Button: _______________
- Sign Up Button: _______________
- Layout: [Stacked / Horizontal]

### Body Scroll Lock

Lock Scroll When Open: [Yes/No]
Scroll Lock Method: [overflow: hidden / fixed positioning]

### Mobile Menu States

Open State: _______________
Closed State: _______________
Transition State: _______________

---

## COMPONENT 4.1.3: STICKY HEADER

### Sticky Behavior

Sticky: [Yes/No]
Sticky Threshold: _______________ px (scroll distance before sticky)

Sticky Styling Changes:
- Background: _______________ (may add opacity or blur)
- Shadow: _______________ (add shadow when sticky)
- Height: _______________ (may reduce height)
- Logo Size: _______________ (may reduce)
- Padding: _______________ (may reduce)

Scroll Direction Detection:
- Hide on Scroll Down: [Yes/No]
- Show on Scroll Up: [Yes/No]
- Threshold: _______________ px

Animation:
- Transition: _______________ (e.g., "all 200ms ease-in-out")
- Transform: _______________ (e.g., translateY)

### Sticky States

```typescript
interface StickyState {
  isSticky: boolean;
  isHidden: boolean;
  scrollDirection: 'up' | 'down' | null;
  scrollY: number;
}
```

---

## COMPONENT 4.1.4: MEGA MENU (If Applicable)

### When to Use

Use Mega Menu For: _______________ (e.g., "Products", "Solutions", "Resources")

### Component Props

```typescript
interface MegaMenuProps {
  title: string;
  columns: MegaMenuColumn[];
  featured?: FeaturedContent;
  cta?: CTAConfig;
}

interface MegaMenuColumn {
  title: string;
  items: MenuItemConfig[];
  icon?: string;
}
```

### Visual Design

Layout: [2 columns / 3 columns / 4 columns / Featured + columns]
Width: [Full width / Container width / Custom width]

Styling:
- Background: _______________
- Border: _______________
- Shadow: _______________
- Border Radius: _______________
- Padding: _______________

Column Configuration:

Column 1:
- Width: _______________
- Title: _______________
- Items Count: _______________

Column 2:
- Width: _______________
- Title: _______________
- Items Count: _______________

Column 3:
- Width: _______________
- Title: _______________
- Items Count: _______________

Column 4 (Optional):
- Width: _______________
- Title: _______________
- Items Count: _______________

### Column Styling

Column Title:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Margin Bottom: _______________

Menu Items:
- Font Size: _______________
- Color: _______________
- Padding: _______________
- Hover Background: _______________
- Icon: [Show/Hide]
- Icon Size: _______________
- Description: [Show/Hide]
- Description Style: _______________

### Featured Content Area

Include Featured: [Yes/No]

If Yes:
- Position: [Left / Right / Top]
- Width: _______________
- Content Type: [Product highlight / Banner / Video / Image]
- Background: _______________
- Padding: _______________

Featured Content:
- Headline: _______________
- Description: _______________
- Image: _______________
- CTA: _______________

### Mega Menu Behavior

Open Trigger: [Hover / Click]
Close Trigger: [Mouse leave / Click outside / Explicit close]
Hover Delay: _______________ ms
Animation: [Fade in / Slide down / Scale]
Duration: _______________ ms

---

## COMPONENT 4.1.5: BREADCRUMBS

### Component Props

```typescript
interface BreadcrumbsProps {
  items: BreadcrumbItem[];
  separator?: string;
  maxItems?: number;
  showHome?: boolean;
}

interface BreadcrumbItem {
  label: string;
  href: string;
  current?: boolean;
}
```

### Visual Design

Position: [Below header / Top of content / In page]
Background: _______________
Padding: _______________

Item Styling:
- Font Size: _______________
- Color: _______________
- Color (Current): _______________
- Hover Color: _______________
- Font Weight: _______________

Separator:
- Type: [/ / > / Chevron / Custom]
- Color: _______________
- Size: _______________
- Spacing: _______________

Home Icon:
- Show: [Yes/No]
- Icon: _______________ (e.g., Home from lucide-react)
- Size: _______________

Truncation:
- Max Items: _______________ (before ellipsis)
- Ellipsis Position: [Middle / Start]
- Ellipsis Text: "..."

### Responsive Behavior

Mobile: [Show all / Show current only / Hide]
Mobile Layout: [Horizontal scroll / Vertical / Truncated]

---

## COMPONENT 4.1.6: USER MENU / PROFILE DROPDOWN

### Component Props

```typescript
interface UserMenuProps {
  user: {
    name: string;
    email: string;
    avatar?: string;
    role?: string;
  };
  menuItems: UserMenuItem[];
  onLogout: () => void;
}

interface UserMenuItem {
  label: string;
  href?: string;
  onClick?: () => void;
  icon?: string;
  divider?: boolean;
}
```

### Trigger Button

Avatar:
- Size: _______________ (e.g., h-10 w-10)
- Border: _______________
- Fallback: [Initials / Icon / Default image]

Dropdown Indicator: [Show/Hide]
Hover Effect: _______________

### Dropdown Menu

Position: [Right-aligned / Left-aligned]
Width: _______________
Offset: _______________

Styling:
- Background: _______________
- Border: _______________
- Shadow: _______________
- Border Radius: _______________
- Padding: _______________

### Menu Header

Show User Info: [Yes/No]

If Yes:
- Avatar: [Show/Hide]
- Name: [Show/Hide]
- Email: [Show/Hide]
- Role/Plan: [Show/Hide]
- Styling: _______________

Divider After Header: [Yes/No]

### Menu Items

Common Items:
- [ ] Dashboard
- [ ] Profile/Account Settings
- [ ] Billing
- [ ] Team Settings
- [ ] Support/Help
- [ ] Documentation
- [ ] Preferences
- [ ] Logout

Item Styling:
- Font Size: _______________
- Padding: _______________
- Hover Background: _______________
- Icon Position: [Left / Right]
- Icon Size: _______________

Dividers: [Between groups]

Logout Item:
- Position: [Bottom]
- Styling: _______________ (may use destructive color)

---

## COMPONENT 4.1.7: LANGUAGE SWITCHER

### Component Props

```typescript
interface LanguageSwitcherProps {
  languages: Language[];
  currentLanguage: string;
  onChange: (lang: string) => void;
  variant?: 'dropdown' | 'flags' | 'minimal';
}

interface Language {
  code: string;
  name: string;
  flag?: string;
}
```

### Display Options

Type: [Dropdown / Flags / Text only / Icons + text]

Languages Offered:
Language 1:
- Code: _______________ (e.g., "en")
- Name: _______________
- Flag: _______________ (emoji or icon)

Language 2:
- Code: _______________
- Name: _______________
- Flag: _______________

Language 3:
- Code: _______________
- Name: _______________
- Flag: _______________

[Continue for all languages...]

### Visual Design

Button/Trigger:
- Display: [Flag + Code / Flag only / Code only / Name]
- Size: _______________
- Hover Effect: _______________

Dropdown Menu:
- Position: [Center-aligned / Right-aligned / Left-aligned]
- Width: _______________
- Max Height: _______________ (with scroll if needed)

Menu Items:
- Display: [Flag + Name / Name only]
- Selected State: [Checkmark / Background / Bold]
- Hover State: _______________

### Behavior

Storage: [localStorage / Cookie / URL parameter]
Page Reload: [Yes/No]
Redirect: [Yes/No]
URL Pattern: _______________ (e.g., /en/page, /uk/page)

---

## COMPONENT 4.1.8: SEARCH HEADER (If Applicable)

### Component Props

```typescript
interface SearchHeaderProps {
  onSearch: (query: string) => void;
  placeholder?: string;
  suggestions?: SearchSuggestion[];
  variant?: 'icon' | 'bar' | 'modal';
}
```

### Search Display Type

Type: [Icon button / Search bar / Command palette]

If Icon Button:
- Position: _______________
- Icon: [Search / MagnifyingGlass]
- Click Action: [Open modal / Expand inline]

If Search Bar:
- Width: _______________
- Position: _______________
- Always Visible: [Yes/No]

If Modal:
- Trigger: [Icon button / Keyboard shortcut]
- Keyboard Shortcut: _______________ (e.g., Cmd+K, Ctrl+K)

### Search Input Styling

Input Field:
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Padding: _______________
- Font Size: _______________
- Placeholder Color: _______________

Icon:
- Position: [Left / Right]
- Size: _______________
- Color: _______________

Clear Button:
- Show When: [Text entered]
- Icon: _______________

### Search Results/Suggestions

Show Suggestions: [Yes/No]

Dropdown Styling:
- Position: [Below input]
- Background: _______________
- Shadow: _______________
- Max Height: _______________
- Padding: _______________

Result Item:
- Styling: _______________
- Hover State: _______________
- Icon: [Show/Hide]
- Highlight Matching Text: [Yes/No]

Categories:
- Show: [Yes/No]
- Categories: [Pages / Blog / Products / Help / Other]

Empty State:
- Message: _______________
- Icon: _______________

---

## SHARED SPECIFICATIONS

### Accessibility Requirements

All Components Must Include:
- [ ] Semantic HTML (nav, button, ul/li)
- [ ] ARIA labels and roles
- [ ] Keyboard navigation support
- [ ] Focus indicators visible
- [ ] Screen reader announcements
- [ ] Skip to main content link
- [ ] Focus trap in mobile menu
- [ ] ESC key closes menus
- [ ] ARIA expanded states
- [ ] Color contrast WCAG AA

### Animation Configuration

Transitions:
- Duration: _______________ (recommend 200ms)
- Easing: _______________ (recommend ease-in-out)
- Properties: [transform, opacity]

Reduced Motion:
- Respect prefers-reduced-motion
- Alternative: [Instant / Shorter duration]

### Z-Index Hierarchy

Navigation Z-Index: 1000
Dropdown Menus: 1001
Mobile Menu Overlay: 999
Mobile Menu Panel: 1000
Search Modal: 1100

### Performance Optimization

- [ ] Lazy load heavy components
- [ ] Optimize images (logo, avatars)
- [ ] Debounce search input
- [ ] Virtual scrolling (large menus)
- [ ] Code splitting
- [ ] Minimize re-renders

### Testing Requirements

Test Cases:
- [ ] All links work correctly
- [ ] Mobile menu opens/closes
- [ ] Dropdowns trigger on hover/click
- [ ] Active states display correctly
- [ ] Keyboard navigation works
- [ ] Screen reader announces properly
- [ ] Language switcher changes language
- [ ] Search returns results
- [ ] Responsive at all breakpoints
- [ ] Works on touch devices
- [ ] No layout shift on load

### State Management

```typescript
interface NavigationState {
  isMobileMenuOpen: boolean;
  activeDropdown: string | null;
  isSearchOpen: boolean;
  isSticky: boolean;
  currentLanguage: string;
  user: User | null;
}
```

---

## IMPLEMENTATION NOTES

Routing:
- Integration: [React Router / Next.js / Other]
- Link Component: _______________
- Active Link Detection: _______________

Authentication:
- Check User State: _______________
- Conditional Rendering: [Show/Hide items based on auth]
- Protected Routes: _______________

Analytics:
- Track: [Navigation clicks, menu opens, search queries]
- Event Names: _______________

Multi-language:
- Translation Keys: _______________
- RTL Support: [Yes/No]
- Language-specific Navigation: [Yes/No]

---

## USAGE EXAMPLES

Example Usage:
```tsx
<MainNavigation
  logo={{
    src: "/logo.svg",
    alt: "Company Name",
    width: 120,
    height: 32,
    href: "/"
  }}
  navItems={navigationItems}
  transparent={false}
  sticky={true}
  currentPath={pathname}
/>
```

---

## NOTES & SPECIAL REQUIREMENTS
_______________________________________________
_______________________________________________
_______________________________________________
```

---

## ✅ IMPLEMENTATION PROMPT FOR LOVABLE

After filling this template:

```
Create Navigation & Header Components based on the completed specification.

CONTEXT: I have defined a comprehensive navigation system with desktop nav, mobile menu, sticky header, mega menus, breadcrumbs, user menu, language switcher, and search components.

TASK:
1. Create MainNavigation component with logo and nav items
2. Build MobileNavigation with hamburger menu and slide-out panel
3. Implement StickyHeader with scroll detection
4. Create MegaMenu component (if specified)
5. Build Breadcrumbs component
6. Implement UserMenu dropdown
7. Create LanguageSwitcher component
8. Add SearchHeader component (if specified)
9. Set up proper TypeScript interfaces
10. Ensure full accessibility and keyboard navigation

GUIDELINES:
- Use React + TypeScript
- Style with Tailwind CSS semantic tokens
- Mobile-first responsive design
- Smooth animations and transitions
- Full keyboard navigation support
- ARIA labels and semantic HTML
- Focus management for modals/dropdowns
- Touch-friendly on mobile (44px min targets)

CONSTRAINTS:
- Must work with routing system
- Performance optimized (no jank)
- Accessibility WCAG 2.1 AA compliant
- Support all specified languages
- Z-index hierarchy respected
- No layout shift
- Works on all modern browsers

[Paste your filled navigation template here]

EXPECTED DELIVERABLES:
1. MainNavigation component (desktop)
2. MobileNavigation component
3. StickyHeader behavior
4. MegaMenu component (if applicable)
5. Breadcrumbs component
6. UserMenu dropdown
7. LanguageSwitcher component
8. SearchHeader component (if applicable)
9. Proper TypeScript types
10. Accessibility features implemented
```

---

## 📝 USAGE INSTRUCTIONS

1. **Start with mobile** - design mobile menu first, scale up
2. **Keep it simple** - max 5-7 main nav items
3. **Active states** - users need to know where they are
4. **Touch targets** - minimum 44x44px on mobile
5. **Keyboard nav** - Tab, Arrow keys, Enter, Escape
6. **Sticky header** - improves navigation but consider UX
7. **Test thoroughly** - navigation is critical infrastructure
8. **Performance** - navigation loads on every page

---

## 💡 BEST PRACTICES

- Logo should always link to homepage
- Active page indication should be obvious
- Mobile menu should close when link clicked
- Mega menus for 8+ submenu items
- Sticky header shouldn't be too tall (reduces content area)
- Hide sticky header on scroll down, show on scroll up
- Language switcher should be accessible but not prominent
- Search should be easily discoverable
- User menu should group related items logically
- Breadcrumbs improve UX and SEO
- Keep dropdown menus shallow (max 2 levels)
- Use icons sparingly in navigation
- Ensure touch targets are large enough on mobile

---

## ⚠️ CRITICAL REMINDERS

- Navigation appears on every page - must be perfect
- Mobile menu is critical - most traffic is mobile
- Accessibility is non-negotiable for navigation
- Active link indication improves orientation
- Keyboard navigation must work flawlessly
- Focus trap in mobile menu prevents scroll issues
- Z-index conflicts break layering
- Navigation performance impacts every page
- Test on real devices, not just dev tools
- Sticky header can be annoying if poorly implemented
- Mega menus work great for content-heavy sites
- Simple dropdowns better for small menus
- Logo size affects header height
- Header height affects page layout
