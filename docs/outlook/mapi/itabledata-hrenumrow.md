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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6c149a215a048b96408025e08df55972fa989f46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801215"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="5f6e4-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="5f6e4-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="5f6e4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f6e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f6e4-105">テーブル内の位置に基づいて行を取得します。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="5f6e4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5f6e4-106">Parameters</span></span>

 <span data-ttu-id="5f6e4-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="5f6e4-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="5f6e4-108">[in]プロパティを返す対象の行の数です。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="5f6e4-109">_UlRowNumber_パラメーターの値は 0 から n までの 1、テーブルの最後の行を示す、テーブルの最初の行から任意の値にできます。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="5f6e4-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="5f6e4-110">_lppSRow_</span></span>
  
> <span data-ttu-id="5f6e4-111">[out]対象の行を記述する[SRow](srow.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5f6e4-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5f6e4-112">Return value</span></span>

<span data-ttu-id="5f6e4-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f6e4-113">S_OK</span></span> 
  
> <span data-ttu-id="5f6e4-114">行が正常に取得されたか、 _ulRowNumber_パラメーターで指定された行番号の行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5f6e4-115">備考</span><span class="sxs-lookup"><span data-stu-id="5f6e4-115">Remarks</span></span>

<span data-ttu-id="5f6e4-116">**ITableData::HrEnumRow**メソッドは、序数に基づく行を取得します。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="5f6e4-117">この番号は、挿入の順序を表します (最初の行は 0 し、-1 行の数は、最後の行を示します)。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="5f6e4-118">MAPI では、この時系列テーブルのデータ オブジェクトの有効期間の行を挿入の順序を維持します。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="5f6e4-119">番号で指定された_ulRowNumber_は、テーブル内の行には対応していない、 **HrEnumRow**は S_OK を返し、 _lppSRow_パラメーターを NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="5f6e4-120">MAPI では、テーブルのデータ オブジェクトが作成されたときに[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用して、返された**SRow**構造体のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="5f6e4-121">呼び出し元は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって、このメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="5f6e4-122">挿入された順序で、テーブルから行を取得するためには、テーブルのデータ オブジェクトのユーザーは、 **HrEnumRow**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5f6e4-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f6e4-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f6e4-123">See also</span></span>



[<span data-ttu-id="5f6e4-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="5f6e4-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="5f6e4-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5f6e4-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5f6e4-126">SRow</span><span class="sxs-lookup"><span data-stu-id="5f6e4-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="5f6e4-127">ITableData: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f6e4-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

