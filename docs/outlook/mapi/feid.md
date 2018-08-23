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
ms.openlocfilehash: 3e534f91863e2a1300e03d112d1f532f486eedd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588308"
---
# <a name="feid"></a><span data-ttu-id="8b518-103">FEID</span><span class="sxs-lookup"><span data-stu-id="8b518-103">FEID</span></span>

 
  
<span data-ttu-id="8b518-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b518-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b518-105">フォルダーの識別子です。</span><span class="sxs-lookup"><span data-stu-id="8b518-105">Identifier for a folder.</span></span> <span data-ttu-id="8b518-106">エントリ id とその他の関連する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b518-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8b518-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="8b518-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="8b518-108">Members</span><span class="sxs-lookup"><span data-stu-id="8b518-108">Members</span></span>

 <span data-ttu-id="8b518-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="8b518-109">_abFlags_</span></span>
  
> <span data-ttu-id="8b518-110">フォルダーの識別子を 4 バイトのエントリです。</span><span class="sxs-lookup"><span data-stu-id="8b518-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="8b518-111">MAPI エントリ id の詳細については、**[エントリ ID](entryid.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b518-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="8b518-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="8b518-112">_muid_</span></span>
  
> <span data-ttu-id="8b518-113">ストア プロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="8b518-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="8b518-114">**MAPIUID**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b518-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="8b518-115">_プレースホルダー_</span><span class="sxs-lookup"><span data-stu-id="8b518-115">_placeholder_</span></span>
  
> <span data-ttu-id="8b518-116">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8b518-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="8b518-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="8b518-117">_ltid_</span></span>
  
> <span data-ttu-id="8b518-118">フォルダーの長期的な ID です。</span><span class="sxs-lookup"><span data-stu-id="8b518-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b518-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b518-119">See also</span></span>



[<span data-ttu-id="8b518-120">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="8b518-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8b518-121">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="8b518-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8b518-122">LTID</span><span class="sxs-lookup"><span data-stu-id="8b518-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="8b518-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="8b518-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="8b518-124">SYNC</span><span class="sxs-lookup"><span data-stu-id="8b518-124">SYNC</span></span>](sync.md)

