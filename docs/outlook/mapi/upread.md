---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fa3c0b90a64c90a7c854cb22ac75438fa5fca23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804188"
---
# <a name="upread"></a><span data-ttu-id="ef3f1-103">UPREAD</span><span class="sxs-lookup"><span data-stu-id="ef3f1-103">UPREAD</span></span>

  
  
<span data-ttu-id="ef3f1-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef3f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef3f1-105">[アップロード ステータスの状態を読み取り](upload-read-status-state.md)中にはアイテムの読み取り状態をアップロードする方法の詳細については。</span><span class="sxs-lookup"><span data-stu-id="ef3f1-105">Information for uploading the read state of items during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ef3f1-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ef3f1-106">Quick info</span></span>

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="ef3f1-107">Members</span><span class="sxs-lookup"><span data-stu-id="ef3f1-107">Members</span></span>

 <span data-ttu-id="ef3f1-108">_pupre_</span><span class="sxs-lookup"><span data-stu-id="ef3f1-108">_pupre_</span></span>
  
>  <span data-ttu-id="ef3f1-109">[out]**[UPREADE](upreade.md)** エントリのベクターです。</span><span class="sxs-lookup"><span data-stu-id="ef3f1-109">[out] Vector of **[UPREADE](upreade.md)** entries.</span></span> 
    
 <span data-ttu-id="ef3f1-110">_セント_</span><span class="sxs-lookup"><span data-stu-id="ef3f1-110">_cEnt_</span></span>
  
>  <span data-ttu-id="ef3f1-111">[out]**UPREADE**エントリの数です。</span><span class="sxs-lookup"><span data-stu-id="ef3f1-111">[out] Number of **UPREADE** entries.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ef3f1-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef3f1-112">See also</span></span>



[<span data-ttu-id="ef3f1-113">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="ef3f1-113">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ef3f1-114">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="ef3f1-114">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ef3f1-115">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="ef3f1-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ef3f1-116">UPREADE</span><span class="sxs-lookup"><span data-stu-id="ef3f1-116">UPREADE</span></span>](upreade.md)

