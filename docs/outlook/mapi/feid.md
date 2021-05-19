---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409812"
---
# <a name="feid"></a><span data-ttu-id="1f028-103">FEID</span><span class="sxs-lookup"><span data-stu-id="1f028-103">FEID</span></span>

 
  
<span data-ttu-id="1f028-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f028-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f028-105">フォルダーの識別子。</span><span class="sxs-lookup"><span data-stu-id="1f028-105">Identifier for a folder.</span></span> <span data-ttu-id="1f028-106">エントリ識別子と他の関連情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="1f028-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1f028-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1f028-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="1f028-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="1f028-108">Members</span></span>

 <span data-ttu-id="1f028-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="1f028-109">_abFlags_</span></span>
  
> <span data-ttu-id="1f028-110">フォルダーの 4 バイトのエントリ識別子。</span><span class="sxs-lookup"><span data-stu-id="1f028-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="1f028-111">MAPI エントリ識別子の詳細については **[、「ENTRYID」を参照してください](entryid.md)**。</span><span class="sxs-lookup"><span data-stu-id="1f028-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="1f028-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="1f028-112">_muid_</span></span>
  
> <span data-ttu-id="1f028-113">ストア プロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="1f028-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="1f028-114">MAPIUID の型定義については、mapidefs.h **を参照してください**。</span><span class="sxs-lookup"><span data-stu-id="1f028-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="1f028-115">_プレースホルダー_</span><span class="sxs-lookup"><span data-stu-id="1f028-115">_placeholder_</span></span>
  
> <span data-ttu-id="1f028-116">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1f028-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="1f028-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="1f028-117">_ltid_</span></span>
  
> <span data-ttu-id="1f028-118">フォルダーの長期 ID。</span><span class="sxs-lookup"><span data-stu-id="1f028-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f028-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f028-119">See also</span></span>



[<span data-ttu-id="1f028-120">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="1f028-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="1f028-121">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="1f028-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="1f028-122">LTID</span><span class="sxs-lookup"><span data-stu-id="1f028-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="1f028-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="1f028-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="1f028-124">SYNC</span><span class="sxs-lookup"><span data-stu-id="1f028-124">SYNC</span></span>](sync.md)

