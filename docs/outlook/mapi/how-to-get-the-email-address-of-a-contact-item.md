---
title: 連絡先アイテムのメール アドレスを取得する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344689"
---
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="66831-103">連絡先アイテムのメール アドレスを取得する</span><span class="sxs-lookup"><span data-stu-id="66831-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="66831-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66831-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66831-105">このトピックでは、microsoft outlook 2010 または microsoft outlook 2013 の連絡先アイテムの電子メールアドレスを表す名前付きプロパティの値を取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="66831-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="66831-106">outlook 2010 および outlook 2013 の連絡先アイテムには、最大3つの電子メールアドレスを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="66831-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="66831-107">各電子メールアドレスは、outlook 2010 および outlook 2013 オブジェクトモデルの outlook 2010 または outlook 2013 **ContactItem**オブジェクトのプロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="66831-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="66831-108">outlook 2010 および outlook 2013 の内部では、電子メールアドレスは MAPI の名前付きプロパティにも対応しています。</span><span class="sxs-lookup"><span data-stu-id="66831-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="66831-109">たとえば、連絡先の最初の電子メールアドレスは、outlook 2010 および outlook 2013 オブジェクトモデルの**ContactItem**の**Email1Address**プロパティに対応し、outlook 2010 および outlook 2013 の内部名[PidLidEmail1EmailAddress 標準プロパティ](pidlidemail1emailaddress-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="66831-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="66831-110">連絡先アイテムの電子メールアドレスの値を取得するには、outlook 2010 または outlook 2013 オブジェクトモデルの**PropertyAccessor**オブジェクトを使用するか、または、最初に[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用して、名前付きプロパティのプロパティタグを取得してから、このプロパティタグを[imapiprop:: GetProps](imapiprop-getprops.md)で指定して、値を取得します。</span><span class="sxs-lookup"><span data-stu-id="66831-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="66831-111">**imapiprop:: getidsfromnames**を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に適切な値を指定します。</span><span class="sxs-lookup"><span data-stu-id="66831-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="66831-112">次のコードサンプルは、 **getidsfromnames**と**GetProps**を使用して`lpContact`、指定された連絡先の最初の電子メールアドレスを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="66831-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
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


