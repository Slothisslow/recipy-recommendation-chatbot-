# 🥘 Smart Recipe Chatbot (Veg/Non-Veg Filter)

This is a **Python-based recipe recommendation chatbot** that suggests Indian recipes based on the ingredients you provide. It also allows filtering recipes by diet preference (vegetarian, non-vegetarian, or any).  

---

## How the Code Works

1. **Data Loading**:  
   - The script loads recipe data from `indian_food.csv`.
   - Expected columns: `name`, `ingredients`, `diet`.

2. **Preprocessing Ingredients**:  
   - Ingredients are converted to lowercase, commas are removed, and extra spaces are trimmed.

3. **TF-IDF Vectorization**:  
   - Converts all recipe ingredients into numeric vectors to measure similarity.

4. **User Input Handling**:  
   - Takes ingredients input from the user.
   - Accepts diet preference (`veg`, `non-veg`, or `any`).
   - Filters recipes based on diet preference.

5. **Recipe Matching**:  
   - Computes **cosine similarity** between user input and recipe ingredients.
   - Returns top 5 matching recipes with their ingredients and match score.

6. **Chat Interface**:  
   - Runs in a loop until the user types `exit`.
   - Displays recipe suggestions interactively.

---

## Dataset

- CSV file: `indian_food.csv`
- Required columns:

| Column      | Description                          |
|------------|--------------------------------------|
| name       | Name of the recipe                    |
| ingredients| Comma-separated list of ingredients  |
| diet       | Diet type: `vegetarian` or `non vegetarian` |

**Example:**

| name                 | ingredients                     | diet          |
|---------------------|---------------------------------|---------------|
| Paneer Butter Masala | paneer, butter, cream, tomato   | vegetarian    |
| Chicken Curry        | chicken, onion, garlic, spices | non vegetarian |

---

## How to Run

```bash
python recipe_chatbot.py
