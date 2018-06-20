---
title: 連絡先アイテムの電子メール アドレスを取得します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: ce9579cb6b07336cae7d69fe503c918d96946b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800227"
---
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="fad46-103">連絡先アイテムの電子メール アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="fad46-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="fad46-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fad46-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fad46-105">このトピックでは、Microsoft Outlook 2010 または Microsoft Outlook 2013 の連絡先アイテムの電子メール アドレスを表す名前付きプロパティの値を取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fad46-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="fad46-106">最大 3 つの電子メール アドレスを Outlook 2010、Outlook 2013 で連絡先アイテムと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="fad46-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="fad46-107">各電子メール アドレスは、Outlook 2010、Outlook 2013 オブジェクト モデルで Outlook 2010 または Outlook 2013 **ContactItem**オブジェクトのプロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="fad46-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="fad46-108">Outlook 2010、Outlook 2013 の内部、電子メール アドレスにも対応して、MAPI 名前付きプロパティ。</span><span class="sxs-lookup"><span data-stu-id="fad46-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="fad46-109">連絡先の最初の電子メール アドレスが、Outlook 2010、Outlook 2013 オブジェクト モデル、および Outlook 2010、Outlook 2013 の内部名前付き[で**ContactItem**の**Email1Address**プロパティに対応するなど、標準的なプロパティを PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="fad46-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="fad46-110">連絡先アイテムの電子メール アドレスの値を取得するには、Outlook 2010 または Outlook 2013 オブジェクト モデルの**PropertyAccessor**オブジェクトを使用して、または最初に、名前付きプロパティのプロパティ タグを取得する[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用し、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)では、このプロパティのタグを指定します。</span><span class="sxs-lookup"><span data-stu-id="fad46-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="fad46-111">**IMAPIProp::GetIDsFromNames**を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の適切な値を指定します。</span><span class="sxs-lookup"><span data-stu-id="fad46-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="fad46-112">次のコード サンプルは、指定した連絡先の最初の電子メール アドレスを取得する方法を示します`lpContact`、 **GetIDsFromNames**と**GetProps**を使用します。</span><span class="sxs-lookup"><span data-stu-id="fad46-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
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


