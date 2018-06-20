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
# <a name="get-the-email-address-of-a-contact-item"></a>連絡先アイテムの電子メール アドレスを取得します。

**適用されます**: Outlook 
  
このトピックでは、Microsoft Outlook 2010 または Microsoft Outlook 2013 の連絡先アイテムの電子メール アドレスを表す名前付きプロパティの値を取得する方法を示します。
  
最大 3 つの電子メール アドレスを Outlook 2010、Outlook 2013 で連絡先アイテムと関連付けることができます。 各電子メール アドレスは、Outlook 2010、Outlook 2013 オブジェクト モデルで Outlook 2010 または Outlook 2013 **ContactItem**オブジェクトのプロパティに対応します。 Outlook 2010、Outlook 2013 の内部、電子メール アドレスにも対応して、MAPI 名前付きプロパティ。 連絡先の最初の電子メール アドレスが、Outlook 2010、Outlook 2013 オブジェクト モデル、および Outlook 2010、Outlook 2013 の内部名前付き[で**ContactItem**の**Email1Address**プロパティに対応するなど、標準的なプロパティを PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)。
  
連絡先アイテムの電子メール アドレスの値を取得するには、Outlook 2010 または Outlook 2013 オブジェクト モデルの**PropertyAccessor**オブジェクトを使用して、または最初に、名前付きプロパティのプロパティ タグを取得する[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用し、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)では、このプロパティのタグを指定します。 **IMAPIProp::GetIDsFromNames**を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の適切な値を指定します。 次のコード サンプルは、指定した連絡先の最初の電子メール アドレスを取得する方法を示します`lpContact`、 **GetIDsFromNames**と**GetProps**を使用します。 
  
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


