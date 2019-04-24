---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341007"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="5c4c1-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="5c4c1-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="5c4c1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c4c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c4c1-105">次に[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出したときに、サービスプロバイダーによって使用されるように設定されたテーブル列セットの有効性をテストします。</span><span class="sxs-lookup"><span data-stu-id="5c4c1-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c4c1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5c4c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c4c1-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="5c4c1-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="5c4c1-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="5c4c1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5c4c1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5c4c1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5c4c1-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5c4c1-110">Called by:</span></span>  <br/> |<span data-ttu-id="5c4c1-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="5c4c1-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="5c4c1-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5c4c1-112">Parameters</span></span>

 <span data-ttu-id="5c4c1-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="5c4c1-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="5c4c1-114">順番検証するテーブル列を定義するプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c4c1-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5c4c1-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="5c4c1-115">Return value</span></span>

<span data-ttu-id="5c4c1-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="5c4c1-116">TRUE</span></span> 
  
> <span data-ttu-id="5c4c1-117">指定した列セットが無効です。</span><span class="sxs-lookup"><span data-stu-id="5c4c1-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="5c4c1-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="5c4c1-118">FALSE</span></span> 
  
> <span data-ttu-id="5c4c1-119">指定した列セットは有効です。</span><span class="sxs-lookup"><span data-stu-id="5c4c1-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5c4c1-120">解説</span><span class="sxs-lookup"><span data-stu-id="5c4c1-120">Remarks</span></span>

<span data-ttu-id="5c4c1-121">**FBadColumnSet**関数は、PT_ERROR 型の列を無効として扱い、PT_NULL 型の列を有効なものとして処理します。</span><span class="sxs-lookup"><span data-stu-id="5c4c1-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

