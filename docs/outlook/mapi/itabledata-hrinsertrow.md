---
title: ITableDataHrInsertRow
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 29fdbf060576ee9309473fddf8740b06229dae9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801211"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="a9510-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="a9510-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="a9510-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9510-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9510-105">テーブルの行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="a9510-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="a9510-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a9510-106">Parameters</span></span>

 <span data-ttu-id="a9510-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="a9510-107">_uliRow_</span></span>
  
> <span data-ttu-id="a9510-108">[in]特定の行を表す連続した行の数です。</span><span class="sxs-lookup"><span data-stu-id="a9510-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="a9510-109">ローの数を示す新しい行に配置されます。</span><span class="sxs-lookup"><span data-stu-id="a9510-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="a9510-110">_UliRow_パラメーターは、0 から n 行番号が含まれていますが、n は、テーブル内の行の合計数です。</span><span class="sxs-lookup"><span data-stu-id="a9510-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="a9510-111">N を_uliRow_に渡すと、テーブルの末尾に行が追加されます。</span><span class="sxs-lookup"><span data-stu-id="a9510-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="a9510-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="a9510-112">_lpSRow_</span></span>
  
> <span data-ttu-id="a9510-113">[in]挿入する行を説明する[SRow](srow.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9510-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a9510-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a9510-114">Return value</span></span>

<span data-ttu-id="a9510-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9510-115">S_OK</span></span> 
  
> <span data-ttu-id="a9510-116">行は正しく挿入されました。</span><span class="sxs-lookup"><span data-stu-id="a9510-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="a9510-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a9510-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="a9510-118">テーブルに既に挿入する行が存在するとそのインデックス列に対して同じ値を持つ行です。</span><span class="sxs-lookup"><span data-stu-id="a9510-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9510-119">備考</span><span class="sxs-lookup"><span data-stu-id="a9510-119">Remarks</span></span>

<span data-ttu-id="a9510-120">**ITableData::HrInsertRow**メソッドでは、特定の位置にあるテーブルに行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="a9510-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="a9510-121">_UliRow_パラメーターによって指定された位置にある行の後に、新しい行が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="a9510-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="a9510-122">_UliRow_は、テーブル内の行の数に設定されている場合は、テーブルの末尾に新しい行が追加されます。</span><span class="sxs-lookup"><span data-stu-id="a9510-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="a9510-123">**LpProps** 、 [SRow](srow.md)構造体のメンバー、 _lpSRow_パラメーターが指すは、テーブルのインデックス列として機能するプロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9510-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="a9510-124">このインデックスのプロパティ、 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) を通常は、将来の保守タスクの行を一意に識別されます。</span><span class="sxs-lookup"><span data-stu-id="a9510-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="a9510-125">**SRow**構造体のプロパティ列をテーブル内のプロパティの列と同じ順序にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a9510-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="a9510-126">行が挿入されると、すべてのクライアントやテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが、サービス プロバイダーに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="a9510-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="a9510-127">制限があるため、ビューに挿入された行が含まれていない場合、通知は送信されません。</span><span class="sxs-lookup"><span data-stu-id="a9510-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9510-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9510-128">See also</span></span>



[<span data-ttu-id="a9510-129">SRow</span><span class="sxs-lookup"><span data-stu-id="a9510-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="a9510-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="a9510-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="a9510-131">ITableData: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9510-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

