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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 06356d60b43d7e5be61d944c07001570bdd5c678
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571109"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="1c308-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="1c308-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="1c308-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c308-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c308-105">既存の行が上書きされる、複数のテーブル行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="1c308-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="1c308-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="1c308-106">Parameters</span></span>

 <span data-ttu-id="1c308-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1c308-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1c308-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="1c308-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1c308-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="1c308-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="1c308-110">[in][SRowSet](srowset.md)構造体へのポインターを含む一連の行を追加するには、必要に応じて既存の行を置き換えることです。</span><span class="sxs-lookup"><span data-stu-id="1c308-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="1c308-111">値構造体のプロパティでは、 **lpProps**各[SRow](srow.md)構造体のメンバーの行に設定するポイントの 1 つのインデックス列で、[への呼び出し内の_ulPropTagIndexColumn_パラメーターで指定された値と同じ値を含める必要があります。CreateTable](createtable.md)関数です。</span><span class="sxs-lookup"><span data-stu-id="1c308-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1c308-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1c308-112">Return value</span></span>

<span data-ttu-id="1c308-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c308-113">S_OK</span></span> 
  
> <span data-ttu-id="1c308-114">行が挿入または変更されました。</span><span class="sxs-lookup"><span data-stu-id="1c308-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="1c308-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1c308-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="1c308-116">渡された行の 1 つ以上には、インデックス列がありません。</span><span class="sxs-lookup"><span data-stu-id="1c308-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="1c308-117">このエラーが返された場合、行は変更されません。</span><span class="sxs-lookup"><span data-stu-id="1c308-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1c308-118">注釈</span><span class="sxs-lookup"><span data-stu-id="1c308-118">Remarks</span></span>

<span data-ttu-id="1c308-119">**ITableData::HrModifyRows**メソッドは、 _lpSRowSet_パラメーターが指す[SRowSet](srowset.md)構造体によって記述された行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="1c308-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="1c308-120">行セット内の行のインデックス列の値には、テーブル内の既存の行の値が一致すると、既存の行が置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="1c308-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="1c308-121">行が存在しない場合**SRowSet**構造体に含まれる 1 つに一致する、 **HrModifyRows**は、テーブルの末尾に行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1c308-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="1c308-122">_LpSRowSet_で指定された行を含むテーブルのすべてのビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="1c308-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="1c308-123">ただし場合は、ビューでは、行が除外されるように制限がある、ある可能性がありますいないユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="1c308-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="1c308-124">_LpSRowSet_で指定された行の列をテーブル内の列と同じ順序にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1c308-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="1c308-125">呼び出し元は、現在のテーブルに存在しない列のプロパティとしても指定できます。</span><span class="sxs-lookup"><span data-stu-id="1c308-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="1c308-126">既存のビューの**HrModifyRows**これらの新しい列を使用できるようですが、現在の列セットには含まれません。</span><span class="sxs-lookup"><span data-stu-id="1c308-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="1c308-127">将来のビューでは、 **HrModifyRows**には、列セットの新しい列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1c308-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="1c308-128">**HrModifyRows**が行を追加すると、すべてのクライアントやテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが、サービス プロバイダーに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="1c308-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="1c308-129">MAPI では、8 行まで、行ごとに、TABLE_ROW_ADDED または TABLE_ROW_MODIFIED の通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="1c308-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="1c308-130">8 つ以上の行が影響を受ける場合、 **HrModifyRows**呼び出しによって MAPI 通知を送信する 1 つ TABLE_CHANGED 代わりにします。</span><span class="sxs-lookup"><span data-stu-id="1c308-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1c308-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c308-131">See also</span></span>



[<span data-ttu-id="1c308-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="1c308-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="1c308-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1c308-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

