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

### 2️⃣ Set Up a Virtual Environment
```bash
# On macOS/Linux
python3 -m venv venv
source venv/bin/activate

# On Windows
python -m venv venv
venv\Scripts\activate

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt

🔑 Google Gemini API Key Setup
This chatbot uses Google Gemini AI to process menu-related queries. You need to configure an API key.

How to Get a Gemini API Key:
Go to Google AI Studio
Sign in with your Google account
Generate an API key from the API Keys section
Copy the API key
Add API Key to the Project:
Open the app.py file
Replace the api_key value in this line:
```bash
genai.configure(api_key="YOUR_GEMINI_API_KEY_HERE")

Save the file
🏃‍♂️ Running the Application
After setting up everything, run the application using Streamlit:

```bash
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
availability (optional)
ratings (optional)

Example CSV:
```bash
dish_name,price,category,cuisine,preparation_time,availability,ratings
Pasta,200,Main Course,Italian,15,Available,4.5
Pizza,300,Main Course,Italian,20,Not Available,4.7
Salad,150,Starter,Healthy,10,Available,4.2

🍲 Placing an Order
Go to the Place Order section.
Select dishes from the multi-select dropdown.
Confirm your order after verifying availability.
Order details are automatically saved to the SQLite database (restaurant_orders.db).

📚 Viewing Order Details in Database
To view saved orders:

```bash
sqlite3 restaurant_orders.db
Then run:
```bash
SELECT * FROM orders;
📝 Generating Order Confirmation
After confirming the order, the chatbot will generate an order summary.
Optionally, download the confirmation receipt in a PDF format.
📜 License
This project is licensed under the MIT License.

