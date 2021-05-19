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
# <a name="itabledatahrenumrow"></a><span data-ttu-id="1835a-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="1835a-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="1835a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1835a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1835a-105">テーブル内の位置に基づいて行を取得します。</span><span class="sxs-lookup"><span data-stu-id="1835a-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="1835a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1835a-106">Parameters</span></span>

 <span data-ttu-id="1835a-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="1835a-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="1835a-108">[in]プロパティを返す行の数。</span><span class="sxs-lookup"><span data-stu-id="1835a-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="1835a-109">_ulRowNumber_ パラメーターの値には、表の最初の行を示す 0 から、表の最後の行を示す n ~ 1 の任意の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1835a-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="1835a-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="1835a-110">_lppSRow_</span></span>
  
> <span data-ttu-id="1835a-111">[out]ターゲット行を表す [SRow](srow.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1835a-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1835a-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="1835a-112">Return value</span></span>

<span data-ttu-id="1835a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1835a-113">S_OK</span></span> 
  
> <span data-ttu-id="1835a-114">行が正常に取得されたか  _、ulRowNumber_ パラメーターで指定された行番号の行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="1835a-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1835a-115">注釈</span><span class="sxs-lookup"><span data-stu-id="1835a-115">Remarks</span></span>

<span data-ttu-id="1835a-116">**ITableData::HrEnumRow** メソッドは、順次番号に基づいて行を取得します。</span><span class="sxs-lookup"><span data-stu-id="1835a-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="1835a-117">この数値は、挿入の順序を表します (0 は最初の行を示し、行数から 1 を引いた数は最後の行を示します)。</span><span class="sxs-lookup"><span data-stu-id="1835a-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="1835a-118">MAPI は、テーブル データ オブジェクトの有効期間の間、行の挿入のこの時系列の順序を維持します。</span><span class="sxs-lookup"><span data-stu-id="1835a-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="1835a-119">_ulRowNumber_ で指定された番号がテーブル内の行に対応していない場合 **、HrEnumRow** は S_OK を返し _、lppSRow_ パラメーターを NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="1835a-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="1835a-120">MAPI は、テーブル データ オブジェクトの作成時に [MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して、返される **SRow** 構造体のメモリを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="1835a-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="1835a-121">呼び出し元は [、MAPIFreeBuffer 関数を呼び出して、このメモリを解放する必要](mapifreebuffer.md) があります。</span><span class="sxs-lookup"><span data-stu-id="1835a-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="1835a-122">テーブルから挿入された順序で行を取得するには、テーブル データ オブジェクトのユーザーが **HrEnumRow メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="1835a-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1835a-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="1835a-123">See also</span></span>



[<span data-ttu-id="1835a-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1835a-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="1835a-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1835a-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1835a-126">SRow</span><span class="sxs-lookup"><span data-stu-id="1835a-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="1835a-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1835a-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

