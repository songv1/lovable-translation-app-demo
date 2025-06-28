# lovable-translation-app-demo

# Product Spec / Prompt for Lovable

## Title: Translation Web App (Powered by OpenAI)

**Overview:**
Build a responsive web application that allows users to translate text from one language to another using OpenAI's GPT-4.1-nano model. The app should be clean, intuitive, and functional across desktop and mobile devices.

---

### **Core Functional Requirements**

1. **API Key Input**

   * Provide an input field where users can enter their OpenAI API key.
   * Store the API key in `sessionStorage` so it is automatically deleted when the browser tab or session is closed.
   * Require the key before allowing access to the translation feature.
   * Validate that the key is present before calling the OpenAI API.

2. **Text Input and Language Selection**

   * Allow users to:

     * Enter any block of text.
     * Select a **target language** from a dropdown or list.
   * There is **no need to select the source language** — the model should detect it automatically.

3. **Translation Output**

   * On submission, send a request to OpenAI using the following configuration:

     * **Model:** `gpt-4.1-nano`
     * Prompt should instruct the model to:

       * Detect the input language.
       * Translate the input to the selected target language.
     * Display the translated result in a clearly labeled output area.
   * Example:

     * Input: `"Hello"`
     * Target language: `"Spanish"`
     * Output: `"Hola"`

---

### **Additional Requirements**

* **Responsive Design**

  * Ensure the layout is mobile-friendly and scales properly across screen sizes.

* **User Feedback**

  * Show loading indicators during API calls.
  * Display error messages if:

    * The API key is missing or invalid.
    * The API request fails.

* **Tech Stack Suggestions (Optional)**

  * Frontend: HTML/CSS/JavaScript (or React)
  * No backend is required — the app runs entirely in-browser.
