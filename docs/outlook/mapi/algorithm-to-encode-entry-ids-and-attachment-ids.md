---
title: エントリ id と添付ファイル id をエンコードするためのアルゴリズム
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6c39fe513be122f265fdc316629a3e64a156fdc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318180"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>エントリ id と添付ファイル id をエンコードするためのアルゴリズム

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストアプロバイダーは、mapi の Uniform resource Locator (URL) の一部として送信し、インデックス処理の準備ができているオブジェクトを識別するために、エントリ id と添付ファイル id を mapi プロトコルハンドラーに送信できます。 ストアプロバイダーは、エントリ id と添付ファイル id を Unicode 文字列としてエンコードします。 このトピックでは、エントリ id または添付ファイル id のコンパクト表現を生成するアルゴリズムを示します。
  
```cpp
const WORD kwBaseOffset = 0xAC00;  // Hangul char range (AC00-D7AF) 
LPWSTR EncodeID(ULONG cbEID, LPENTRYID rgbID) 
{ 
    ULONG   i = 0; 
    LPWSTR  pwzDst = NULL; 
    LPBYTE  pbSrc = NULL; 
    LPWSTR  pwzIDEncoded = NULL; 
 
    // rgbID is the item Entry ID or the attachment ID 
    // cbID is the size in bytes of rgbID 
 
    // Allocate memory for pwzIDEncoded 
    pwzIDEncoded = new WCHAR[cbEID]; 
    if (!pwzIDEncoded) return NULL; 
 
    for (i = 0, pbSrc = (LPBYTE)rgbID, pwzDst = pwzIDEncoded; 
        i < cbEID; 
        i++, pbSrc++, pwzDst++) 
    { 
        *pwzDst = (WCHAR) (*pbSrc + kwBaseOffset); 
    } 
 
    // Ensure NULL terminated 
    *pwzDst = L'\0'; 
 
    // pwzIDEncoded now contains the entry ID encoded. 
    return pwzIDEncoded; 
}
```

## <a name="see-also"></a>関連項目



[通知ベースのストアインデックス作成について](about-notification-based-store-indexing.md)
  
[通知ベースのインデックス作成の MAPI url について](about-mapi-urls-for-notification-based-indexing.md)

