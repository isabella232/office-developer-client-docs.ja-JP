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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800040"
---
# <a name="fbadrestriction"></a><span data-ttu-id="2e6c7-103">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="2e6c7-103">FBadRestriction</span></span>

  
  
<span data-ttu-id="2e6c7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e6c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e6c7-105">テーブルのビューを制限するために使用制限を検証します。</span><span class="sxs-lookup"><span data-stu-id="2e6c7-105">Validates a restriction used to limit a table view.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e6c7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2e6c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="2e6c7-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2e6c7-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2e6c7-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2e6c7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2e6c7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2e6c7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2e6c7-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2e6c7-110">Called by:</span></span>  <br/> |<span data-ttu-id="2e6c7-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2e6c7-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a><span data-ttu-id="2e6c7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2e6c7-112">Parameters</span></span>

 <span data-ttu-id="2e6c7-113">_lpres_</span><span class="sxs-lookup"><span data-stu-id="2e6c7-113">_lpres_</span></span>
  
> <span data-ttu-id="2e6c7-114">[in]検証する制限を定義する[SRestriction](srestriction.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="2e6c7-114">[in] An [SRestriction](srestriction.md) structure defining the restriction to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2e6c7-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="2e6c7-115">Return value</span></span>

<span data-ttu-id="2e6c7-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="2e6c7-116">TRUE</span></span> 
  
> <span data-ttu-id="2e6c7-117">指定した制限、または 1 つ以上の subrestrictions では、が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="2e6c7-117">The specified restriction, or one or more of its subrestrictions, is invalid.</span></span> 
    
<span data-ttu-id="2e6c7-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="2e6c7-118">FALSE</span></span> 
  
> <span data-ttu-id="2e6c7-119">指定された制限とそのすべての subrestrictions は、有効です。</span><span class="sxs-lookup"><span data-stu-id="2e6c7-119">The specified restriction and all its subrestrictions are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e6c7-120">注釈</span><span class="sxs-lookup"><span data-stu-id="2e6c7-120">Remarks</span></span>

<span data-ttu-id="2e6c7-121">制限を確認すると、特定の行、テーブルの行を検索する[IMAPITable::FindRow](imapitable-findrow.md)メソッドおよび[IMAPIContainer](imapicontainerimapiprop.md)のメソッドは、テーブルを制限するのには、 [IMAPITable::Restrict](imapitable-restrict.md)メソッドの呼び出しで渡すことができます。コンテナー オブジェクトの制限を実行するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="2e6c7-121">Once a restriction is validated, it can be passed in calls to the [IMAPITable::Restrict](imapitable-restrict.md) method to restrict the table to certain rows, to the [IMAPITable::FindRow](imapitable-findrow.md) method to locate a table row, and to methods of the [IMAPIContainer](imapicontainerimapiprop.md) interface to perform a restriction on a container object.</span></span> 
  

