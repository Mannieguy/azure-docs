---
title: 'Tutorial: Azure Active Directory integration with BorrowBox | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and BorrowBox.
services: active-directory
documentationCenter: na
author: jeevansd
manager: femila
ms.reviewer: joflore

ms.assetid: dd8e4178-9a63-492a-bd48-782e94e404af
ms.service: active-directory
ms.component: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 10/26/2018
ms.author: jeedes

---
# Tutorial: Azure Active Directory integration with BorrowBox

In this tutorial, you learn how to integrate BorrowBox with Azure Active Directory (Azure AD).

Integrating BorrowBox with Azure AD provides you with the following benefits:

- You can control in Azure AD who has access to BorrowBox.
- You can enable your users to automatically get signed-on to BorrowBox (Single Sign-On) with their Azure AD accounts.
- You can manage your accounts in one central location - the Azure portal.

If you want to know more details about SaaS app integration with Azure AD, see [what is application access and single sign-on with Azure Active Directory](../manage-apps/what-is-single-sign-on.md).

## Prerequisites

To configure Azure AD integration with BorrowBox, you need the following items:

- An Azure AD subscription
- A BorrowBox single sign-on enabled subscription

> [!NOTE]
> To test the steps in this tutorial, we do not recommend using a production environment.

To test the steps in this tutorial, you should follow these recommendations:

- Do not use your production environment, unless it is necessary.
- If you don't have an Azure AD trial environment, you can [get a one-month trial](https://azure.microsoft.com/pricing/free-trial/).

## Scenario description
In this tutorial, you test Azure AD single sign-on in a test environment. 
The scenario outlined in this tutorial consists of two main building blocks:

1. Adding BorrowBox from the gallery
2. Configuring and testing Azure AD single sign-on

## Adding BorrowBox from the gallery
To configure the integration of BorrowBox into Azure AD, you need to add BorrowBox from the gallery to your list of managed SaaS apps.

**To add BorrowBox from the gallery, perform the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory** icon. 

	![image](./common/selectazuread.png)

2. Navigate to **Enterprise applications**. Then go to **All applications**.

	![image](./common/a_select_app.png)
	
3. To add new application, click **New application** button on the top of dialog.

	![image](./common/a_new_app.png)

4. In the search box, type **BorrowBox**, select **BorrowBox** from result panel then click **Add** button to add the application.

	 ![image](./media/borrowbox-tutorial/tutorial_borrowbox_addfromgallery.png)

## Configure and test Azure AD single sign-on

In this section, you configure and test Azure AD single sign-on with BorrowBox based on a test user called "Britta Simon".

For single sign-on to work, Azure AD needs to know what the counterpart user in BorrowBox is to a user in Azure AD. In other words, a link relationship between an Azure AD user and the related user in BorrowBox needs to be established.

To configure and test Azure AD single sign-on with BorrowBox, you need to complete the following building blocks:

