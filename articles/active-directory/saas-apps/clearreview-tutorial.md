---
title: 'Tutorial: Azure Active Directory integration with Clear Review | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and Clear Review.
services: active-directory
documentationCenter: na
author: jeevansd
manager: femila
ms.reviewer: joflore

ms.assetid: 8264159a-11a2-4a8c-8285-4efea0adac8c
ms.service: active-directory
ms.component: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 03/12/2018
ms.author: jeedes

---
# Tutorial: Azure Active Directory integration with Clear Review

In this tutorial, you learn how to integrate Clear Review with Azure Active Directory (Azure AD).

Integrating Clear Review with Azure AD provides you with the following benefits:

- You can control in Azure AD who has access to Clear Review.
- You can enable your users to automatically get signed-on to Clear Review (Single Sign-On) with their Azure AD accounts.
- You can manage your accounts in one central location - the Azure portal.

If you want to know more details about SaaS app integration with Azure AD, see [what is application access and single sign-on with Azure Active Directory](../manage-apps/what-is-single-sign-on.md).

## Prerequisites

To configure Azure AD integration with Clear Review, you need the following items:

- An Azure AD subscription
- A Clear Review single sign-on enabled subscription

> [!NOTE]
> To test the steps in this tutorial, we do not recommend using a production environment.

To test the steps in this tutorial, you should follow these recommendations:

- Do not use your production environment, unless it is necessary.
- If you don't have an Azure AD trial environment, you can [get a one-month trial](https://azure.microsoft.com/pricing/free-trial/).

## Scenario description
In this tutorial, you test Azure AD single sign-on in a test environment. 
The scenario outlined in this tutorial consists of two main building blocks:

1. Adding Clear Review from the gallery
2. Configuring and testing Azure AD single sign-on

## Adding Clear Review from the gallery
To configure the integration of Clear Review into Azure AD, you need to add Clear Review from the gallery to your list of managed SaaS apps.

**To add Clear Review from the gallery, perform the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory** icon. 

	![The Azure Active Directory button][1]

2. Navigate to **Enterprise applications**. Then go to **All applications**.

	![The Enterprise applications blade][2]
	
3. To add new application, click **New application** button on the top of dialog.

	![The New application button][3]

4. In the search box, type **Clear Review**, select **Clear Review** from result panel then click **Add** button to add the application.

	![Clear Review in the results list](./media/clearreview-tutorial/tutorial_clearreview_addfromgallery.png)

## Configure and test Azure AD single sign-on

In this section, you configure and test Azure AD single sign-on with Clear Review based on a test user called "Britta Simon".

For single sign-on to work, Azure AD needs to know what the counterpart user in Clear Review is to a user in Azure AD. In other words, a link relationship between an Azure AD user and the related user in Clear Review needs to be established.

In Clear Review, assign the value of the **user name** in Azure AD as the value of the **Username** to establish the link relationship.

To configure and test Azure AD single sign-on with Clear Review, you need to complete the following building blocks:

