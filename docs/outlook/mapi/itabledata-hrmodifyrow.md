---
title: ITableDataHrModifyRow
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5ef210aedc884e5c09eca6335199e2ef284b901c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574833"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="b37b3-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="b37b3-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="b37b3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b37b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b37b3-105">既存の行が上書きされる、テーブルの新しい行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="b37b3-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="b37b3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b37b3-106">Parameters</span></span>

 <span data-ttu-id="b37b3-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="b37b3-107">_lpSRow_</span></span>
  
> <span data-ttu-id="b37b3-108">[in]行を追加する既存の行を置換するかを説明する[SRow](srow.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b37b3-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="b37b3-109">CreateTable の[への呼び出し内の_ulPropTagIndexColumn_パラメーターで指定された値と同じ値であるインデックス列が含まれている必要があります、 **lpProps** 、 **SRow**構造体のメンバーで指定されたプロパティ値の構造体のいずれか](createtable.md)関数です。</span><span class="sxs-lookup"><span data-stu-id="b37b3-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b37b3-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b37b3-110">Return value</span></span>

<span data-ttu-id="b37b3-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b37b3-111">S_OK</span></span> 
  
> <span data-ttu-id="b37b3-112">行を挿入または変更に成功しました。</span><span class="sxs-lookup"><span data-stu-id="b37b3-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="b37b3-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b37b3-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b37b3-114">渡された行には、インデックス列がありません。</span><span class="sxs-lookup"><span data-stu-id="b37b3-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b37b3-115">注釈</span><span class="sxs-lookup"><span data-stu-id="b37b3-115">Remarks</span></span>

<span data-ttu-id="b37b3-116">**ITableData::HrModifyRow**メソッドは、 _lpSRow_パラメーターが指す**SRow**の構造体によって記述された行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="b37b3-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="b37b3-117">テーブル内に既に存在する場合は、その_lpSRow_ポイントの行とそのインデックス列に対して同じ値を持つ行を既存の行が置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="b37b3-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="b37b3-118">行が存在しない場合、 **SRow**構造体に含まれる 1 つに一致する、 **HrModifyRow**は、テーブルの末尾に行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b37b3-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="b37b3-119">テーブルのすべてのビューは、 _lpSRow_で指定された行を含むように変更されます。</span><span class="sxs-lookup"><span data-stu-id="b37b3-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="b37b3-120">ただし場合は、ビューでは、行が除外されるように制限がある、ある可能性がありますいないユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="b37b3-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="b37b3-121">_LpSRow_で指定された行の列をテーブル内の列と同じ順序にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b37b3-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="b37b3-122">呼び出し元は、現在のテーブルに存在しない列のプロパティとしても指定できます。</span><span class="sxs-lookup"><span data-stu-id="b37b3-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="b37b3-123">既存のビューの**HrModifyRow**これらの新しい列を使用できるようですが、現在の列セットには含まれません。</span><span class="sxs-lookup"><span data-stu-id="b37b3-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="b37b3-124">将来のビューでは、 **HrModifyRow**には、列セットの新しい列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b37b3-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="b37b3-125">**HrModifyRow**は、行を追加した後にすべてのクライアントまたはサービス プロバイダーのテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="b37b3-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b37b3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="b37b3-126">See also</span></span>



[<span data-ttu-id="b37b3-127">SRow</span><span class="sxs-lookup"><span data-stu-id="b37b3-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="b37b3-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b37b3-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="b37b3-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b37b3-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

