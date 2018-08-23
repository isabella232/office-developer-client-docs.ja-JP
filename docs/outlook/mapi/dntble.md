---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: d92e8d7b3fb14051ffceb829f3df3f6fa12e6e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565859"
---
# <a name="dntble"></a><span data-ttu-id="03382-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="03382-103">DNTBLE</span></span>

  
  
<span data-ttu-id="03382-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03382-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03382-105">[テーブルの状態をダウンロード](download-table-state.md)する時にサーバーからフォルダーの内容をダウンロードするための情報です。</span><span class="sxs-lookup"><span data-stu-id="03382-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="03382-106">このダウンロードのプロセスでは、Microsoft Exchange 増分変更の同期 (ICS) を使用します。</span><span class="sxs-lookup"><span data-stu-id="03382-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="03382-107">ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03382-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="03382-108">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="03382-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="03382-109">Members</span><span class="sxs-lookup"><span data-stu-id="03382-109">Members</span></span>

 <span data-ttu-id="03382-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="03382-110">_cEntNew_</span></span>
  
> <span data-ttu-id="03382-111">[out]ローカル ストアに追加された項目の数です。</span><span class="sxs-lookup"><span data-stu-id="03382-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="03382-112">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03382-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="03382-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="03382-113">_cEntMod_</span></span>
  
> <span data-ttu-id="03382-114">[out]ローカル ストアに変更された項目の数です。</span><span class="sxs-lookup"><span data-stu-id="03382-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="03382-115">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03382-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="03382-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="03382-116">_cEntRead_</span></span>
  
> <span data-ttu-id="03382-117">[out]アイテムの数は、読み取りまたはローカル ストア上の未読のマークです。</span><span class="sxs-lookup"><span data-stu-id="03382-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="03382-118">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03382-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="03382-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="03382-119">_cEntDel_</span></span>
  
> <span data-ttu-id="03382-120">[out]ローカル ストアで削除されたアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="03382-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="03382-121">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03382-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03382-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="03382-122">See also</span></span>



[<span data-ttu-id="03382-123">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="03382-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="03382-124">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="03382-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="03382-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="03382-125">DNTBL</span></span>](dntbl.md)

