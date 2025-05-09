# RNR Vehicle Fitment Tool

A web application that provides wheel and tire fitment information for vehicles, powered by OpenAI.

## Features

- Select vehicle year, make, model, and trim
- View OEM (factory) wheel and tire specifications
- See upgrade options for 20", 22", and 24" wheels
- Check inventory availability
- Export fitment details
- Save search history

## Deployment Instructions

### Prerequisites

- A Netlify account (free tier is fine)
- An OpenAI API key
- Node.js and npm installed for local development (optional)

### Option 1: Deploy via Netlify UI

1. **Prepare Your Files**
   - Create a ZIP file containing these files:
     - `index.html`
     - `netlify.toml`
     - `package.json`
     - Create a folder named `netlify/functions` and place `get-fitment.js` inside it

2. **Deploy to Netlify**
   - Log in to your Netlify account
   - Go to the "Sites" section
   - Drag and drop the ZIP file onto the Netlify dashboard
   - Wait for deployment to complete

3. **Set Environment Variables**
   - In your Netlify site dashboard, go to Site settings > Environment variables
   - Add a new variable:
     - Key: `OPENAI_API_KEY`
     - Value: Your OpenAI API key

4. **Test Your Deployment**
   - Visit your Netlify site URL
   - Enter vehicle information to test the functionality

### Option 2: Deploy via Netlify CLI (for Developers)

1. **Clone this Repository**
   ```
   git clone <repository-url>
   cd rnr-vehicle-fitment-tool
   ```

2. **Install Dependencies**
   ```
   npm install
   ```

3. **Set Up Environment Variables**
   - Create a `.env` file in the root directory:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```

4. **Test Locally**
   ```
   netlify dev
   ```

5. **Deploy to Netlify**
   ```
   netlify deploy --prod
   ```

6. **Set Environment Variables in Netlify**
   - After deployment, go to Netlify dashboard
   - Go to Site settings > Environment variables
   - Add your OpenAI API key as described in Option 1

## Customization

- Modify the HTML and CSS to change the appearance
- Adjust the OpenAI prompt in `get-fitment.js` to change the output format or requested information
- Add additional functionality by extending the JavaScript code

## Troubleshooting

- **Fitment Data Not Loading**: Check your OpenAI API key and usage limits
- **Missing Wheel Sizes**: Try different vehicle combinations or adjust the OpenAI prompt
- **Function Error**: Check the Netlify function logs in your Netlify dashboard

## Support

For assistance, contact Shane Lockhart at aslockhart10@gmail.com
