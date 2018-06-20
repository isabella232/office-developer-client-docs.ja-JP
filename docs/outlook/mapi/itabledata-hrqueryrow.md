---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 92540159386e6f37d93684aff037b235071010f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801231"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="73d3f-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="73d3f-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="73d3f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73d3f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73d3f-105">テーブルの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="73d3f-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="73d3f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="73d3f-106">Parameters</span></span>

 <span data-ttu-id="73d3f-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="73d3f-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="73d3f-108">[in]取得する行のインデックス列を説明するプロパティ値の構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="73d3f-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="73d3f-109">プロパティ値の構造体の**ulPropTag**メンバーは、 [ITableData](itabledataiunknown.md)の実装にアクセスする、 [CreateTable](createtable.md)関数への呼び出しの_ulPropTagIndexColumn_パラメーターと同じプロパティ タグを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="73d3f-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="73d3f-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="73d3f-110">_lppSRow_</span></span>
  
> <span data-ttu-id="73d3f-111">[out]取得した行へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="73d3f-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="73d3f-112">_lpuliRow_</span><span class="sxs-lookup"><span data-stu-id="73d3f-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="73d3f-113">[で [チェック アウト]入力、有効なポインターまたは NULL の場合は、返される情報が必要がないことをことを示します。</span><span class="sxs-lookup"><span data-stu-id="73d3f-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="73d3f-114">出力では、有効なポインターを指す行の行番号、テーブル内の行の位置を示す序数。</span><span class="sxs-lookup"><span data-stu-id="73d3f-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73d3f-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="73d3f-115">Return value</span></span>

<span data-ttu-id="73d3f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="73d3f-116">S_OK</span></span> 
  
> <span data-ttu-id="73d3f-117">行が正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="73d3f-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="73d3f-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="73d3f-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="73d3f-119">[SPropValue](spropvalue.md)構造をその_lpSPropValue_が指すインデックス列のプロパティが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="73d3f-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="73d3f-120">備考</span><span class="sxs-lookup"><span data-stu-id="73d3f-120">Remarks</span></span>

<span data-ttu-id="73d3f-121">**ITableData::HrQueryRow**メソッドは、すべての_lpSPropValue_が指すプロパティの構造体に含まれているインデックス列の値に一致するインデックス列を持つ行のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="73d3f-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="73d3f-122">**HrQueryRow**は、呼び出し元が要求した場合、テーブル内の行の位置を識別するにも、行番号を返します。</span><span class="sxs-lookup"><span data-stu-id="73d3f-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="73d3f-123">**HrQueryRow**は、 _lpSPropValue_が指す**SPropValue**構造体を変更しません、ため呼び出し元は、 **HrQueryRow**が返されるときに構造体を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73d3f-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="73d3f-124">呼び出し元では、取得した行を格納する**SRow**構造体を解放する必要がありますも。</span><span class="sxs-lookup"><span data-stu-id="73d3f-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73d3f-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="73d3f-125">See also</span></span>



[<span data-ttu-id="73d3f-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="73d3f-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="73d3f-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="73d3f-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="73d3f-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="73d3f-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="73d3f-129">SRow</span><span class="sxs-lookup"><span data-stu-id="73d3f-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="73d3f-130">ITableData: IUnknown</span><span class="sxs-lookup"><span data-stu-id="73d3f-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

