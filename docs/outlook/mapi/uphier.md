---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a1ec71d7120eab220ee3b11d2a751fba51cee48e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592095"
---
# <a name="uphier"></a><span data-ttu-id="b0a32-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="b0a32-103">UPHIER</span></span>
 
<span data-ttu-id="b0a32-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0a32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0a32-105">[階層の状態をアップロード](upload-hierarchy-state.md)する際にフォルダー階層を同期するための情報です。</span><span class="sxs-lookup"><span data-stu-id="b0a32-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b0a32-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b0a32-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="b0a32-107">Members</span><span class="sxs-lookup"><span data-stu-id="b0a32-107">Members</span></span>

<span data-ttu-id="b0a32-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0a32-108">_ulFlags_</span></span>
  
> <span data-ttu-id="b0a32-109">[in]フォルダー階層を同期するときの動作を変更するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="b0a32-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="b0a32-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="b0a32-110">UPH_OK</span></span>
    
    - <span data-ttu-id="b0a32-111">[in]アップロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="b0a32-111">[in] Upload was successful.</span></span> <span data-ttu-id="b0a32-112">クライアントでは、正常に情報をサーバーにアップロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="b0a32-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="b0a32-113">このフラグを表示するには、時に、Outlook は、フォルダー階層の更新が必要なことを示す内部のブックキーピング情報をクリアします。</span><span class="sxs-lookup"><span data-stu-id="b0a32-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="b0a32-114">クライアントは、アップロードが失敗した場合、HRESULT を渡します。</span><span class="sxs-lookup"><span data-stu-id="b0a32-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="b0a32-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="b0a32-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="b0a32-116">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b0a32-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="b0a32-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="b0a32-117">_iEnt_</span></span>
  
> <span data-ttu-id="b0a32-118">[out]*セント*で指定されたフォルダーの数の同期を追跡するためにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b0a32-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="b0a32-119">_セント_</span><span class="sxs-lookup"><span data-stu-id="b0a32-119">_cEnt_</span></span>
  
> <span data-ttu-id="b0a32-120">[out]同期が取られているフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="b0a32-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0a32-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0a32-121">See also</span></span>

- [<span data-ttu-id="b0a32-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="b0a32-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="b0a32-123">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="b0a32-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="b0a32-124">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="b0a32-124">MAPI Constants</span></span>](mapi-constants.md)

