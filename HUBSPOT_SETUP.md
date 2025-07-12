# HubSpot Integration Setup Guide

## 🚀 **Complete HubSpot Integration for KloudEdge.cloud**

This guide will help you set up HubSpot CRM integration with your website to collect and manage contact form submissions.

## 📋 **Step-by-Step Setup**

### **Step 1: Create HubSpot Account**

1. **Sign Up for HubSpot**
   - Go to [hubspot.com](https://hubspot.com)
   - Click "Get Started Free"
   - Choose "Marketing Hub" (free tier)
   - Complete your profile setup

2. **Verify Your Account**
   - Check your email for verification
   - Complete your company profile
   - Set up your team members

### **Step 2: Get Your HubSpot Credentials**

1. **Find Your Portal ID**
   - Log into HubSpot
   - Go to **Settings** → **Account Setup** → **Integrations** → **API Keys**
   - Copy your **Portal ID** (it's a number like 12345678)

2. **Create a Contact Form**
   - Go to **Marketing** → **Lead Capture** → **Forms**
   - Click "Create form"
   - Choose "Contact us" template
   - Add these fields:
     - First Name (required)
     - Email (required)
     - Company Name
     - Service Interest (dropdown)
     - Message (required)
   - Save the form and copy the **Form ID**

### **Step 3: Update Your Website Code**

1. **Update Portal ID**
   - Open `index.html`
   - Find line 12: `src="//js.hs-scripts.com/YOUR_PORTAL_ID.js"`
   - Replace `YOUR_PORTAL_ID` with your actual Portal ID

2. **Update Form ID**
   - Find the HubSpot form creation script
   - Replace `YOUR_FORM_ID` with your actual Form ID

### **Step 4: Configure Form Fields**

In your HubSpot form, map these fields:

```javascript
// HubSpot Form Field Mapping
{
    "firstname": "First Name",
    "email": "Email Address", 
    "company": "Company Name",
    "service_interest": "Service Interest",
    "message": "Message"
}
```

### **Step 5: Set Up Email Notifications**

1. **Create Email Template**
   - Go to **Marketing** → **Email** → **Templates**
   - Create a new template for form notifications
   - Include form submission details

2. **Set Up Workflow**
   - Go to **Automation** → **Workflows**
   - Create new workflow triggered by form submission
   - Add email notification action

## 🔧 **Advanced Configuration**

### **Custom Form Styling**

The CSS is already configured to match your website design. You can customize further:

```css
/* Custom HubSpot form colors */
.hs-button {
    background: linear-gradient(45deg, #6366f1, #8b5cf6) !important;
    color: white !important;
}

.hs-form-field input:focus {
    border-color: #6366f1 !important;
}
```

### **Lead Scoring Setup**

1. **Configure Lead Scoring**
   - Go to **Settings** → **Properties** → **Lead Scoring**
   - Set up scoring based on:
     - Service interest (AI/Cloud = higher score)
     - Company size
     - Message length

2. **Create Lead Scoring Properties**
   - Service Interest Weight: AI (10), Cloud (8), Analytics (6)
   - Company Size: Enterprise (10), Medium (6), Small (3)
   - Message Quality: Detailed (5), Basic (2)

### **Email Automation**

1. **Welcome Email Series**
   - Create 3-5 email sequence
   - Send immediately after form submission
   - Include service-specific content

2. **Follow-up Workflow**
   - Day 1: Welcome email
   - Day 3: Service-specific case study
   - Day 7: Consultation booking reminder
   - Day 14: Final follow-up

## 📊 **Data Collection Fields**

### **Recommended Form Fields:**

1. **Basic Information**
   - First Name (required)
   - Last Name
   - Email (required)
   - Phone Number

2. **Company Information**
   - Company Name
   - Industry
   - Company Size
   - Job Title

3. **Project Details**
   - Service Interest (dropdown)
   - Project Timeline
   - Budget Range
   - Project Description

4. **Lead Source**
   - How did you hear about us?
   - Referral Source
   - Campaign Source

## 🎯 **Lead Management**

### **Lead Status Workflow:**

1. **New Lead** → Form submission
2. **Qualified** → Initial contact made
3. **Meeting Scheduled** → Consultation booked
4. **Proposal Sent** → Quote delivered
5. **Negotiation** → Contract discussion
6. **Closed Won** → Project started
7. **Closed Lost** → No response/declined

### **Lead Scoring Criteria:**

- **High Priority (80-100)**
  - Enterprise companies
  - AI/Cloud services
  - Detailed project description
  - Immediate timeline

- **Medium Priority (50-79)**
  - Medium companies
  - Data analytics services
  - General consultation
  - 3-6 month timeline

- **Low Priority (0-49)**
  - Small companies
  - Basic inquiries
  - No specific timeline

## 📈 **Analytics & Reporting**

### **Key Metrics to Track:**

1. **Form Performance**
   - Form submission rate
   - Conversion rate by page
   - Drop-off points

2. **Lead Quality**
   - Lead score distribution
   - Service interest breakdown
   - Company size distribution

3. **Sales Pipeline**
   - Lead to opportunity conversion
   - Average deal size
   - Sales cycle length

### **Dashboard Setup:**

Create a custom dashboard with:
- Daily form submissions
- Lead quality metrics
- Sales pipeline status
- Revenue projections

## 🔒 **Data Privacy & Compliance**

### **GDPR Compliance:**

1. **Privacy Policy**
   - Add privacy policy link to form
   - Include data usage explanation
   - Provide opt-out options

2. **Cookie Consent**
   - Implement cookie banner
   - Track user consent
   - Respect user preferences

3. **Data Retention**
   - Set data retention policies
   - Regular data cleanup
   - User deletion requests

## 🚀 **Testing & Validation**

### **Test Your Integration:**

1. **Form Submission Test**
   - Submit test form
   - Verify data appears in HubSpot
   - Check email notifications

2. **Workflow Testing**
   - Test email sequences
   - Verify lead scoring
   - Check automation triggers

3. **Mobile Testing**
   - Test form on mobile devices
   - Verify responsive design
   - Check submission process

## 📞 **Support & Troubleshooting**

### **Common Issues:**

1. **Form Not Loading**
   - Check Portal ID and Form ID
   - Verify HubSpot script is loaded
   - Check browser console for errors

2. **Data Not Syncing**
   - Verify form field mapping
   - Check HubSpot API limits
   - Review form configuration

3. **Styling Issues**
   - Check CSS conflicts
   - Verify HubSpot CSS overrides
   - Test in different browsers

### **HubSpot Support:**
- **Documentation**: [developers.hubspot.com](https://developers.hubspot.com)
- **Community**: [community.hubspot.com](https://community.hubspot.com)
- **Support**: Available in HubSpot account

## 🎉 **Next Steps**

1. **Complete the setup** using this guide
2. **Test the integration** thoroughly
3. **Set up email automation** workflows
4. **Configure lead scoring** rules
5. **Create reporting** dashboards
6. **Train your team** on HubSpot usage

Your KloudEdge.cloud website is now ready to collect leads efficiently with HubSpot CRM integration! 