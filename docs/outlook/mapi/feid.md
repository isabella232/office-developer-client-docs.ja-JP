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
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800054"
---
# <a name="feid"></a><span data-ttu-id="f5938-103">FEID</span><span class="sxs-lookup"><span data-stu-id="f5938-103">FEID</span></span>

 
  
<span data-ttu-id="f5938-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5938-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5938-105">フォルダーの識別子です。</span><span class="sxs-lookup"><span data-stu-id="f5938-105">Identifier for a folder.</span></span> <span data-ttu-id="f5938-106">エントリ id とその他の関連する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5938-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f5938-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f5938-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="f5938-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="f5938-108">Members</span></span>

 <span data-ttu-id="f5938-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="f5938-109">_abFlags_</span></span>
  
> <span data-ttu-id="f5938-110">フォルダーの識別子を 4 バイトのエントリです。</span><span class="sxs-lookup"><span data-stu-id="f5938-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="f5938-111">MAPI エントリ id の詳細については、**[エントリ ID](entryid.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f5938-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="f5938-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="f5938-112">_muid_</span></span>
  
> <span data-ttu-id="f5938-113">ストア プロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="f5938-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="f5938-114">**MAPIUID**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f5938-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="f5938-115">_プレースホルダー_</span><span class="sxs-lookup"><span data-stu-id="f5938-115">_placeholder_</span></span>
  
> <span data-ttu-id="f5938-116">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f5938-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="f5938-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="f5938-117">_ltid_</span></span>
  
> <span data-ttu-id="f5938-118">フォルダーの長期的な ID です。</span><span class="sxs-lookup"><span data-stu-id="f5938-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5938-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5938-119">See also</span></span>



[<span data-ttu-id="f5938-120">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="f5938-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f5938-121">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="f5938-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f5938-122">LTID</span><span class="sxs-lookup"><span data-stu-id="f5938-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="f5938-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="f5938-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="f5938-124">同期</span><span class="sxs-lookup"><span data-stu-id="f5938-124">SYNC</span></span>](sync.md)

