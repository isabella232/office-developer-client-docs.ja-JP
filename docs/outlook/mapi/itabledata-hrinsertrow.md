---
title: 挿入行
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435440"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="60df0-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="60df0-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="60df0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60df0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60df0-105">表の行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="60df0-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="60df0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="60df0-106">Parameters</span></span>

 <span data-ttu-id="60df0-107">_ウリロウ_</span><span class="sxs-lookup"><span data-stu-id="60df0-107">_uliRow_</span></span>
  
> <span data-ttu-id="60df0-108">[in]特定の行を表す連続行番号。</span><span class="sxs-lookup"><span data-stu-id="60df0-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="60df0-109">新しい行は、番号が示す行の後に配置されます。</span><span class="sxs-lookup"><span data-stu-id="60df0-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="60df0-110">_uliRow_ パラメーターには、0 から n までの行番号を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="60df0-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="60df0-111">_uliRow_ で n を渡すと、行はテーブルの末尾に追加されます。</span><span class="sxs-lookup"><span data-stu-id="60df0-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="60df0-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="60df0-112">_lpSRow_</span></span>
  
> <span data-ttu-id="60df0-113">[in]挿入する行を記述する [SRow](srow.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="60df0-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="60df0-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="60df0-114">Return value</span></span>

<span data-ttu-id="60df0-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="60df0-115">S_OK</span></span> 
  
> <span data-ttu-id="60df0-116">行は正常に挿入されました。</span><span class="sxs-lookup"><span data-stu-id="60df0-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="60df0-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="60df0-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="60df0-118">挿入する行と同じインデックス列の値を持つ行がテーブルに既に存在します。</span><span class="sxs-lookup"><span data-stu-id="60df0-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60df0-119">解説</span><span class="sxs-lookup"><span data-stu-id="60df0-119">Remarks</span></span>

<span data-ttu-id="60df0-120">メソッドは **、** 特定の位置のテーブルに行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="60df0-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="60df0-121">新しい行は  _、uliRow_ パラメーターで指定された位置にある行の後に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="60df0-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="60df0-122">_uliRow_ がテーブルの行数に設定されている場合、新しい行はテーブルの末尾に追加されます。</span><span class="sxs-lookup"><span data-stu-id="60df0-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="60df0-123">テーブルのインデックス列として機能するプロパティは _、lpSRow_ パラメーターによって指される [SRow](srow.md)構造体の **lpProps** メンバーに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="60df0-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="60df0-124">このインデックス プロパティは、通常 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) は、今後のメンテナンス タスクの行を一意に識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="60df0-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="60df0-125">**SRow** 構造体のプロパティ列は、テーブル内のプロパティ列と同じ順序である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="60df0-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="60df0-126">行が挿入されると、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md) メソッドを呼び出して通知を登録するすべてのクライアントまたはサービス プロバイダーに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="60df0-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="60df0-127">制限のため、挿入された行がビューに含まれていない場合は、通知は送信されません。</span><span class="sxs-lookup"><span data-stu-id="60df0-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60df0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="60df0-128">See also</span></span>



[<span data-ttu-id="60df0-129">SRow</span><span class="sxs-lookup"><span data-stu-id="60df0-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="60df0-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="60df0-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="60df0-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60df0-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

