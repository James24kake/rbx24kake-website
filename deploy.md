# Deployment Guide for Roblox Rewards Website

## Prerequisites
1. Install Vercel CLI:
   ```
   npm install -g vercel
   ```

2. Create an account on Vercel.com if you don't have one

## Deployment Steps

1. Login to Vercel from the command line:
   ```
   vercel login
   ```

2. Deploy the project:
   ```
   vercel
   ```

3. Follow the prompts:
   - Set up and deploy? Yes
   - Which scope? (Select your account)
   - Link to existing project? No
   - Project name? (Press Enter for default or type a name)
   - In which directory is your code located? ./ (or press Enter)
   - Want to override settings? No

4. Set Environment Variables in the Vercel Dashboard:
   - SUPABASE_URL=https://sikwknhwosbuqvrffbdm.supabase.co
   - SUPABASE_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InNpa3drbmh3b3NidXF2cmZmYmRtIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NDc2OTAzNDYsImV4cCI6MjA2MzI2NjM0Nn0.3rh1d8K1OABbLfOsv74MmDxY7dvNDfXxtkTzze4MdsY
   - JWT_SECRET=roblox-rewards-secret-key
   - JWT_EXPIRE=30d
   - NODE_ENV=production
   - PORT=5000
   - FRONTEND_URL=https://rbx24kake.com

5. Configure Domain:
   - Go to your Vercel project
   - Click on "Domains"
   - Add your domain: rbx24kake.com
   - Follow the instructions to set up DNS records with your domain provider (Namecheap)

## Updating Your Deployment

To update your site after making changes:
1. Commit your changes
2. Run `vercel --prod` to deploy to production

## Monitoring
1. View logs in the Vercel dashboard
2. Set up email notifications for deployment failures

## Troubleshooting
1. Check Vercel deployment logs
2. If the build fails, try building locally first
3. For database connection issues, verify your environment variables
4. For API errors, check backend logs 