# Deciding Between `cchdo.ucsd.edu` and `cchdo.io`

---

## **Advantages of Switching to `cchdo.io`:**

### 1. **Branding & Recognition**
   - A standalone domain (cchdo.io) can be more memorable than a subdomain.
   - Helps with brand identity and promotion.

### 2. **Flexibility**
   - More control over domain and settings.
   - Not tied to primary domain policies.

### 3. **SEO (Search Engine Optimization)**
   - Standalone domain offers more SEO control.
   - Consolidates authority more easily.

### 4. **Independence**
   - Ensures continuity and control, irrespective of changes at UCSD.

---

## **Disadvantages of Switching to `cchdo.io`:**

### 1. **Loss of Association**
   - Being under UCSD lends credibility.

### 2. **Migration Efforts**
   - Requires efforts like content migration, redirecting links, etc.

### 3. **Email Transition**
   - Need to transition to new email addresses.

### 4. **SEO Risks**
   - Risk of search rankings drop if migration is not done correctly.

---

## **Things to Consider:**

| **Consideration** | **Details** |
| --- | --- |
| **Audience Perception** | How users perceive the UCSD association. |
| **Future Plans** | Potential to outgrow UCSD or benefit from a distinct brand. |
| **Technical Capabilities** | Resources to manage smooth domain transition. |

---

![image](https://github.com/Samdopika/presentation/blob/main/Pink%20Landscape%20Desktop%20Wallpaper.gif?raw=true)





# Deciding Between `cchdo.ucsd.edu` and `cchdo.io`

---

## **Advantages of Switching to `cchdo.io`:**

(Using ASCII art for a basic plus symbol representing pros)




### 1. **Branding & Recognition**
### 2. **Flexibility**
### 3. **SEO (Search Engine Optimization)**
### 4. **Independence**

---

## **Disadvantages of Switching to `cchdo.io`:**

(Using ASCII art for a basic minus symbol representing cons)



----------------------------------

# Technical Roadmap for Disabling Cookies in Google Analytics

## 1. Infrastructure Review:
- Confirm access to the website server, Content Management System (CMS), and Google Analytics (GA) account.
- Check if the website uses Google Tag Manager (GTM) or a direct GA script.

## 2. Current Setup Analysis:
- Audit existing GA tags in GTM or within site code.
- Catalog the events, goals, or custom dimensions/metrics that rely on user-specific data.

## 3. Local Development Environment Setup:
- Clone the website to a local development environment.
- Ensure the local version accurately mirrors the live site in terms of tracking.

![Local Development Setup Diagram](URL_to_your_diagram_image_1.png)

## 4. Modify Tracking Code:
- If using **GTM**:
  - Navigate to the GA tag.
  - Within the tag configuration, locate the "Fields to Set" option.
  - Add a new field with the name `storage` and set its value to `none`.
  
- If using **direct GA script**:
  - Locate the `gtag.js` script on the website.
  - Add the following configuration to the script:
    ```javascript
    gtag('config', 'GA_MEASUREMENT_ID', {
      'storage': 'none'
    });
    ```
  Replace `GA_MEASUREMENT_ID` with your actual Google Analytics Measurement ID.

## 5. Implement Fallback User Identification (optional):
- Consider utilizing local storage or session storage as a means of identifying user sessions without using cookies.

![Fallback Identification Diagram](URL_to_your_diagram_image_2.png)

## 6. QA & Testing in Development Environment:
- Use tools like Google Analytics Debugger or Tag Assistant to ensure GA is firing correctly.
- Ensure that no `_ga` cookies are being set.
- Test the site on different browsers to ensure consistent behavior.

## 7. Push to Staging/Pre-production:
- Move the changes to a staging or pre-production environment.
- This environment should mirror the live site and allow for testing in a production-like setting.

## 8. Thorough Testing:
- Conduct end-to-end tests, ensuring that key user journeys and events are still being tracked.
- Engage in load testing if possible to ensure tracking doesn’t impact performance.

![Load Testing Diagram](URL_to_your_diagram_image_3.png)
  
## 9. Document Everything:
- Maintain a technical changelog detailing the steps taken, codes modified, and the reason for changes.
  
## 10. Backup:
- Backup the current live site and its configurations, including any GTM containers.

## 11. Push to Production:
- Implement the changes on the live site.
- If using a version control system, this often means merging the development branch with the master/main branch and deploying.

## 12. Post-deployment Monitoring:
- Monitor real-time GA reports to ensure data is flowing in.
- Check server logs and error logs for any unforeseen issues that might arise due to changes.

![Monitoring Diagram](URL_to_your_diagram_image_4.png)

## 13. Address Potential Issues:
- In the event of missing data or unexpected behavior, consult the documentation and technical changelog to troubleshoot.

## 14. Inform Stakeholders:
- Let non-technical stakeholders know that the change has been implemented and provide insights on any observed data discrepancies or changes.

## 15. Continuous Monitoring & Updates:
- Regularly check for any GA updates or GDPR regulations changes that may require further modifications.

![Continuous Monitoring Diagram](URL_to_your_diagram_image_5.png)

