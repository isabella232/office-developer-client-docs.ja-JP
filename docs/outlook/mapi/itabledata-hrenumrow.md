---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418373"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="a123c-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="a123c-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="a123c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a123c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a123c-105">テーブル内の位置に基づいて行を取得します。</span><span class="sxs-lookup"><span data-stu-id="a123c-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="a123c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a123c-106">Parameters</span></span>

 <span data-ttu-id="a123c-107">_ulrownumber_</span><span class="sxs-lookup"><span data-stu-id="a123c-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="a123c-108">順番プロパティを返す行の番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="a123c-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="a123c-109">_ulrownumber_パラメーターの値には、テーブルの最初の行を示す0から、テーブルの最後の行を示す n-1 までの任意の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a123c-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="a123c-110">_lppsrow_</span><span class="sxs-lookup"><span data-stu-id="a123c-110">_lppSRow_</span></span>
  
> <span data-ttu-id="a123c-111">読み上げ目的の行を記述する[srow](srow.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a123c-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a123c-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="a123c-112">Return value</span></span>

<span data-ttu-id="a123c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a123c-113">S_OK</span></span> 
  
> <span data-ttu-id="a123c-114">行が正常に取得されたか、 _ulrownumber_パラメーターで指定された行番号の行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="a123c-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a123c-115">注釈</span><span class="sxs-lookup"><span data-stu-id="a123c-115">Remarks</span></span>

<span data-ttu-id="a123c-116">**itabledata:: HrEnumRow**メソッドは、連続した番号に基づいて行を取得します。</span><span class="sxs-lookup"><span data-stu-id="a123c-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="a123c-117">この数は、挿入の順序 (0 は最初の行を示し、行数から1を引いた数は最後の行を示します) を表します。</span><span class="sxs-lookup"><span data-stu-id="a123c-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="a123c-118">MAPI では、この順序で行が挿入され、テーブルデータオブジェクトの有効期間が維持されます。</span><span class="sxs-lookup"><span data-stu-id="a123c-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="a123c-119">_ulrownumber_で指定された数値がテーブルの行に対応していない場合、 **HrEnumRow**は S_OK を返し、 _lppsrow_パラメーターを NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="a123c-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="a123c-120">MAPI は、テーブルデータオブジェクトの作成時に[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して、返された**srow**構造のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a123c-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="a123c-121">呼び出し元は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出してこのメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a123c-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="a123c-122">テーブルから挿入された順序で行を取得するには、テーブルデータオブジェクトのユーザーは**HrEnumRow**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a123c-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a123c-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="a123c-123">See also</span></span>



[<span data-ttu-id="a123c-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a123c-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a123c-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a123c-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a123c-126">SRow</span><span class="sxs-lookup"><span data-stu-id="a123c-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="a123c-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a123c-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

