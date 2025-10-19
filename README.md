# A One Car - Premium Car Rental Website

A fully responsive, modern car rental website built with HTML, CSS, JavaScript, and Firebase. This website provides a complete car rental solution with booking system, admin dashboard, and customer management.

## 🚗 Features

### Frontend Features
- **Responsive Design**: Works perfectly on all devices (mobile, tablet, desktop)
- **Modern UI/UX**: Clean, professional design with smooth animations
- **Car Catalog**: Browse available cars with detailed information
- **Advanced Filtering**: Filter cars by type, seats, fuel, and price
- **Real-time Booking**: Instant booking system with Firebase integration
- **Contact Forms**: Multiple contact options with form validation
- **WhatsApp Integration**: Direct WhatsApp contact button
- **SEO Optimized**: Meta tags, structured data, and optimized content

### Backend Features
- **Firebase Integration**: Real-time database for cars, bookings, and inquiries
- **Admin Dashboard**: Complete admin panel for managing cars and bookings
- **Authentication**: Secure admin login with Google Sign-in
- **Image Upload**: Automatic image hosting via ImgBB API
- **Data Export**: CSV export functionality for bookings
- **Real-time Updates**: Live updates across all connected clients

## 📁 File Structure

```
carorent/
├── index.html          # Homepage
├── about.html          # About us page
├── cars.html           # Car catalog with filtering
├── contact.html        # Contact page with forms
├── pricing.html        # Pricing information
├── vehicles.html       # Alternative vehicle showcase
├── admin.html          # Admin dashboard
└── README.md           # This file
```

## 🛠️ Technologies Used

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Tailwind CSS, Custom CSS
- **Backend**: Firebase (Firestore, Authentication)
- **Image Hosting**: ImgBB API
- **Animations**: AOS (Animate On Scroll)
- **Icons**: SVG icons and emojis
- **Fonts**: Google Fonts (Inter)

## 🚀 Setup Instructions

### 1. Firebase Setup
1. Create a new Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable Firestore Database
3. Enable Authentication (Email/Password and Google)
4. Update Firebase config in all HTML files:
   ```javascript
   const firebaseConfig = {
     apiKey: "your-api-key",
     authDomain: "your-project.firebaseapp.com",
     projectId: "your-project-id",
     storageBucket: "your-project.appspot.com",
     messagingSenderId: "your-sender-id",
     appId: "your-app-id"
   };
   ```

### 2. Database Structure
Create these collections in Firestore:

#### Cars Collection (`cars`)
```javascript
{
  name: "Car Name",
  slug: "car-slug",
  type: "Sedan|SUV|Hatchback|Luxury",
  seats: 5,
  fuel: "Petrol|Diesel|Electric",
  transmission: "Automatic|Manual",
  pricePerDay: 1200,
  pricePerWeek: 7000,
  pricePerMonth: 25000,
  features: ["AC", "GPS", "Bluetooth"],
  imageUrl: "https://image-url.com/car.jpg",
  active: true,
  createdAt: timestamp
}
```

#### Bookings Collection (`bookings`)
```javascript
{
  carId: "car-document-id",
  userName: "Customer Name",
  userEmail: "customer@email.com",
  userPhone: "+91XXXXXXXXXX",
  pickupDateTime: timestamp,
  dropDateTime: timestamp,
  plan: "Daily|Weekly|Monthly",
  status: "pending|confirmed|completed|cancelled",
  createdAt: timestamp
}
```

#### Inquiries Collection (`inquiries`)
```javascript
{
  name: "Customer Name",
  email: "customer@email.com",
  phone: "+91XXXXXXXXXX",
  subject: "General Inquiry",
  message: "Customer message",
  createdAt: timestamp
}
```

### 3. Admin Setup
1. Add admin emails to the hardcoded admin list in `admin.html`:
   ```javascript
   const HARDCODED_ADMINS = ["admin@aonecar.com", "your-email@domain.com"];
   ```
2. Or create an `adminList` document in Firestore with an `admins` array field

### 4. Image Upload Setup
1. Get a free API key from [ImgBB](https://api.imgbb.com/)
2. Replace the API key in `admin.html`:
   ```javascript
   const IMGBB_API_KEY = "your-imgbb-api-key";
   ```

### 5. Contact Information
Update contact details throughout the website:
- Phone: +91 6263814758
- Email: contact@aonecar.com
- Address: Vijay Nagar, Indore, MP
- WhatsApp: https://wa.me/916263814758

## 📱 Pages Overview

### 1. Homepage (`index.html`)
- Hero section with call-to-action
- Featured cars from database
- Services overview
- Customer testimonials
- Pricing plans
- Contact information

### 2. About Page (`about.html`)
- Company story and mission
- Team information
- Service areas
- Company statistics
- Timeline of achievements

### 3. Cars Page (`cars.html`)
- Complete car catalog
- Advanced filtering system
- Search functionality
- Real-time booking modal
- Car specifications

### 4. Contact Page (`contact.html`)
- Contact form with Firebase integration
- Business hours
- Location map
- FAQ section
- Multiple contact methods

### 5. Pricing Page (`pricing.html`)
- Dynamic pricing table from database
- Comparison of daily/weekly/monthly rates
- Transparent pricing information

### 6. Admin Dashboard (`admin.html`)
- Secure authentication
- Car management (CRUD operations)
- Booking management
- Customer inquiries
- Analytics overview
- Data export functionality

## 🎨 Customization

### Colors
The website uses a gold and dark theme. Main colors:
- Primary Gold: #D4AF37
- Dark Background: #1a1a1a
- Card Background: rgba(45, 45, 45, 0.9)

### Fonts
- Primary Font: Inter (Google Fonts)
- Fallback: system fonts

### Animations
- AOS (Animate On Scroll) for entrance animations
- Custom CSS transitions for interactions
- Loading spinners and hover effects

## 📊 Features in Detail

### Booking System
- Real-time availability checking
- Customer information collection
- Date and time selection
- Plan selection (Daily/Weekly/Monthly)
- Status tracking (Pending/Confirmed/Completed/Cancelled)

### Admin Dashboard
- **Dashboard**: Overview statistics and recent activity
- **Cars**: Add, edit, delete, and manage car inventory
- **Bookings**: View and manage customer bookings
- **Inquiries**: Handle customer inquiries and messages
- **Analytics**: Basic reporting (expandable)

### SEO Features
- Meta tags for all pages
- Open Graph tags for social sharing
- Structured data (JSON-LD)
- Semantic HTML structure
- Optimized images and loading

## 🔧 Maintenance

### Regular Tasks
1. **Update Car Inventory**: Add new cars, update prices, manage availability
2. **Process Bookings**: Confirm bookings, update statuses
3. **Respond to Inquiries**: Handle customer questions and requests
4. **Monitor Analytics**: Track website performance and user behavior
5. **Backup Data**: Regular Firebase data exports

### Security
- Firebase security rules should be configured
- Admin access is restricted to authorized emails
- Input validation on all forms
- HTTPS enforcement recommended

## 📞 Support

For technical support or customization requests:
- **Developer**: Rao Developers
- **Website**: https://raodevlopers.xyz
- **Contact**: Available through the website

## 📄 License

This project is proprietary software developed for A One Car. All rights reserved.

---

**A One Car** - Your trusted partner for premium car rentals in Indore, Madhya Pradesh.