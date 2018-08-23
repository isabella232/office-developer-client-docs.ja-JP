---
title: エントリ ID と添付 ID をエンコードするためのアルゴリズム
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4d3ca89ea7d3d72f625d38e37494e253b05b1569
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577920"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="1ffe8-103">エントリ ID と添付 ID をエンコードするためのアルゴリズム</span><span class="sxs-lookup"><span data-stu-id="1ffe8-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="1ffe8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ffe8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ffe8-105">ストア プロバイダーに送信できます MAPI 統一リソース ロケーター (URL) の一部として、エントリ ID と、添付ファイル ID MAPI プロトコル ハンドラーでインデックス作成の準備が整っているオブジェクトを識別します。</span><span class="sxs-lookup"><span data-stu-id="1ffe8-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="1ffe8-106">ストア プロバイダーは、ID と ID の添付ファイルのエントリを Unicode 文字列としてエンコードします。</span><span class="sxs-lookup"><span data-stu-id="1ffe8-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="1ffe8-107">このトピックは、エントリ ID または添付ファイル ID のコンパクトな表現を生成するアルゴリズムを示しています。</span><span class="sxs-lookup"><span data-stu-id="1ffe8-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="1ffe8-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ffe8-108">See also</span></span>



[<span data-ttu-id="1ffe8-109">通知ベースのストア インデックス作成について</span><span class="sxs-lookup"><span data-stu-id="1ffe8-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="1ffe8-110">通知ベースのインデックス作成の MAPI URL について</span><span class="sxs-lookup"><span data-stu-id="1ffe8-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

