---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801286"
---
# <a name="ltid"></a><span data-ttu-id="3517f-103">LTID</span><span class="sxs-lookup"><span data-stu-id="3517f-103">LTID</span></span>

  
  
<span data-ttu-id="3517f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3517f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3517f-105">汎用長い用語 ID は、Outlook、ストア内のオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="3517f-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3517f-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3517f-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="3517f-107">Members</span><span class="sxs-lookup"><span data-stu-id="3517f-107">Members</span></span>

 <span data-ttu-id="3517f-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="3517f-108">_guid_</span></span>
  
- <span data-ttu-id="3517f-109">[out]オブジェクトを作成したサーバーの GUID です。</span><span class="sxs-lookup"><span data-stu-id="3517f-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="3517f-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="3517f-110">_globcnt_</span></span>
  
- <span data-ttu-id="3517f-111">[out]Outlook ストア内のオブジェクトを識別する 6 バイトの一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="3517f-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="3517f-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="3517f-112">_wLevel_</span></span>
  
- <span data-ttu-id="3517f-113">[out]Exchange お気に入りパブリック フォルダーのエントリ ID の階層レベルです。</span><span class="sxs-lookup"><span data-stu-id="3517f-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3517f-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="3517f-114">See also</span></span>



[<span data-ttu-id="3517f-115">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="3517f-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3517f-116">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="3517f-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3517f-117">FEID</span><span class="sxs-lookup"><span data-stu-id="3517f-117">FEID</span></span>](feid.md)

