
FitFuse App

FitFuse is a personal fashion management app that helps users organize their wardrobe, get AI-powered outfit recommendations, and interact with a fashion community.

Features

Wardrobe Management – Add, categorize, and manage your personal clothing items.
AI Outfit Recommendations** – Uses AI (in the `fitfuse-recommender`) to suggest daily outfits based on weather, events, and your wardrobe.
Outfit Matching** – Automatically matches clothing items for stylish combinations.
Community Page** – Share your outfits and see recommendations from other users.
Save Preferences** – Track your fashion choices and save favorite styles.

Setup Instructions

1. Install Dependencies

     Flutter dependencies for the mobile app.
     Python dependencies for the AI recommender:

     ```bash
     pip install -r fitfuse-recommender/requirements.txt
     ```

2. Firebase Setup

    Add your `google-services.json` in `android/app/` for Firebase integration.
    Make sure not to commit `google-services.json` or any other secrets to GitHub.

3. Run AI Recommender

    Navigate to the `fitfuse-recommender` folder.
    Run the recommender on your local machine or deploy it on a server:

     ```bash
     uvicorn main:app --reload
     ```
     This exposes a FastAPI endpoint that the Flutter app can query to get outfit recommendations.

4. Run the Flutter App

    Use Flutter CLI or your IDE to launch the mobile app on an emulator or device:

   ```bash
     flutter pub get
     flutter run
     ```

Important Notes

Do not commit any secret files** (like `serviceAccount.json` or `google-services.json`) to the repository.
The AI recommender should be running locally or on a server for the app to fetch real-time outfit suggestions.

License

This project is licensed under **Creative Commons Attribution-NonCommercial (CC BY-NC 4.0)**. You may **use, share, and modify the project for non-commercial purposes only**, and you must give appropriate credit.

For details: [CC BY-NC 4.0 License](https://creativecommons.org/licenses/by-nc/4.0/)
