---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414922"
---
# <a name="uphier"></a><span data-ttu-id="4ace9-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="4ace9-103">UPHIER</span></span>
 
<span data-ttu-id="4ace9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ace9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ace9-105">アップロード階層の状態中にフォルダー階層を [同期する場合の情報](upload-hierarchy-state.md)です。</span><span class="sxs-lookup"><span data-stu-id="4ace9-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4ace9-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="4ace9-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="4ace9-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="4ace9-107">Members</span></span>

<span data-ttu-id="4ace9-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4ace9-108">_ulFlags_</span></span>
  
> <span data-ttu-id="4ace9-109">[in]フォルダー階層を同期するときに動作を変更するフラグ。</span><span class="sxs-lookup"><span data-stu-id="4ace9-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="4ace9-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="4ace9-110">UPH_OK</span></span>
    
    - <span data-ttu-id="4ace9-111">[in]アップロード成功しました。</span><span class="sxs-lookup"><span data-stu-id="4ace9-111">[in] Upload was successful.</span></span> <span data-ttu-id="4ace9-112">クライアントは、サーバーに情報を正常にアップロードした後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="4ace9-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="4ace9-113">このフラグを表示すると、Outlook更新が必要なフォルダー階層を示す内部簿記情報が消去されます。</span><span class="sxs-lookup"><span data-stu-id="4ace9-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="4ace9-114">アップロードが成功しなかった場合、クライアントは HRESULT を渡します。</span><span class="sxs-lookup"><span data-stu-id="4ace9-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="4ace9-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="4ace9-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="4ace9-116">[out]このメンバーは、内部Outlookのために予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4ace9-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="4ace9-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="4ace9-117">_iEnt_</span></span>
  
> <span data-ttu-id="4ace9-118">[out]cEnt で指定されたフォルダー数の同期を追跡する  *インデックス*  です。</span><span class="sxs-lookup"><span data-stu-id="4ace9-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="4ace9-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="4ace9-119">_cEnt_</span></span>
  
> <span data-ttu-id="4ace9-120">[out]同期外のフォルダーの数。</span><span class="sxs-lookup"><span data-stu-id="4ace9-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ace9-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ace9-121">See also</span></span>

- [<span data-ttu-id="4ace9-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="4ace9-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="4ace9-123">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="4ace9-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="4ace9-124">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="4ace9-124">MAPI Constants</span></span>](mapi-constants.md)

