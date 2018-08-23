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
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569856"
---
# <a name="ltid"></a><span data-ttu-id="204e9-103">LTID</span><span class="sxs-lookup"><span data-stu-id="204e9-103">LTID</span></span>

  
  
<span data-ttu-id="204e9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="204e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="204e9-105">汎用長い用語 ID は、Outlook、ストア内のオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="204e9-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="204e9-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="204e9-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="204e9-107">Members</span><span class="sxs-lookup"><span data-stu-id="204e9-107">Members</span></span>

 <span data-ttu-id="204e9-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="204e9-108">_guid_</span></span>
  
- <span data-ttu-id="204e9-109">[out]オブジェクトを作成したサーバーの GUID です。</span><span class="sxs-lookup"><span data-stu-id="204e9-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="204e9-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="204e9-110">_globcnt_</span></span>
  
- <span data-ttu-id="204e9-111">[out]Outlook ストア内のオブジェクトを識別する 6 バイトの一意の番号です。</span><span class="sxs-lookup"><span data-stu-id="204e9-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="204e9-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="204e9-112">_wLevel_</span></span>
  
- <span data-ttu-id="204e9-113">[out]Exchange お気に入りパブリック フォルダーのエントリ ID の階層レベルです。</span><span class="sxs-lookup"><span data-stu-id="204e9-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="204e9-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="204e9-114">See also</span></span>



[<span data-ttu-id="204e9-115">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="204e9-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="204e9-116">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="204e9-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="204e9-117">FEID</span><span class="sxs-lookup"><span data-stu-id="204e9-117">FEID</span></span>](feid.md)

