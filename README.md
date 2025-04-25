# Artistic Scrappy

A web application built with Python and Django that allows users to buy and sell used items.

## Features

- **User Authentication**: Register, login, and manage user profiles
- **Product Listing**: Users can list their used items for sale with details and images
- **Product Browsing**: Browse available items by categories
- **Search Functionality**: Search for specific items
- **Shopping Cart**: Add items to cart and proceed to checkout
- **Order Tracking**: Track the status of placed orders
- **Payment Integration**: Integration with payment gateway (Paytm)
- **Contact System**: Contact sellers or administrators
- **Blog Section**: Read and post updates related to recycling and reuse

## Tech Stack

- **Backend**: Python, Django
- **Database**: SQLite (default), can be configured for PostgreSQL or MySQL
- **Frontend**: HTML, CSS, JavaScript
- **Payment Gateway**: Paytm (integration available)

## Setup Instructions

### Prerequisites
- Python 3.x
- pip (Python package manager)

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/artistic-scrappy.git
cd artistic-scrappy
```

2. Create a virtual environment
```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

The requirements.txt file includes:
- Django>=4.0.1,<5.0.0
- Pillow>=9.0.0 (for image handling)
- pycryptodome>=3.10.1 (for Paytm payment integration)
- requests>=2.27.1 (for API requests)

4. Apply migrations
```bash
python manage.py migrate
```

5. Create a superuser
```bash
python manage.py createsuperuser
```

6. Configure Paytm (for payment functionality)
   - Sign up for a Paytm Business account at [https://business.paytm.com/](https://business.paytm.com/)
   - Get your Merchant ID and Merchant Key
   - Update the following settings in `shop/views.py`:
     ```python
     MERCHANT_KEY = 'YOUR_MERCHANT_KEY_HERE'
     ```
   - In the checkout function, update your MID:
     ```python
     'MID': 'YOUR_MERCHANT_ID',
     ```

7. Run the development server
```bash
python manage.py runserver
```

8. Access the application at http://127.0.0.1:8000/

## Usage

1. **Admin Access**: Navigate to http://127.0.0.1:8000/admin to manage products, users, and orders
2. **Selling Items**: Register, login, and use the "Sell Item" option to list products
3. **Buying Items**: Browse products, add to cart, and proceed to checkout
4. **Order Tracking**: Use your order ID and email to track your order status

## Project Structure

- **shop/**: Main app handling product listings and orders
- **blog/**: App for blog functionality
- **home/**: App for landing page and general site navigation
- **Paytm/**: Payment gateway integration
- **media/**: Stores uploaded images and files
- **Scrappy/**: Core project settings

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Django community for the excellent framework
- All contributors who have helped improve this project
