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
ms.openlocfilehash: 51a79075dac62a051f5a28dbcb70e7d6ff200e65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799995"
---
# <a name="dntble"></a><span data-ttu-id="1ef6e-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="1ef6e-103">DNTBLE</span></span>

  
  
<span data-ttu-id="1ef6e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ef6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ef6e-105">[テーブルの状態をダウンロード](download-table-state.md)する時にサーバーからフォルダーの内容をダウンロードするための情報です。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="1ef6e-106">このダウンロードのプロセスでは、Microsoft Exchange 増分変更の同期 (ICS) を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="1ef6e-107">ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1ef6e-108">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1ef6e-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="1ef6e-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="1ef6e-109">Members</span></span>

 <span data-ttu-id="1ef6e-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="1ef6e-110">_cEntNew_</span></span>
  
> <span data-ttu-id="1ef6e-111">[out]ローカル ストアに追加された項目の数です。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="1ef6e-112">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="1ef6e-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="1ef6e-113">_cEntMod_</span></span>
  
> <span data-ttu-id="1ef6e-114">[out]ローカル ストアに変更された項目の数です。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="1ef6e-115">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="1ef6e-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="1ef6e-116">_cEntRead_</span></span>
  
> <span data-ttu-id="1ef6e-117">[out]アイテムの数は、読み取りまたはローカル ストア上の未読のマークです。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="1ef6e-118">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="1ef6e-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="1ef6e-119">_cEntDel_</span></span>
  
> <span data-ttu-id="1ef6e-120">[out]ローカル ストアで削除されたアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="1ef6e-121">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="1ef6e-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ef6e-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ef6e-122">See also</span></span>



[<span data-ttu-id="1ef6e-123">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="1ef6e-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="1ef6e-124">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="1ef6e-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="1ef6e-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="1ef6e-125">DNTBL</span></span>](dntbl.md)

