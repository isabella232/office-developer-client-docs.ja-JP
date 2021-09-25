---
title: エントリの ID と添付ファイルの ID をエンコードするアルゴリズム
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: eb8ace42381002d96a4a89e2a9b7eb36898d7927
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556932"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>エントリの ID と添付ファイルの ID をエンコードするアルゴリズム

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストア プロバイダーは、MAPI Uniform Resource Locator (URL) の一部として、エントリ ID と添付ファイル ID を MAPI プロトコル ハンドラーに送信して、インデックス作成の準備ができているオブジェクトを識別できます。 ストア プロバイダーは、エントリ ID と添付ファイル ID を Unicode 文字列としてエンコードします。 このトピックでは、エントリ ID または添付ファイル ID のコンパクトな表現を生成するアルゴリズムを示します。
  
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



[ストア インデックスNotification-Basedについて](about-notification-based-store-indexing.md)
  
[インデックス作成の MAPI URL Notification-Basedについて](about-mapi-urls-for-notification-based-indexing.md)

