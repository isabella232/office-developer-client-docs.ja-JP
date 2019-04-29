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
# <a name="fbadrestriction"></a><span data-ttu-id="b4bbd-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="b4bbd-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="b4bbd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4bbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4bbd-105">テーブルビューの制限に使用される制限を検証します。</span><span class="sxs-lookup"><span data-stu-id="b4bbd-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4bbd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b4bbd-106">Header file:</span></span>  <br/> |<span data-ttu-id="b4bbd-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b4bbd-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b4bbd-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="b4bbd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b4bbd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b4bbd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b4bbd-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b4bbd-110">Called by:</span></span>  <br/> |<span data-ttu-id="b4bbd-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b4bbd-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="b4bbd-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b4bbd-112">Parameters</span></span>

 <span data-ttu-id="b4bbd-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="b4bbd-113">_lpres_</span></span>
  
> <span data-ttu-id="b4bbd-114">順番検証する制限を定義する[srestriction](srestriction.md)構造。</span><span class="sxs-lookup"><span data-stu-id="b4bbd-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b4bbd-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="b4bbd-115">Return value</span></span>

<span data-ttu-id="b4bbd-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="b4bbd-116">TRUE</span></span> 
  
> <span data-ttu-id="b4bbd-117">指定した制限または1つ以上のサブ制限が無効です。</span><span class="sxs-lookup"><span data-stu-id="b4bbd-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="b4bbd-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="b4bbd-118">FALSE</span></span> 
  
> <span data-ttu-id="b4bbd-119">指定した制限とそのすべてのサブ制限が有効である。</span><span class="sxs-lookup"><span data-stu-id="b4bbd-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b4bbd-120">注釈</span><span class="sxs-lookup"><span data-stu-id="b4bbd-120">Remarks</span></span>

<span data-ttu-id="b4bbd-121">制限が検証されたら、 [imapitable:: Restrict](imapitable-restrict.md)メソッドへの呼び出しで、テーブルを特定の行に制限したり、 [imapitable:: FindRow](imapitable-findrow.md)メソッドを使用してテーブルの行を検索したり、 [IMAPIContainer](imapicontainerimapiprop.md)のメソッドに渡したりすることができます。container オブジェクトに対する制限を実行するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="b4bbd-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

