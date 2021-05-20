---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430309"
---
# <a name="meid"></a><span data-ttu-id="fcdbc-103">MEID</span><span class="sxs-lookup"><span data-stu-id="fcdbc-103">MEID</span></span>

 
  
<span data-ttu-id="fcdbc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcdbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcdbc-105">アイテムの識別子Outlookします。</span><span class="sxs-lookup"><span data-stu-id="fcdbc-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="fcdbc-106">エントリ識別子と他の関連情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="fcdbc-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fcdbc-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="fcdbc-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="fcdbc-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="fcdbc-108">Members</span></span>

 <span data-ttu-id="fcdbc-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="fcdbc-109">_abFlags_</span></span>
  
> <span data-ttu-id="fcdbc-110">アイテムの 4 バイトエントリ識別子Outlookします。</span><span class="sxs-lookup"><span data-stu-id="fcdbc-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="fcdbc-111">MAPI エントリ識別子の詳細については **[、「ENTRYID」を参照してください](entryid.md)**。</span><span class="sxs-lookup"><span data-stu-id="fcdbc-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="fcdbc-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="fcdbc-112">_muid_</span></span>
  
> <span data-ttu-id="fcdbc-113">ストア プロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="fcdbc-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="fcdbc-114">MAPIUID の型定義については、mapidefs.h **を参照してください**。</span><span class="sxs-lookup"><span data-stu-id="fcdbc-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="fcdbc-115">_プレースホルダー_</span><span class="sxs-lookup"><span data-stu-id="fcdbc-115">_placeholder_</span></span>
  
> <span data-ttu-id="fcdbc-116">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="fcdbc-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="fcdbc-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="fcdbc-117">_ltidFld_</span></span>
  
> <span data-ttu-id="fcdbc-118">フォルダーの長期 ID。</span><span class="sxs-lookup"><span data-stu-id="fcdbc-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="fcdbc-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="fcdbc-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="fcdbc-120">アイテムの長期 ID Outlookします。</span><span class="sxs-lookup"><span data-stu-id="fcdbc-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcdbc-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="fcdbc-121">See also</span></span>



[<span data-ttu-id="fcdbc-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="fcdbc-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="fcdbc-123">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="fcdbc-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="fcdbc-124">LTID</span><span class="sxs-lookup"><span data-stu-id="fcdbc-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="fcdbc-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="fcdbc-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="fcdbc-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="fcdbc-126">UPMSG</span></span>](upmsg.md)

