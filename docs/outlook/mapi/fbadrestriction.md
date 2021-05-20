---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432241"
---
# <a name="fbadrestriction"></a><span data-ttu-id="48b89-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="48b89-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="48b89-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48b89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48b89-105">テーブル ビューを制限するために使用される制限を検証します。</span><span class="sxs-lookup"><span data-stu-id="48b89-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48b89-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="48b89-106">Header file:</span></span>  <br/> |<span data-ttu-id="48b89-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="48b89-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="48b89-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="48b89-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="48b89-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="48b89-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="48b89-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="48b89-110">Called by:</span></span>  <br/> |<span data-ttu-id="48b89-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="48b89-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="48b89-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="48b89-112">Parameters</span></span>

 <span data-ttu-id="48b89-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="48b89-113">_lpres_</span></span>
  
> <span data-ttu-id="48b89-114">[in]検証 [する制限を定義する SRestriction](srestriction.md) 構造。</span><span class="sxs-lookup"><span data-stu-id="48b89-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48b89-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="48b89-115">Return value</span></span>

<span data-ttu-id="48b89-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="48b89-116">TRUE</span></span> 
  
> <span data-ttu-id="48b89-117">指定された制限、または 1 つ以上のサブ制限が無効です。</span><span class="sxs-lookup"><span data-stu-id="48b89-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="48b89-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="48b89-118">FALSE</span></span> 
  
> <span data-ttu-id="48b89-119">指定された制限とそのすべてのサブ制限が有効です。</span><span class="sxs-lookup"><span data-stu-id="48b89-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48b89-120">注釈</span><span class="sxs-lookup"><span data-stu-id="48b89-120">Remarks</span></span>

<span data-ttu-id="48b89-121">制限が検証された後 [、IMAPITable::Restrict](imapitable-restrict.md) メソッドへの呼び出しで渡して、テーブルを特定の行に制限し [、IMAPITable::FindRow](imapitable-findrow.md) メソッドでテーブル行を検索し [、IMAPIContainer](imapicontainerimapiprop.md) インターフェイスのメソッドに渡してコンテナー オブジェクトに対する制限を実行できます。</span><span class="sxs-lookup"><span data-stu-id="48b89-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

