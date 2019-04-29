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
  
このトピックでは、microsoft outlook 2010 または microsoft outlook 2013 の連絡先アイテムの電子メールアドレスを表す名前付きプロパティの値を取得する方法について説明します。
  
outlook 2010 および outlook 2013 の連絡先アイテムには、最大3つの電子メールアドレスを関連付けることができます。 各電子メールアドレスは、outlook 2010 および outlook 2013 オブジェクトモデルの outlook 2010 または outlook 2013 **ContactItem**オブジェクトのプロパティに対応します。 outlook 2010 および outlook 2013 の内部では、電子メールアドレスは MAPI の名前付きプロパティにも対応しています。 たとえば、連絡先の最初の電子メールアドレスは、outlook 2010 および outlook 2013 オブジェクトモデルの**ContactItem**の**Email1Address**プロパティに対応し、outlook 2010 および outlook 2013 の内部名[PidLidEmail1EmailAddress 標準プロパティ](pidlidemail1emailaddress-canonical-property.md)。
  
連絡先アイテムの電子メールアドレスの値を取得するには、outlook 2010 または outlook 2013 オブジェクトモデルの**PropertyAccessor**オブジェクトを使用するか、または、最初に[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用して、名前付きプロパティのプロパティタグを取得してから、このプロパティタグを[imapiprop:: GetProps](imapiprop-getprops.md)で指定して、値を取得します。 **imapiprop:: getidsfromnames**を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に適切な値を指定します。 次のコードサンプルは、 **getidsfromnames**と**GetProps**を使用して`lpContact`、指定された連絡先の最初の電子メールアドレスを取得する方法を示しています。 
  
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


