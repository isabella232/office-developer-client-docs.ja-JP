---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: '最終更新日: 2012 年7月3日'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430309"
---
# <a name="meid"></a><span data-ttu-id="7c453-103">MEID</span><span class="sxs-lookup"><span data-stu-id="7c453-103">MEID</span></span>

 
  
<span data-ttu-id="7c453-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c453-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c453-105">Outlook アイテムの識別子。</span><span class="sxs-lookup"><span data-stu-id="7c453-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="7c453-106">エントリ id とその他の関連情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c453-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7c453-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="7c453-107">Quick info</span></span>

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a><span data-ttu-id="7c453-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="7c453-108">Members</span></span>

 <span data-ttu-id="7c453-109">_abflags_</span><span class="sxs-lookup"><span data-stu-id="7c453-109">_abFlags_</span></span>
  
> <span data-ttu-id="7c453-110">Outlook アイテムの4バイトのエントリ id。</span><span class="sxs-lookup"><span data-stu-id="7c453-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="7c453-111">MAPI エントリ識別子の詳細については、「 **[ENTRYID](entryid.md)**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c453-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="7c453-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="7c453-112">_muid_</span></span>
  
> <span data-ttu-id="7c453-113">ストアプロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="7c453-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="7c453-114">**MAPIUID**の型定義については、「mapidefs.h」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c453-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="7c453-115">_プレースホルダー_</span><span class="sxs-lookup"><span data-stu-id="7c453-115">_placeholder_</span></span>
  
> <span data-ttu-id="7c453-116">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7c453-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="7c453-117">_ltidfld_</span><span class="sxs-lookup"><span data-stu-id="7c453-117">_ltidFld_</span></span>
  
> <span data-ttu-id="7c453-118">フォルダーの長期 ID。</span><span class="sxs-lookup"><span data-stu-id="7c453-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="7c453-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="7c453-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="7c453-120">Outlook アイテムの長期 ID。</span><span class="sxs-lookup"><span data-stu-id="7c453-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c453-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c453-121">See also</span></span>



[<span data-ttu-id="7c453-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="7c453-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7c453-123">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="7c453-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7c453-124">LTID</span><span class="sxs-lookup"><span data-stu-id="7c453-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="7c453-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="7c453-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="7c453-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="7c453-126">UPMSG</span></span>](upmsg.md)

