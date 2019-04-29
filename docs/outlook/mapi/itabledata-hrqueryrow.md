---
title: itabledatahrqueryrow
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: da41fadc9a71a410dd115e28ce2cf9c81442b104
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434768"
---
# <a name="itabledatahrqueryrow"></a><span data-ttu-id="15b99-103">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="15b99-103">ITableData::HrQueryRow</span></span>

  
  
<span data-ttu-id="15b99-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15b99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15b99-105">表の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="15b99-105">Retrieves a table row.</span></span>
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a><span data-ttu-id="15b99-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="15b99-106">Parameters</span></span>

 <span data-ttu-id="15b99-107">_lpspropvalue_</span><span class="sxs-lookup"><span data-stu-id="15b99-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="15b99-108">順番取得する行のインデックス列を記述するプロパティ値構造へのポインター。</span><span class="sxs-lookup"><span data-stu-id="15b99-108">[in] A pointer to a property value structure that describes the index column for the row to be retrieved.</span></span> <span data-ttu-id="15b99-109">プロパティ値構造の**ulPropTag**メンバーには、 _ulPropTagIndexColumn_パラメーターと同じプロパティタグが含まれている必要があります。この関数は、 [itabledata](itabledataiunknown.md)実装にアクセスする[CreateTable](createtable.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="15b99-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function, which accesses the [ITableData](itabledataiunknown.md) implementation.</span></span> 
    
 <span data-ttu-id="15b99-110">_lppsrow_</span><span class="sxs-lookup"><span data-stu-id="15b99-110">_lppSRow_</span></span>
  
> <span data-ttu-id="15b99-111">読み上げ取得した行へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="15b99-111">[out] A pointer to a pointer to the retrieved row.</span></span> 
    
 <span data-ttu-id="15b99-112">_lpulirow_</span><span class="sxs-lookup"><span data-stu-id="15b99-112">_lpuliRow_</span></span>
  
> <span data-ttu-id="15b99-113">[入力]入力時に、有効なポインターまたは NULL を返します。これは、返される情報がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="15b99-113">[in, out] On input, a valid pointer or NULL, which indicates that no information needs to be returned.</span></span> <span data-ttu-id="15b99-114">出力では、行の行番号をポイントする有効なポインターは、テーブル内の行の位置を識別する連続した番号です。</span><span class="sxs-lookup"><span data-stu-id="15b99-114">On output, a valid pointer that points to the row's row number, a sequential number that identifies the row's position in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="15b99-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="15b99-115">Return value</span></span>

<span data-ttu-id="15b99-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="15b99-116">S_OK</span></span> 
  
> <span data-ttu-id="15b99-117">行が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="15b99-117">The row was successfully retrieved.</span></span>
    
<span data-ttu-id="15b99-118">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="15b99-118">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="15b99-119">_lpspropvalue_がポイントする[spropvalue](spropvalue.md)構造に、インデックス列プロパティが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="15b99-119">The [SPropValue](spropvalue.md) structure that  _lpSPropValue_ points to does not contain the index column property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="15b99-120">注釈</span><span class="sxs-lookup"><span data-stu-id="15b99-120">Remarks</span></span>

<span data-ttu-id="15b99-121">**itabledata:: hrqueryrow**メソッドは、 _lpspropvalue_が指すプロパティ構造に含まれるインデックス列の値に一致するインデックス列を持つ行のすべてのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="15b99-121">The **ITableData::HrQueryRow** method retrieves all of the properties for the row that has an index column that matches the value of the index column included in the property structure pointed to by  _lpSPropValue_.</span></span> <span data-ttu-id="15b99-122">\*\*\*\* また、呼び出し元が要求した場合、テーブル内の行の位置を示す行番号も返します。</span><span class="sxs-lookup"><span data-stu-id="15b99-122">**HrQueryRow** also returns the row number, if the caller requests it, that identifies the row's position in the table.</span></span> 
  
<span data-ttu-id="15b99-123">**hrqueryrow**は、 _lpspropvalue_によって示される**spropvalue**構造体を変更しないので、 **hrqueryrow**が戻るときには、呼び出し元は構造を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15b99-123">Because **HrQueryRow** does not modify the **SPropValue** structure pointed to by  _lpSPropValue_, callers must free the structure when **HrQueryRow** returns.</span></span> <span data-ttu-id="15b99-124">呼び出し元は、取得した行を含む**srow**構造も解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15b99-124">Callers must also free the **SRow** structure that contains the retrieved row.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15b99-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="15b99-125">See also</span></span>



[<span data-ttu-id="15b99-126">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="15b99-126">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="15b99-127">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="15b99-127">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="15b99-128">SPropValue</span><span class="sxs-lookup"><span data-stu-id="15b99-128">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="15b99-129">SRow</span><span class="sxs-lookup"><span data-stu-id="15b99-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="15b99-130">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15b99-130">ITableData : IUnknown</span></span>](itabledataiunknown.md)