1. **[Configure Azure AD Single Sign-On](#configure-azure-ad-single-sign-on)** - to enable your users to use this feature.
2. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
3. **[Create a BorrowBox test user](#create-a-borrowbox-test-user)** - to have a counterpart of Britta Simon in BorrowBox that is linked to the Azure AD representation of user.
4. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

### Configure Azure AD single sign-on

In this section, you enable Azure AD single sign-on in the Azure portal and configure single sign-on in your BorrowBox application.

**To configure Azure AD single sign-on with BorrowBox, perform the following steps:**

1. In the [Azure portal](https://portal.azure.com/), on the **BorrowBox** application integration page, select **Single sign-on**.

    ![image](./common/B1_B2_Select_SSO.png)

2. On the **Select a Single sign-on method** dialog, select **SAML** mode to enable single sign-on.

    ![image](./common/b1_b2_saml_sso.png)

3. On the **Set up Single Sign-On with SAML** page, click **Edit** button to open **Basic SAML Configuration** dialog.

	![image](./common/b1-domains_and_urlsedit.png)

4. On the **Basic SAML Configuration** section, the user does not have to perform any step as the app is already pre-integrated with Azure.

    ![image](./media/borrowbox-tutorial/tutorial_borrowbox_url.png)

    a. Click **set additional URLs**.

    b. In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://fe.bolindadigital.com/wldcs_bol_fo/b2i/mainPage.html?b2bSite=<ID>`

    ![image](./media/borrowbox-tutorial/tutorial_borrowbox_url1.png)

	> [!NOTE]
	> The Sign-on URL value is not real. Update the value with the actual Sign-on URL. Contact [BorrowBox Client support team](mailto:borrowbox@bolinda.com) to get the value.

5. BorrowBox application expects the SAML assertions in a specific format. Configure the following claims for this application. You can manage the values of these attributes from the **User Attributes & Claims** section on application integration page. On the **Set up Single Sign-On with SAML** page, click **Edit** button to open **User Attributes & Claims** dialog.

	![image](./media/borrowbox-tutorial/i4-attribute.png)

6. In the **User Claims** section on the **User Attributes & Claims** dialog, configure SAML token attribute as shown in the image above and perform the following steps:
    
	a. Click on **Edit icon** to open the **Manage user claims** dialog.

	![image](./media/borrowbox-tutorial/i2-attribute.png)

	![image](./media/borrowbox-tutorial/i3-attribute.png)

	b. From the **Source attribute** list, select **user.mail**.

	c. Click **Save**. 

7. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, click **Download** to download the appropriate certificate as per your requirement and save it on your computer.

	![image](./media/borrowbox-tutorial/tutorial_borrowbox_certificate.png) 

8. To configure single sign-on on **BorrowBox** side, you need to send the certificate/metadata which you have downloaded from Azure portal to [BorrowBox support team](mailto:borrowbox@bolinda.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create an Azure AD test user

The objective of this section is to create a test user in the Azure portal called Britta Simon.

1. In the Azure portal, in the left pane, select **Azure Active Directory**, select **Users**, and then select **All users**.

    ![image](./common/d_users_and_groups.png)

2. Select **New user** at the top of the screen.

    ![image](./common/d_adduser.png)

3. In the User properties, perform the following steps.

    ![image](./common/d_userproperties.png)

    a. In the **Name** field enter **BrittaSimon**.
  
    b. In the **User name** field type **brittasimon@yourcompanydomain.extension**  
    For example, BrittaSimon@contoso.com

    c. Select **Properties**, select the **Show password** check box, and then write down the value that's displayed in the Password box.

    d. Select **Create**.
 
### Create a BorrowBox test user

The objective of this section is to create a user called Britta Simon in BorrowBox. BorrowBox supports just-in-time provisioning, which is by default enabled. There is no action item for you in this section. A new user is created during an attempt to access BorrowBox if it doesn't exist yet.
>[!Note]
>If you need to create a user manually, contact [BorrowBox support team](mailto:borrowbox@bolinda.com).

### Assign the Azure AD test user

In this section, you enable Britta Simon to use Azure single sign-on by granting access to BorrowBox.

1. In the Azure portal, select **Enterprise Applications**, select **All applications**.

	![image](./common/d_all_applications.png)

2. In the applications list, select **BorrowBox**.

	![image](./media/borrowbox-tutorial/tutorial_borrowbox_app.png)

3. In the menu on the left, select **Users and groups**.

    ![image](./common/d_leftpaneusers.png)

4. Select the **Add** button, then select **Users and groups** in the **Add Assignment** dialog.

    ![image](./common/d_assign_user.png)

4. In the **Users and groups** dialog select **Britta Simon** in the Users list, then click the **Select** button at the bottom of the screen.

5. In the **Add Assignment** dialog select the **Assign** button.
	
### Test single sign-on

In this section, you test your Azure AD single sign-on configuration using the Access Panel.

When you click the BorrowBox tile in the Access Panel, you should get automatically signed-on to your BorrowBox application.
For more information about the Access Panel, see [Introduction to the Access Panel](../active-directory-saas-access-panel-introduction.md). 

## Additional resources

* [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](tutorial-list.md)
* [What is application access and single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)
