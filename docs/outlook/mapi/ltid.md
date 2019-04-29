---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419437"
---
# <a name="ltid"></a><span data-ttu-id="58e7e-103">LTID</span><span class="sxs-lookup"><span data-stu-id="58e7e-103">LTID</span></span>

  
  
<span data-ttu-id="58e7e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58e7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58e7e-105">Outlook ストア内のオブジェクトの一般的な長い用語 ID。</span><span class="sxs-lookup"><span data-stu-id="58e7e-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="58e7e-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="58e7e-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="58e7e-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="58e7e-107">Members</span></span>

 <span data-ttu-id="58e7e-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="58e7e-108">_guid_</span></span>
  
- <span data-ttu-id="58e7e-109">読み上げオブジェクトを作成したサーバーの GUID。</span><span class="sxs-lookup"><span data-stu-id="58e7e-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="58e7e-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="58e7e-110">_globcnt_</span></span>
  
- <span data-ttu-id="58e7e-111">読み上げOutlook ストア内のオブジェクトを識別する6バイトの一意の番号。</span><span class="sxs-lookup"><span data-stu-id="58e7e-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="58e7e-112">_wlevel_</span><span class="sxs-lookup"><span data-stu-id="58e7e-112">_wLevel_</span></span>
  
- <span data-ttu-id="58e7e-113">読み上げExchange お気に入りパブリックフォルダーのエントリ ID の階層レベル。</span><span class="sxs-lookup"><span data-stu-id="58e7e-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58e7e-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="58e7e-114">See also</span></span>



[<span data-ttu-id="58e7e-115">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="58e7e-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="58e7e-116">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="58e7e-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="58e7e-117">FEID</span><span class="sxs-lookup"><span data-stu-id="58e7e-117">FEID</span></span>](feid.md)

