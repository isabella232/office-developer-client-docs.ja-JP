---
title: エントリ ID と添付 ID をエンコードするためのアルゴリズム
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 710ba5173dcce6e948e1f49c7d82e46bc83b8200
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799677"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>エントリ ID と添付 ID をエンコードするためのアルゴリズム

  
  
**適用対象**: Outlook 
  
ストア プロバイダーに送信できます MAPI 統一リソース ロケーター (URL) の一部として、エントリ ID と、添付ファイル ID MAPI プロトコル ハンドラーでインデックス作成の準備が整っているオブジェクトを識別します。 ストア プロバイダーは、ID と ID の添付ファイルのエントリを Unicode 文字列としてエンコードします。 このトピックは、エントリ ID または添付ファイル ID のコンパクトな表現を生成するアルゴリズムを示しています。
  
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



[通知ベースのストア インデックス作成について](about-notification-based-store-indexing.md)
  
[通知ベースのインデックス作成の MAPI URL について](about-mapi-urls-for-notification-based-indexing.md)

