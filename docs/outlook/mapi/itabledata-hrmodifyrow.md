---
title: itabledatahrmodifyrow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348665"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="c935d-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="c935d-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="c935d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c935d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c935d-105">既存の行を置き換える可能性がある新しいテーブル行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="c935d-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="c935d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c935d-106">Parameters</span></span>

 <span data-ttu-id="c935d-107">_lpsrow_</span><span class="sxs-lookup"><span data-stu-id="c935d-107">_lpSRow_</span></span>
  
> <span data-ttu-id="c935d-108">順番追加する行を記述する[srow](srow.md)構造体へのポインター、または既存の行を置換するためのポインター。</span><span class="sxs-lookup"><span data-stu-id="c935d-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="c935d-109">**srow**構造の**lpprops**メンバーによって参照されるプロパティ値構造の1つに、インデックス列、CreateTable への呼び出しで_ulPropTagIndexColumn_パラメーターで指定したものと同じ値が含まれている必要があります。 [](createtable.md)関数。</span><span class="sxs-lookup"><span data-stu-id="c935d-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c935d-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="c935d-110">Return value</span></span>

<span data-ttu-id="c935d-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c935d-111">S_OK</span></span> 
  
> <span data-ttu-id="c935d-112">行が正常に挿入または変更されました。</span><span class="sxs-lookup"><span data-stu-id="c935d-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="c935d-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c935d-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c935d-114">渡された行にインデックス列がありません。</span><span class="sxs-lookup"><span data-stu-id="c935d-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c935d-115">解説</span><span class="sxs-lookup"><span data-stu-id="c935d-115">Remarks</span></span>

<span data-ttu-id="c935d-116">**itabledata:: hrmodifyrow**メソッドは、 _lpsrow_パラメーターで指定された**srow**構造によって示される行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="c935d-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="c935d-117">テーブル内に既に存在する_lpsrow_と同じ値のインデックス列の行がある場合、既存の行は置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="c935d-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="c935d-118">**srow**構造に含まれるものと一致する行が存在しない場合、 **hrmodifyrow**はテーブルの末尾に行を追加します。</span><span class="sxs-lookup"><span data-stu-id="c935d-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="c935d-119">テーブルのすべてのビューが変更され、 _lpsrow_によって示される行が含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="c935d-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="c935d-120">ただし、その行を除外する制限がビューにある場合は、ユーザーに表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="c935d-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="c935d-121">_lpsrow_によって参照される行の列は、テーブル内の列と同じ順序である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c935d-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="c935d-122">また、呼び出し元には、現在テーブルにない列のプロパティを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="c935d-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="c935d-123">既存のビューの場合、 **hrmodifyrow**によって、これらの新しい列が使用可能になりますが、現在の列のセットには含まれません。</span><span class="sxs-lookup"><span data-stu-id="c935d-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="c935d-124">今後のビューの場合、 **hrmodifyrow**には列セットの新しい列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c935d-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="c935d-125">**hrmodifyrow**が行を追加すると、テーブルのビューを持つすべてのクライアントまたはサービスプロバイダーに通知が送信され、通知を登録するためにテーブルの[IMAPITable:: Advise](imapitable-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c935d-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c935d-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="c935d-126">See also</span></span>



[<span data-ttu-id="c935d-127">SRow</span><span class="sxs-lookup"><span data-stu-id="c935d-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="c935d-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c935d-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="c935d-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c935d-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

