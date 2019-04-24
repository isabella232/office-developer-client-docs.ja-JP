---
title: itabledatahrmodifyrows
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348672"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="e2312-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="e2312-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="e2312-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2312-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2312-105">複数のテーブル行を挿入します。既存の行を置換する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="e2312-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="e2312-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2312-106">Parameters</span></span>

 <span data-ttu-id="e2312-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2312-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e2312-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="e2312-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e2312-109">_lpsrowset_</span><span class="sxs-lookup"><span data-stu-id="e2312-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="e2312-110">順番追加する行のセットを含む[srowset](srowset.md)構造体へのポインター。必要に応じて既存の行を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e2312-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="e2312-111">行セットの各[srow](srow.md)構造の**lpprops**メンバーによって参照されているプロパティ値構造の1つに、インデックス列が含まれている必要があります。これには、 __ [ulPropTagIndexColumn パラメーターで指定したものと同じ値があります。CreateTable](createtable.md)関数。</span><span class="sxs-lookup"><span data-stu-id="e2312-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e2312-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="e2312-112">Return value</span></span>

<span data-ttu-id="e2312-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2312-113">S_OK</span></span> 
  
> <span data-ttu-id="e2312-114">行が正常に挿入または変更されました。</span><span class="sxs-lookup"><span data-stu-id="e2312-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="e2312-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e2312-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="e2312-116">渡された1つ以上の行にインデックス列がありません。</span><span class="sxs-lookup"><span data-stu-id="e2312-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="e2312-117">このエラーが返された場合、行は変更されません。</span><span class="sxs-lookup"><span data-stu-id="e2312-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2312-118">解説</span><span class="sxs-lookup"><span data-stu-id="e2312-118">Remarks</span></span>

<span data-ttu-id="e2312-119">**itabledata:: hrmodifyrows**メソッドは、 _lpsrowset_パラメーターで指定された[srowset](srowset.md)構造によって示される行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="e2312-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="e2312-120">行セットの行のインデックス列の値が、テーブル内の既存の行の値と一致する場合は、既存の行が置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="e2312-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="e2312-121">**srowset**構造に含まれるものに一致する行が存在しない場合、 **hrmodifyrows**はテーブルの末尾に行を追加します。</span><span class="sxs-lookup"><span data-stu-id="e2312-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="e2312-122">テーブルのすべてのビューは、 _lpsrowset_で示される行を含むように変更されます。</span><span class="sxs-lookup"><span data-stu-id="e2312-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="e2312-123">ただし、ビューに行を除外する制限がある場合は、ユーザーに表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="e2312-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="e2312-124">_lpsrowset_で示される行の列は、テーブル内の列と同じ順序である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e2312-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="e2312-125">また、呼び出し元には、現在テーブルにない列のプロパティを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="e2312-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="e2312-126">既存のビューの場合、 **hrmodifyrows**によって、これらの新しい列が使用可能になりますが、現在の列のセットには含まれません。</span><span class="sxs-lookup"><span data-stu-id="e2312-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="e2312-127">今後のビューの場合、 **hrmodifyrows**には列セットの新しい列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e2312-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="e2312-128">**hrmodifyrows**が行を追加すると、テーブルのビューを持つすべてのクライアントまたはサービスプロバイダーに通知が送信され、通知のために登録するためにテーブルの[IMAPITable:: アドバイズ](imapitable-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e2312-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="e2312-129">MAPI は、各行に対して TABLE_ROW_ADDED または TABLE_ROW_MODIFIED の通知を送信します。最大8行。</span><span class="sxs-lookup"><span data-stu-id="e2312-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="e2312-130">**hrmodifyrows**呼び出しの処理に8行を超える行が含まれている場合、MAPI は代わりに1つの TABLE_CHANGED 通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="e2312-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2312-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2312-131">See also</span></span>



[<span data-ttu-id="e2312-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e2312-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="e2312-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2312-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

