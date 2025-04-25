# Artistic Scrappy

A modern web application built with Python and Django that facilitates buying and selling of pre-owned items, promoting sustainability through reuse.

## 🌟 Features

- **User Authentication**: Secure register, login, and profile management system
- **Product Marketplace**: 
  - List items for sale with detailed descriptions and multiple images
  - Browse available items by categories and filters
  - Advanced search functionality
- **Shopping Experience**:
  - Intuitive shopping cart
  - Streamlined checkout process
  - Secure payment integration via Paytm
- **Order Management**: Track orders from placement to delivery
- **Communication**: Built-in messaging system to contact sellers
- **Blog Platform**: Community content about sustainability, recycling tips, and reuse ideas

## 🛠️ Tech Stack

- **Backend**: Python 3.x, Django 4.x
- **Database**: SQLite (development), PostgreSQL/MySQL (production-ready)
- **Frontend**: HTML5, CSS3, JavaScript
- **Payment Processing**: Paytm Gateway
- **Image Processing**: Pillow

## 🚀 Getting Started

### Prerequisites
- Python 3.x
- pip (Python package manager)
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/schivam18/artistic-scrappy
   cd artistic-scrappy
   ```

2. **Set up a virtual environment**
   ```bash
   python -m venv env
   
   # On Windows
   env\Scripts\activate
   
   # On macOS/Linux
   source env/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Apply database migrations**
   ```bash
   python manage.py migrate
   ```

5. **Create an admin user**
   ```bash
   python manage.py createsuperuser
   ```

6. **Configure Paytm payment gateway**
   - Register for a [Paytm Business account](https://business.paytm.com/)
   - Obtain your Merchant ID and Merchant Key
   - Update the configuration in `shop/views.py`:
     ```python
     MERCHANT_KEY = 'YOUR_MERCHANT_KEY_HERE'
     
     # In the checkout function:
     'MID': 'YOUR_MERCHANT_ID',
     ```

7. **Start the development server**
   ```bash
   python manage.py runserver
   ```

8. **Access the application**
   - Website: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
   - Admin panel: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)

## 📝 Usage Guide

### For Sellers
1. Register an account and complete your profile
2. Click on "Sell Item" in the navigation menu
3. Fill in the product details, upload images, and set your price
4. Manage your listings from your seller dashboard

### For Buyers
1. Browse products by category or use the search function
2. Add desired items to your cart
3. Proceed to checkout and select your payment method
4. Track your order status using the provided order ID

### For Administrators
Access the admin panel to:
- Manage user accounts
- Review and approve product listings
- Handle order processing
- Moderate blog content

## 📁 Project Structure

```
artistic-scrappy/
├── blog/                # Blog functionality
├── home/                # Landing page and site navigation
├── media/               # User-uploaded content
├── Paytm/               # Payment gateway integration
├── shop/                # Core marketplace functionality
├── static/              # Static assets (CSS, JS, images)
├── staticfiles/         # Collected static files
├── manage.py            # Django management script
├── requirements.txt     # Project dependencies
└── README.md            # This documentation
```

## 🤝 Contributing

We welcome contributions to improve Artistic Scrappy! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please ensure your code follows the project's style guidelines and includes appropriate tests.

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Django community for the robust framework
- All contributors who have invested time in improving this project
- Users who provide valuable feedback

---
