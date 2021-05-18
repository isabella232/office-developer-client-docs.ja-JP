---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405360"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="59251-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="59251-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="59251-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59251-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59251-105">複数のテーブル行を挿入し、既存の行を置き換える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="59251-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="59251-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="59251-106">Parameters</span></span>

 <span data-ttu-id="59251-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="59251-107">_ulFlags_</span></span>
  
> <span data-ttu-id="59251-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="59251-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="59251-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="59251-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="59251-110">[in]追加する行のセットを含む [SRowSet](srowset.md) 構造体へのポインターで、必要に応じて既存の行を置き換える。</span><span class="sxs-lookup"><span data-stu-id="59251-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="59251-111">行セット内の [各 SRow](srow.md)構造体の **lpProps** メンバーが指すプロパティ値構造の 1 つには [、CreateTable](createtable.md)関数の呼び出しで _ulPropTagIndexColumn_ パラメーターで指定されたのと同じインデックス列が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="59251-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="59251-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="59251-112">Return value</span></span>

<span data-ttu-id="59251-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="59251-113">S_OK</span></span> 
  
> <span data-ttu-id="59251-114">行が正常に挿入または変更されました。</span><span class="sxs-lookup"><span data-stu-id="59251-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="59251-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="59251-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="59251-116">1 つ以上の渡された行にインデックス列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="59251-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="59251-117">このエラーが返された場合、行は変更されません。</span><span class="sxs-lookup"><span data-stu-id="59251-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59251-118">注釈</span><span class="sxs-lookup"><span data-stu-id="59251-118">Remarks</span></span>

<span data-ttu-id="59251-119">**ITableData::HrModifyRows** メソッドは _、lpSRowSet_ パラメーターが指す [SRowSet](srowset.md)構造体で記述された行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="59251-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="59251-120">行セット内の行のインデックス列の値がテーブル内の既存の行の値と一致する場合は、既存の行が置き換えられる。</span><span class="sxs-lookup"><span data-stu-id="59251-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="59251-121">**SRowSet** 構造体に含まれる行と一致する行が存在しない場合 **、HrModifyRows** は行をテーブルの末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="59251-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="59251-122">テーブルのすべてのビューは  _、lpSRowSet_ が指す行を含む変更を行います。</span><span class="sxs-lookup"><span data-stu-id="59251-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="59251-123">ただし、ビューに行を除外する制限がある場合は、ユーザーに表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="59251-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="59251-124">_lpSRowSet_ が指す行の列は、テーブル内の列と同じ順序である必要があります。</span><span class="sxs-lookup"><span data-stu-id="59251-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="59251-125">呼び出し元は、現在テーブルに含めされていない列プロパティとして含めすることもできます。</span><span class="sxs-lookup"><span data-stu-id="59251-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="59251-126">既存のビューの **場合、HrModifyRows** は、これらの新しい列を使用できますが、現在の列セットには含められません。</span><span class="sxs-lookup"><span data-stu-id="59251-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="59251-127">今後のビューでは **、HrModifyRows には** 列セットに新しい列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="59251-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="59251-128">**HrModifyRows** が行を追加すると、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出して通知を登録しているすべてのクライアントまたはサービス プロバイダーに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="59251-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="59251-129">MAPI は、TABLE_ROW_ADDED行TABLE_ROW_MODIFIED、最大 8 行の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="59251-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="59251-130">8 行以上が **HrModifyRows** 呼び出しの影響を受ける場合、MAPI は代わりに 1 つのTABLE_CHANGED送信します。</span><span class="sxs-lookup"><span data-stu-id="59251-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59251-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="59251-131">See also</span></span>



[<span data-ttu-id="59251-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="59251-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="59251-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="59251-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

