# Gemstone Platform

A modern, mobile-friendly online platform for viewing, purchasing, and managing premium gemstones.

## Features
- Browse gemstones with filters, search, and image sliders
- Add to cart and place orders (no login required for customers)
- Admin dashboard for managing gemstones (add, edit, delete, upload images)
- Supabase backend for data and image storage
- Responsive, elegant UI with modern animations

## Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Configure Supabase
- Create a project at [supabase.com](https://supabase.com/)
- In your project, create the following tables:
  - `gems` (id, name, type, description, price, weight, color, availability, featured)
  - `gem_images` (id, gem_id, image_url, order)
  - `orders` (id, gem_ids, name, email, address, total_price, created_at)
- Enable Supabase Auth (email/password) for admin login
- Create a storage bucket for gem images
- Get your Supabase URL and anon key
- Create a `.env` file in the root:
  ```env
  VITE_SUPABASE_URL=your_supabase_url
  VITE_SUPABASE_ANON_KEY=your_anon_key
  ```

### 3. Run the App
```bash
npm run dev
```

### 4. Admin Usage
- Go to `/admin/login` and log in with your Supabase admin credentials
- Use the dashboard to add, edit, or delete gemstones
- Upload images for each gemstone (3+ images recommended)
- Set price, weight, type, color, and availability
- Featured gems will appear on the home page

### 5. Deployment
- Deploy the frontend to Vercel, Netlify, or any static host
- Supabase remains fully online (no local servers needed)

---

## Customization
- Update theme colors in `tailwind.config.js`
- Add more gem types or fields as needed

## License
MIT 