1. **[Configure Azure AD Single Sign-On](#configure-azure-ad-single-sign-on)** - to enable your users to use this feature.
2. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
3. **[Create a Clear Review test user](#create-a-clear-review-test-user)** - to have a counterpart of Britta Simon in Clear Review that is linked to the Azure AD representation of user.
4. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

### Configure Azure AD single sign-on

In this section, you enable Azure AD single sign-on in the Azure portal and configure single sign-on in your Clear Review application.

**To configure Azure AD single sign-on with Clear Review, perform the following steps:**

1. In the Azure portal, on the **Clear Review** application integration page, click **Single sign-on**.

	![Configure single sign-on link][4]

2. On the **Single sign-on** dialog, select **Mode** as	**SAML-based Sign-on** to enable single sign-on.
 
	![Single sign-on dialog box](./media/clearreview-tutorial/tutorial_clearreview_samlbase.png)

3. On the **Clear Review Domain and URLs** section, perform the following steps if you wish to configure the application in **IdP initiated** mode:

	![Clear Review Domain and URLs single sign-on information](./media/clearreview-tutorial/tutorial_clearreview_url.png)

    a. In the **Identifier** textbox, type a URL using the following pattern: `https://<customer name>.clearreview.com/sso/metadata/`

	b. In the **Reply URL** textbox, type a URL using the following pattern: `https://<customer name>.clearreview.com/sso/acs/`

4. Check **Show advanced URL settings** and perform the following step if you wish to configure the application in **SP** initiated mode:

	![Clear Review Domain and URLs single sign-on information](./media/clearreview-tutorial/tutorial_clearreview_url_sp.png)

	In the **Sign-on URL** textbox, type a URL using the following pattern:`https://<customer name>.clearreview.com`

	> [!NOTE] 
	> These values are not real. Update these values with the actual Sign-on URL, Identifier, and Reply URL. Contact [Clear Review support team](https://clearreview.com/contact/) to get these values.

5. Clear Review application expect the unique user identifier value in the Name Identifier claim. You should map the user identifier value to **user.mail**.

	![The Attribute Section](./media/clearreview-tutorial/attribute.png)


6. On the **SAML Signing Certificate** section, click **Certificate (Base64)** and then save the certificate file on your computer.

	![The Certificate download link](./media/clearreview-tutorial/tutorial_clearreview_certificate.png)

7. Click **Save** button.

	![Configure Single Sign-On Save button](./media/clearreview-tutorial/tutorial_general_400.png)

8. On the **Clear Review Configuration** section, click **Configure Clear Review** to open **Configure sign-on** window. Copy the **Sign-Out URL ,SAML Entity ID and SAML Single Sign-On Service URL** from the **Quick Reference section.**

	![Clear Review Configuration](./media/clearreview-tutorial/tutorial_clearreview_configure.png) 

9. To configure single sign-on on **Clear Review** side, open the **Clear Review** portal with admin credentials.

10. Select **Admin** from the left navigation.

	![Configure Single Sign-On Save button](./media/clearreview-tutorial/tutorial_clearreview_app_admin1.png)

11. Select **Change** at the bottom of the page.

	![Configure Single Sign-On Save button](./media/clearreview-tutorial/tutorial_clearreview_app_admin2.png)

12. Perform following steps on **Single Sign-On Settings** page

	![Configure Single Sign-On Save button](./media/clearreview-tutorial/tutorial_clearreview_app_admin3.png)

	a. In the **Issuer URL** textbox, paste the value of **SAML Entity ID** which you have copied from Azure portal.

	b. In the **SAML Endpoint** textbox, paste the value of **SAML Single Sign-On Service URL** which you have copied from Azure portal.	

	c. In the **SLO Endpoint** textbox, paste the value of **Sign-On Service URL** which you have copied from Azure portal.	

	d. Open the downloaded certificate in notepad and paste the content in the **X.509 Certificate** textbox.	

13. Click **Save**.

> [!TIP]
> You can now read a concise version of these instructions inside the [Azure portal](https://portal.azure.com), while you are setting up the app!  After adding this app from the **Active Directory > Enterprise Applications** section, simply click the **Single Sign-On** tab and access the embedded documentation through the **Configuration** section at the bottom. You can read more about the embedded documentation feature here: [Azure AD embedded documentation]( https://go.microsoft.com/fwlink/?linkid=845985)

### Create an Azure AD test user

The objective of this section is to create a test user in the Azure portal called Britta Simon.

   ![Create an Azure AD test user][100]

**To create a test user in Azure AD, perform the following steps:**

1. In the Azure portal, in the left pane, click the **Azure Active Directory** button.

    ![The Azure Active Directory button](./media/clearreview-tutorial/create_aaduser_01.png)

2. To display the list of users, go to **Users and groups**, and then click **All users**.

    ![The "Users and groups" and "All users" links](./media/clearreview-tutorial/create_aaduser_02.png)

3. To open the **User** dialog box, click **Add** at the top of the **All Users** dialog box.

    ![The Add button](./media/clearreview-tutorial/create_aaduser_03.png)

4. In the **User** dialog box, perform the following steps:

    ![The User dialog box](./media/clearreview-tutorial/create_aaduser_04.png)

    a. In the **Name** box, type **BrittaSimon**.

    b. In the **User name** box, type the email address of user Britta Simon.

    c. Select the **Show Password** check box, and then write down the value that's displayed in the **Password** box.

    d. Click **Create**.
  
### Create a Clear Review test user

In this section, you create a user called Britta Simon in Clear Review. Please work with [Clear Review support team](https://clearreview.com/contact/) to add the users in the Clear Review platform.

### Assign the Azure AD test user

In this section, you enable Britta Simon to use Azure single sign-on by granting access to Clear Review.

![Assign the user role][200] 

**To assign Britta Simon to Clear Review, perform the following steps:**

1. In the Azure portal, open the applications view, and then navigate to the directory view and go to **Enterprise applications** then click **All applications**.

	![Assign User][201] 

2. In the applications list, select **Clear Review**.

	![The Clear Review link in the Applications list](./media/clearreview-tutorial/tutorial_clearreview_app.png)  

3. In the menu on the left, click **Users and groups**.

	![The "Users and groups" link][202]

4. Click **Add** button. Then select **Users and groups** on **Add Assignment** dialog.

	![The Add Assignment pane][203]

5. On **Users and groups** dialog, select **Britta Simon** in the Users list.

6. Click **Select** button on **Users and groups** dialog.

7. Click **Assign** button on **Add Assignment** dialog.
	
### Test single sign-on

In this section, you test your Azure AD single sign-on configuration using the Access Panel.

When you click the Clear Review tile in the Access Panel, you should get automatically signed-on to your Clear Review application.
For more information about the Access Panel, see [Introduction to the Access Panel](../active-directory-saas-access-panel-introduction.md). 

## Additional resources

* [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](tutorial-list.md)
* [What is application access and single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)



<!--Image references-->

[1]: ./media/clearreview-tutorial/tutorial_general_01.png
[2]: ./media/clearreview-tutorial/tutorial_general_02.png
[3]: ./media/clearreview-tutorial/tutorial_general_03.png
[4]: ./media/clearreview-tutorial/tutorial_general_04.png

[100]: ./media/clearreview-tutorial/tutorial_general_100.png

[200]: ./media/clearreview-tutorial/tutorial_general_200.png
[201]: ./media/clearreview-tutorial/tutorial_general_201.png
[202]: ./media/clearreview-tutorial/tutorial_general_202.png
[203]: ./media/clearreview-tutorial/tutorial_general_203.png
