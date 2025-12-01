# MedFee India: MBBS Fee Calculator & AI Counselor

A comprehensive React-based application designed for Indian medical aspirants to calculate MBBS course expenses, predict eligible colleges based on NEET scores, and receive AI-powered counseling.

## 🚀 Features

*   **College Predictor**: Filter colleges by NEET score, State, College Type (Govt/Private/Deemed), and Budget.
*   **Fee Calculator**: Detailed breakdown of Tuition, Hostel, Mess, and One-time fees with visual Pie Charts.
*   **AI Counselor**: Integrated with Google Gemini API to answer specific queries about bonds, placements, and admission rules.
*   **Data Visualization**: Interactive charts using Recharts.
*   **Responsive Design**: Built with Tailwind CSS for mobile and desktop.

## 🛠️ Tech Stack

*   **Frontend**: React (v19), TypeScript, Vite
*   **Styling**: Tailwind CSS, Lucide React (Icons)
*   **Charts**: Recharts
*   **AI Integration**: Google Gemini API (`@google/genai`)

## ⚙️ Installation & Local Development

1.  **Clone the repository** (or download source files):
    ```bash
    git clone <your-repo-url>
    cd medfee-india
    ```

2.  **Install dependencies**:
    ```bash
    npm install
    ```

3.  **Configure API Key**:
    *   Create a file named `.env` in the root directory.
    *   Add your Google Gemini API Key:
    ```env
    VITE_API_KEY=your_actual_api_key_here
    ```
    *   *Note: Get your key from [Google AI Studio](https://aistudio.google.com/).*

4.  **Run the development server**:
    ```bash
    npm run dev
    ```
    Open `http://localhost:5173` in your browser.

## 📦 Building for Production

To create an optimized build for deployment:

```bash
npm run build
```

This will create a `dist` folder containing the static `index.html`, JavaScript, and CSS files.

## 🌐 Deployment Guides

### 1. General Deployment (Vercel/Netlify/Hostinger)
1.  Run `npm run build`.
2.  Upload the contents of the `dist` folder to your hosting provider's public directory (usually `public_html`).

### 2. Deploying to a Subdomain (e.g., calculator.acembbs.com)
The project is already configured with `base: './'` in `vite.config.ts` to support relative paths.

1.  Create the subdomain in your hosting control panel (cPanel, etc.).
2.  Run `npm run build`.
3.  Open the `dist` folder.
4.  Upload **all files inside `dist`** to the folder created for your subdomain (e.g., `public_html/calculator`).

### 3. Embedding in WordPress
**Method A: Iframe (Recommended)**
1.  Host the app on a separate platform (like Vercel) or a subdomain.
2.  Add a Custom HTML block in WordPress:
    ```html
    <iframe 
      src="https://calculator.yourdomain.com" 
      width="100%" 
      height="800px" 
      style="border:none;"
    ></iframe>
    ```

**Method B: Direct Embed**
1.  Upload the `.js` and `.css` files from `dist/assets` to your WordPress media library.
2.  In a Custom HTML block on your page:
    ```html
    <div id="root"></div>
    <link rel="stylesheet" href="/path/to/your/style.css">
    <script type="module" src="/path/to/your/script.js"></script>
    ```

## ⚠️ Disclaimer
The fee data provided in `constants.ts` is for estimation purposes based on historical data. Users should verify actual fees from official college websites or MCC counseling brochures.
