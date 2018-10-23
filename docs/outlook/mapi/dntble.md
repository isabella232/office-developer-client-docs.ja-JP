---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '最終更新日: 2012 年 7 月 5 日'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391949"
---
# <a name="dntble"></a><span data-ttu-id="a68eb-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="a68eb-103">DNTBLE</span></span>

  
  
<span data-ttu-id="a68eb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a68eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a68eb-105">[テーブルの状態をダウンロード](download-table-state.md)中に、サーバーからフォルダーの内容をダウンロードするための情報です。</span><span class="sxs-lookup"><span data-stu-id="a68eb-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="a68eb-106">このダウンロード手順では、 Microsoft Exchange の増分変更の同期 (ICS) を使用します。</span><span class="sxs-lookup"><span data-stu-id="a68eb-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="a68eb-107">ICSの詳細については、[ICSの評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a68eb-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a68eb-108">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a68eb-108">Quick Info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="a68eb-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="a68eb-109">Members</span></span>

 <span data-ttu-id="a68eb-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="a68eb-110">_cEntNew_</span></span>
  
> <span data-ttu-id="a68eb-111">[out]ローカル ストアに追加されたアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="a68eb-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="a68eb-112">ICS を使用してダウンロードしている間に Outlook がこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a68eb-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="a68eb-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="a68eb-113">_cEntMod_</span></span>
  
> <span data-ttu-id="a68eb-114">[out]ローカル ストアで変更されるアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="a68eb-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="a68eb-115">ICS を使用してダウンロードしている間に Outlook がこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a68eb-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="a68eb-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="a68eb-116">_cEntRead_</span></span>
  
> <span data-ttu-id="a68eb-117">[出力]ローカル ストアで開封済みまたは未読にされているアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="a68eb-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="a68eb-118">ICS を使用してダウンロードしている間に Outlook がこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a68eb-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="a68eb-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="a68eb-119">_cEntDel_</span></span>
  
> <span data-ttu-id="a68eb-120">[out]ローカル ストアで削除されるアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="a68eb-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="a68eb-121">ICS を使用してダウンロードしている間に Outlook がこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a68eb-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a68eb-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="a68eb-122">See also</span></span>



[<span data-ttu-id="a68eb-123">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="a68eb-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a68eb-124">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="a68eb-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a68eb-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="a68eb-125">DNTBL</span></span>](dntbl.md)

