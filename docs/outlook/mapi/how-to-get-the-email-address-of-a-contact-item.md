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
# <a name="get-the-email-address-of-a-contact-item"></a>連絡先アイテムのメール アドレスを取得する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、連絡先アイテムまたは連絡先アイテムの電子メール アドレスを表す名前付きプロパティのMicrosoft Outlook 2010 Microsoft Outlook 2013示します。
  
2010 年および 2013 年 2013 年に最大 3 つのメール アドレスを連絡先Outlook関連付Outlookできます。 各電子メール アドレスは、Outlook 2010 および Outlook 2013 オブジェクト モデルの Outlook 2010 または Outlook 2013 **ContactItem** オブジェクトのプロパティに対応します。 2010 Outlook 2013 Outlook内部では、電子メール アドレスは MAPI という名前のプロパティにも対応します。 たとえば、連絡先の最初の電子メール アドレスは、Outlook 2010 および Outlook 2013 オブジェクト モデルの **ContactItem** の **Email1Address** プロパティ、および [pidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)標準プロパティという名前の Outlook 2010 および Outlook 2013 内部に対応します。
  
連絡先アイテムの電子メール アドレスの値を取得するには、Outlook 2010 または Outlook 2013 オブジェクト モデルの **PropertyAccessor** オブジェクトを使用するか、最初に [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して名前付きプロパティのプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティ タグを指定して値を取得できます。 **IMAPIProp::GetIDsFromNames** を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体の適切な値を指定します。 次のコード サンプルは  `lpContact` **、GetIDsFromNames と GetProps** を使用して、指定した連絡先の最初の電子メール アドレスを取得する **方法を示しています**。 
  
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


