# 🍽️ Restaurant Menu Chatbot 🤖  
This is a **Streamlit-based AI-powered Restaurant Menu Chatbot** that allows users to:

- Upload restaurant menus in CSV format and query dish availability using Google Gemini AI.  
- Get recommendations for dishes, check preparation times, and order food.  
- Place orders and save them in an SQLite database.  

---

## ✅ Features  
✅ Upload restaurant menu in CSV format  
✅ AI-powered chatbot to answer menu-related queries  
✅ Place and confirm orders  
✅ Check dish availability and get preparation time  
✅ Store order details in a database (`restaurant_orders.db`)  

---

## 🚀 Getting Started  

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/restaurant-menu-chatbot.git
cd restaurant-menu-chatbot

2️⃣ Set Up a Virtual Environment
# On macOS/Linux
python3 -m venv venv
source venv/bin/activate

# On Windows
python -m venv venv
venv\Scripts\activate

3️⃣ Install Dependencies
pip install -r requirements.txt

🔑 Google Gemini API Key Setup
This chatbot uses Google Gemini AI to process menu-related queries. You need to configure an API key.

How to Get a Gemini API Key:
1)Go to Google AI Studio
2)Sign in with your Google account
3)Generate an API key from the API Keys section
4)Copy the API key

Add API Key to the Project:
1)Open the app.py file

2)Replace the api_key value in this line:
genai.configure(api_key="YOUR_GEMINI_API_KEY_HERE")

3)Save the file

🏃‍♂️ Running the Application
After setting up everything, run the application using Streamlit:
streamlit run app.py
This will open the web app in your browser.

📂 File Upload Instructions
CSV File Format Example
The uploaded CSV file should contain the following columns:

dish_name
price
category
cuisine
preparation_time
availability 
ratings

🍲 Placing an Order
Go to the Place Order section.
Select dishes from the multi-select dropdown.
Confirm your order after verifying availability.
Order details are automatically saved to the SQLite database (restaurant_orders.db).

📚 Viewing Order Details in Database
To view saved orders:
sqlite3 restaurant_orders.db

Then run:
SELECT * FROM orders;

📝 Generating Order Confirmation
After confirming the order, the chatbot will generate an order summary.
Optionally, download the confirmation receipt in a PDF format.

📜 License
This project is licensed under the MIT License.
