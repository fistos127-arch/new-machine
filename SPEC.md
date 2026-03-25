# Shopzz - E-Commerce Store Specification

## 1. Project Overview
- **Project name**: Shopzz
- **Type**: Single-page e-commerce website
- **Core functionality**: A modern online store with product browsing, filtering, cart management, and checkout flow
- **Target users**: Online shoppers looking for a premium shopping experience

## 2. UI/UX Specification

### Layout Structure
- **Header**: Fixed top navigation (60px height)
- **Hero Section**: Full-width promotional banner (500px height)
- **Category Filter**: Horizontal pill buttons
- **Product Grid**: 4 columns desktop, 2 tablet, 1 mobile
- **Footer**: Multi-column links with newsletter signup

### Responsive Breakpoints
- Mobile: < 640px
- Tablet: 640px - 1024px
- Desktop: > 1024px

### Visual Design

#### Color Palette
- **Background**: #0D0D0D (rich black)
- **Surface**: #1A1A1A (card backgrounds)
- **Surface Elevated**: #242424 (hover states)
- **Primary Accent**: #FF6B35 (vibrant coral-orange)
- **Primary Hover**: #FF8555
- **Text Primary**: #FFFFFF
- **Text Secondary**: #A3A3A3
- **Text Muted**: #666666
- **Border**: #2A2A2A
- **Success**: #22C55E
- **Cart Badge**: #FF6B35

#### Typography
- **Font Family**: "Syne" (headings), "DM Sans" (body)
- **Logo**: 28px, Syne, 800 weight
- **H1**: 48px, Syne, 700 weight
- **H2**: 32px, Syne, 600 weight
- **H3**: 20px, Syne, 600 weight
- **Body**: 15px, DM Sans, 400 weight
- **Small**: 13px, DM Sans, 400 weight
- **Price**: 18px, Syne, 700 weight

#### Spacing System
- **Container max-width**: 1280px
- **Container padding**: 24px (desktop), 16px (mobile)
- **Grid gap**: 24px
- **Card padding**: 0 (image flush), 16px (content area)
- **Section spacing**: 64px vertical

#### Visual Effects
- **Card hover**: translateY(-8px), box-shadow 0 20px 40px rgba(255,107,53,0.15)
- **Button hover**: scale(1.02), background lighten
- **Image hover**: scale(1.05) with overflow hidden
- **Page load**: Staggered fade-in with slide-up (animation-delay increments of 0.1s)
- **Cart slide**: translateX(100%) to 0, 0.3s ease-out

### Components

#### Header
- Logo (left): "shopzz" text with accent color on "zz"
- Navigation (center): Home, Shop, New Arrivals, Sale
- Actions (right): Search icon, User icon, Cart icon with badge count
- Cart badge shows number of items, pulses on add

#### Hero Section
- Large headline: "Discover Your Style"
- Subheadline: "Curated collection of premium products"
- CTA Button: "Shop Now" - coral accent with dark text
- Background: Subtle gradient overlay on abstract pattern
- Floating product images with parallax-lite effect

#### Category Filters
- Horizontal scrollable on mobile
- Pills: All, Electronics, Clothing, Accessories, Home
- Active state: Filled coral background
- Inactive: Border only, transparent background

#### Product Card
- Aspect ratio: 4:5 for images
- Image with hover zoom effect
- Quick view overlay on hover (optional)
- Product name (truncate at 2 lines)
- Price with original/sale price display
- "Add to Cart" button appears on hover
- Wishlist heart icon (top-right corner)

#### Shopping Cart (Sidebar)
- Slides in from right
- Dark overlay on rest of page
- Cart items with thumbnail, name, quantity controls, price
- Remove item button
- Subtotal display
- "Checkout" button (full-width, coral)
- Empty cart state with illustration

#### Footer
- 4 columns: About, Shop, Support, Newsletter
- Social media icons
- Payment method icons
- Copyright text

## 3. Functionality Specification

### Core Features
1. **Product Display**: 12 sample products with images, names, prices
2. **Category Filtering**: Filter products by category
3. **Add to Cart**: Click to add items, increment quantity if exists
4. **Cart Management**: View cart, adjust quantities, remove items
5. **Cart Badge**: Real-time update of cart item count
6. **Responsive Design**: Works on all device sizes
7. **Animations**: Smooth transitions and micro-interactions

### User Interactions
- Click category pill → Filter products (with fade animation)
- Click "Add to Cart" → Add item, animate cart badge, show toast notification
- Click cart icon → Open cart sidebar
- Click outside cart or X → Close cart sidebar
- Click +/- in cart → Adjust quantity
- Click trash icon → Remove item from cart
- Hover product → Show add to cart button, zoom image

### Data Handling
- Products stored in JavaScript array
- Cart state managed in memory
- No backend required

### Edge Cases
- Empty cart shows appropriate message
- Quantity cannot go below 1 (removes item instead)
- Long product names truncated with ellipsis

## 4. Acceptance Criteria
- [ ] Header is fixed and contains logo, nav, search, user, cart icons
- [ ] Cart badge shows correct count and animates on add
- [ ] Hero section displays with headline and CTA button
- [ ] Category filters work and filter products correctly
- [ ] Product grid displays 12 products with images, names, prices
- [ ] Product cards have hover effects (zoom, show add button)
- [ ] Cart sidebar opens/closes smoothly
- [ ] Cart shows correct items, quantities, prices
- [ ] Can add, remove, and adjust quantities in cart
- [ ] Responsive layout works on mobile/tablet/desktop
- [ ] Page load animations play correctly
- [ ] All hover states and transitions are smooth
