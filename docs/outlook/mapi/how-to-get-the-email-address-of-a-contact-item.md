---
title: 連絡先アイテムのメール アドレスを取得する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429594"
---
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="b1e29-103">連絡先アイテムのメール アドレスを取得する</span><span class="sxs-lookup"><span data-stu-id="b1e29-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="b1e29-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1e29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1e29-105">このトピックでは、連絡先アイテムまたは連絡先アイテムの電子メール アドレスを表す名前付きプロパティのMicrosoft Outlook 2010 Microsoft Outlook 2013示します。</span><span class="sxs-lookup"><span data-stu-id="b1e29-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="b1e29-106">2010 年および 2013 年 2013 年に最大 3 つのメール アドレスを連絡先Outlook関連付Outlookできます。</span><span class="sxs-lookup"><span data-stu-id="b1e29-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="b1e29-107">各電子メール アドレスは、Outlook 2010 および Outlook 2013 オブジェクト モデルの Outlook 2010 または Outlook 2013 **ContactItem** オブジェクトのプロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="b1e29-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="b1e29-108">2010 Outlook 2013 Outlook内部では、電子メール アドレスは MAPI という名前のプロパティにも対応します。</span><span class="sxs-lookup"><span data-stu-id="b1e29-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="b1e29-109">たとえば、連絡先の最初の電子メール アドレスは、Outlook 2010 および Outlook 2013 オブジェクト モデルの **ContactItem** の **Email1Address** プロパティ、および [pidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)標準プロパティという名前の Outlook 2010 および Outlook 2013 内部に対応します。</span><span class="sxs-lookup"><span data-stu-id="b1e29-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="b1e29-110">連絡先アイテムの電子メール アドレスの値を取得するには、Outlook 2010 または Outlook 2013 オブジェクト モデルの **PropertyAccessor** オブジェクトを使用するか、最初に [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して名前付きプロパティのプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティ タグを指定して値を取得できます。</span><span class="sxs-lookup"><span data-stu-id="b1e29-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="b1e29-111">**IMAPIProp::GetIDsFromNames** を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体の適切な値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1e29-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="b1e29-112">次のコード サンプルは  `lpContact` **、GetIDsFromNames と GetProps** を使用して、指定した連絡先の最初の電子メール アドレスを取得する **方法を示しています**。</span><span class="sxs-lookup"><span data-stu-id="b1e29-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
```cpp
HRESULT HrGetEmail1(LPMESSAGE lpContact) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID = {0}; 
    LPMAPINAMEID lpNamedID = &NamedID; 
    NamedID.lpguid = (LPGUID)&PSETID_Address; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidEmailEmailAddress; 
 
    hRes = lpContact->GetIDsFromNames( 
           1,  
           &lpNamedID,  
           NULL,  
           &lpNamedPropTags); 
 
    if (SUCCEEDED(hRes) && lpNamedPropTags) 
    { 
        SPropTagArray sPropTagArray; 
 
        sPropTagArray.cValues = 1; 
        sPropTagArray.aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_STRING8); 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
 
        hRes = lpContact->GetProps( 
               &sPropTagArray, 
               NULL, 
               &cProps, 
               &lpProps); 
        if (SUCCEEDED(hRes) &&  
            1 == cProps &&  
            lpProps &&  
            PT_STRING8 == PROP_TYPE(lpProps[0].ulPropTag) && 
            lpProps[0].Value.lpszA) 
        { 
            printf("Email address 1 = \"%s\"\n",lpProps[0].Value.lpszA); 
        } 
        MAPIFreeBuffer(lpProps); 
        MAPIFreeBuffer(lpNamedPropTags); 
     } 
     return hRes; 
}
```


