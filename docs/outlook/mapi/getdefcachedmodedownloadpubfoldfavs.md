---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417708"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="91d8c-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="91d8c-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="91d8c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91d8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91d8c-105">パブリック フォルダーのお気に入りフォルダーのExchange キャッシュ モードを有効にするかどうか、およびこれがポリシーによって適用されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="91d8c-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="91d8c-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="91d8c-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91d8c-107">次の方法でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="91d8c-107">Exported by:</span></span>  <br/> |<span data-ttu-id="91d8c-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="91d8c-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="91d8c-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="91d8c-109">Called by:</span></span>  <br/> |<span data-ttu-id="91d8c-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="91d8c-110">Client</span></span>  <br/> |
|<span data-ttu-id="91d8c-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="91d8c-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="91d8c-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="91d8c-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="91d8c-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="91d8c-113">Parameters</span></span>

 <span data-ttu-id="91d8c-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="91d8c-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="91d8c-115">[out] **戻** り値がポリシーによって適用される場合は **true、適用** されていない場合は false。</span><span class="sxs-lookup"><span data-stu-id="91d8c-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="91d8c-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="91d8c-116">Return values</span></span>

 <span data-ttu-id="91d8c-117">**true**</span><span class="sxs-lookup"><span data-stu-id="91d8c-117">**true**</span></span>
  
- <span data-ttu-id="91d8c-118">キャッシュが有効です。</span><span class="sxs-lookup"><span data-stu-id="91d8c-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="91d8c-119">**false**</span><span class="sxs-lookup"><span data-stu-id="91d8c-119">**false**</span></span>
  
- <span data-ttu-id="91d8c-120">キャッシュは無効です。</span><span class="sxs-lookup"><span data-stu-id="91d8c-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91d8c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="91d8c-121">See also</span></span>



[<span data-ttu-id="91d8c-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="91d8c-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

