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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409000"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="16145-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="16145-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="16145-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16145-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16145-105">新しいテーブル行を挿入し、既存の行を置き換える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="16145-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="16145-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="16145-106">Parameters</span></span>

 <span data-ttu-id="16145-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="16145-107">_lpSRow_</span></span>
  
> <span data-ttu-id="16145-108">[in]追加する行または既存の行を置き換える [SRow](srow.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="16145-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="16145-109">**SRow** 構造体の **lpProps** メンバーが指すプロパティ値構造体の 1 つは [、CreateTable](createtable.md)関数の呼び出しで _ulPropTagIndexColumn_ パラメーターで指定されたのと同じ値のインデックス列を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="16145-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="16145-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="16145-110">Return value</span></span>

<span data-ttu-id="16145-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="16145-111">S_OK</span></span> 
  
> <span data-ttu-id="16145-112">行が正常に挿入または変更されました。</span><span class="sxs-lookup"><span data-stu-id="16145-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="16145-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="16145-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="16145-114">渡された行にはインデックス列が含めではありません。</span><span class="sxs-lookup"><span data-stu-id="16145-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16145-115">注釈</span><span class="sxs-lookup"><span data-stu-id="16145-115">Remarks</span></span>

<span data-ttu-id="16145-116">**ITableData::HrModifyRow** メソッドは _、lpSRow_ パラメーターが指す **SRow** 構造で記述された行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="16145-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="16145-117">インデックス列の値が  _lpSRow_ が示す行と同じ値を持つ行がテーブルに既に存在する場合、既存の行が置き換えられる。</span><span class="sxs-lookup"><span data-stu-id="16145-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="16145-118">**SRow** 構造に含まれる行と一致する行が存在しない場合 **、HrModifyRow** は行をテーブルの末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="16145-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="16145-119">テーブルのすべてのビューが変更され  _、lpSRow_ が指す行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="16145-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="16145-120">ただし、ビューに行を除外する制限がある場合は、ユーザーに表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="16145-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="16145-121">_lpSRow_ が指す行の列は、テーブル内の列と同じ順序である必要があります。</span><span class="sxs-lookup"><span data-stu-id="16145-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="16145-122">呼び出し元は、現在テーブルに含めされていない列プロパティとして含めすることもできます。</span><span class="sxs-lookup"><span data-stu-id="16145-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="16145-123">既存のビューの **場合、HrModifyRow** は新しい列を使用できますが、現在の列セットには含められません。</span><span class="sxs-lookup"><span data-stu-id="16145-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="16145-124">今後のビューでは **、HrModifyRow には** 列セットに新しい列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="16145-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="16145-125">**HrModifyRow** が行を追加すると、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出して通知を登録しているすべてのクライアントまたはサービス プロバイダーに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="16145-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16145-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="16145-126">See also</span></span>



[<span data-ttu-id="16145-127">SRow</span><span class="sxs-lookup"><span data-stu-id="16145-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="16145-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="16145-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="16145-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16145-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

