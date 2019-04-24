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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359424"
---
# <a name="uphier"></a><span data-ttu-id="30fe7-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="30fe7-103">UPHIER</span></span>
 
<span data-ttu-id="30fe7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30fe7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30fe7-105">[階層のアップロード状態](upload-hierarchy-state.md)でのフォルダー階層の同期に関する情報。</span><span class="sxs-lookup"><span data-stu-id="30fe7-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="30fe7-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="30fe7-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="30fe7-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="30fe7-107">Members</span></span>

<span data-ttu-id="30fe7-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="30fe7-108">_ulFlags_</span></span>
  
> <span data-ttu-id="30fe7-109">順番フォルダー階層を同期するときの動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="30fe7-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="30fe7-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="30fe7-110">UPH_OK</span></span>
    
    - <span data-ttu-id="30fe7-111">順番アップロードに成功しました。</span><span class="sxs-lookup"><span data-stu-id="30fe7-111">[in] Upload was successful.</span></span> <span data-ttu-id="30fe7-112">クライアントは、サーバーに情報を正常にアップロードした後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="30fe7-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="30fe7-113">このフラグが表示されると、Outlook は、更新が必要なフォルダー階層を示す内部のブックキーピング情報をクリアします。</span><span class="sxs-lookup"><span data-stu-id="30fe7-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="30fe7-114">アップロードが成功しなかった場合、クライアントは HRESULT を渡します。</span><span class="sxs-lookup"><span data-stu-id="30fe7-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="30fe7-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="30fe7-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="30fe7-116">読み上げこのメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="30fe7-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="30fe7-117">_ient_</span><span class="sxs-lookup"><span data-stu-id="30fe7-117">_iEnt_</span></span>
  
> <span data-ttu-id="30fe7-118">読み上げで指定されたフォルダーの数を同期\*\* するためのインデックスです。</span><span class="sxs-lookup"><span data-stu-id="30fe7-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="30fe7-119">_fea-cent-logging-service_</span><span class="sxs-lookup"><span data-stu-id="30fe7-119">_cEnt_</span></span>
  
> <span data-ttu-id="30fe7-120">読み上げ同期されていないフォルダーの数。</span><span class="sxs-lookup"><span data-stu-id="30fe7-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30fe7-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="30fe7-121">See also</span></span>

- [<span data-ttu-id="30fe7-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="30fe7-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="30fe7-123">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="30fe7-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="30fe7-124">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="30fe7-124">MAPI Constants</span></span>](mapi-constants.md)

