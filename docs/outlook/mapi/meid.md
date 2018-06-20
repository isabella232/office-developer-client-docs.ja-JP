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
ms.openlocfilehash: 1b725dc5151f1f088f2547a1ef82d322c8458b6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801658"
---
# <a name="meid"></a><span data-ttu-id="74125-103">MEID</span><span class="sxs-lookup"><span data-stu-id="74125-103">MEID</span></span>

 
  
<span data-ttu-id="74125-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="74125-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="74125-105">Outlook アイテムの識別子です。</span><span class="sxs-lookup"><span data-stu-id="74125-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="74125-106">エントリ id とその他の関連する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="74125-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="74125-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="74125-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="74125-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="74125-108">Members</span></span>

 <span data-ttu-id="74125-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="74125-109">_abFlags_</span></span>
  
> <span data-ttu-id="74125-110">Outlook アイテムの 4 バイトのエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="74125-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="74125-111">MAPI エントリ id の詳細については、**[エントリ ID](entryid.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74125-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="74125-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="74125-112">_muid_</span></span>
  
> <span data-ttu-id="74125-113">ストア プロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="74125-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="74125-114">**MAPIUID**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74125-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="74125-115">_プレースホルダー_</span><span class="sxs-lookup"><span data-stu-id="74125-115">_placeholder_</span></span>
  
> <span data-ttu-id="74125-116">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="74125-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="74125-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="74125-117">_ltidFld_</span></span>
  
> <span data-ttu-id="74125-118">フォルダーの長期的な ID です。</span><span class="sxs-lookup"><span data-stu-id="74125-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="74125-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="74125-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="74125-120">Outlook アイテムの長期的な ID です。</span><span class="sxs-lookup"><span data-stu-id="74125-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74125-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="74125-121">See also</span></span>



[<span data-ttu-id="74125-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="74125-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="74125-123">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="74125-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="74125-124">LTID</span><span class="sxs-lookup"><span data-stu-id="74125-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="74125-125">同期</span><span class="sxs-lookup"><span data-stu-id="74125-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="74125-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="74125-126">UPMSG</span></span>](upmsg.md)

