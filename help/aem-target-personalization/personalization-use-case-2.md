---
title: Getting Started with AEM and Adobe Target
seo-title: Getting Started with AEM and Adobe Target
description: An end-to-end tutorial showing how to create and deliver personalized experience using Adobe Experience Manager and Adobe Target. In this tutorial, you will also learn about different personas involved in the end to end process and how they collaborate with each other
seo-description: An end-to-end tutorial showing how to create and deliver personalized experience using Adobe Experience Manager and Adobe Target. In this tutorial, you will also learn about different personas involved in the end to end process and how they collaborate with each other
---

# Personalization using Adobe Target {#personalization-use-case-2}

In the previous chapter, we learned how to create a Geo based activity within Adobe Target using content created and exported from AEM as HTML Offers.

In this chapter, we are going to explore how to create an activity to redirect your site pages that's hosted on AEM to a new page using Adobe Target.

## Prerequisites

* **AEM**
  * [AEM author and publish instance](./implementation.md#getting-aem) running on localhost 4502 and 4503 respectively.
  * [AEM integrated with Adobe Target using Launch, By Adobe](./using-launch-adobe-io.md#aem-target-using-launch-by-adobe)
* **Experience Cloud**
  * Access to your organizations Adobe Experience Cloud - <https://>`<yourcompany>`.experiencecloud.adobe.com
  * Experience Cloud provisioned with the following solutions
    * [Adobe Target](https://marketing.adobe.com)

## WKND Site - Use Case {#wknd-site-use-case}

WKND site has a new home page and would like to redirect their current site traffic to their new home page and understand if it improves user engagement. As a marketer, you have been assigned the task to create an activity to redirect the current WKND site home page their new home page. Let us explore the WKND site home page and learn how to create an activity with a re-direct offer using Adobe Target.

## Users Involved

For this exercise, the following users needs to be involved, and to perform some tasks, you might need administrative access.

* **Content Producer/Content Editor** (Adobe Experience Manager)
* **Marketer** (Adobe Target / Optimization Team)

## WKND Site Home Page

 ![AEM Target Use Case 1](assets/personalization-use-case-2/aem-target-use-case-2.png)

## Content Editor

1. Marketer initiates the WKND Home Page redesign discussion with AEM Content Editor and details the requirements.
   * ***Requirement*** : Redesign WKND Site Home Page with card based design.
2. Based on the requirements, AEM Content Editor then creates a new WKND Site home page with a card based design and publishes the new home page.

## Marketer

1. Marketer creates an A/B target activity with the re-direct offer as an Experience and 100% website traffic allotted to the new home page with success goal and metrics added.
   1. From you Adobe Target window, navigate to **Activities** tab.
   2. Click **Create Activity** button and select the activity type as **A/B Test**
    ![Adobe Target - Create Activity](assets/personalization-use-case-2/create-ab-activity.png)
   3. Select the **Web** channel and choose the **Visual Experience Composer**
   4. Enter the **Activity URL** and Click **Next** to open the Virtual Experience Composer.
    ![Adobe Target - Create Activity](assets/personalization-use-case-2/create-activity-ab-name.png)
   5. For **Virtual Experience Composer** to load, enable **Allow Load Unsafe scripts** on your browser and reload your page.
    ![Experience Targeting Activity](assets/personalization-use-case-1/load-unsafe-scripts.png)
   6. Notice the WKND Site home page open in Virtual Experience Composer editor.
    ![VEC](assets/personalization-use-case-2/vec.png)
   7. Hover over **Experience B** and select view other options.
    ![Experience B](assets/personalization-use-case-2/redirect-url.png)
   8. Select **Redirect to URL** option and enter the URL to the new WKND Home Page. (http://localhost:4503/content/wknd/en1.html)
    ![Experience B](assets/personalization-use-case-2/redirect-url-2.png)
   9. **Save** your changes and continue with the next steps of Activity Creation.
   10. Select the **Traffic Allocation Method** as manual and allot 100% traffic to **Experience B**.
    ![Experience B Traffic](assets/personalization-use-case-2/traffic.png)
   11. Click **Next**
   12. Provide **Goal Metrics** for your Activity and Save and Close your A/B Test.
    ![A/B Test Goal Metric](assets/personalization-use-case-2/goal-metric.png)
   13. Provide a name (**WKND Home Page Redesign**) for your Activity and save your changes.
   14. From the Activity details screen, make sure to **Activate** your activity.
    ![Activate Activity](assets/personalization-use-case-2/ab-activate.png)
   15. Navigate to WKND Home Page (http://localhost:4503/content/wknd/en.html) and you will re-directed to the redesigned WKND Site Home Page (http://localhost:4503/content/wknd/en1.html).
     ![WKND Home Page Redesigned](assets/personalization-use-case-2/WKND-home-page-redesign.png)