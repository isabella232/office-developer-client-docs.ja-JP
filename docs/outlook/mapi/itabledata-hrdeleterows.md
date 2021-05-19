---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416455"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="1b9f9-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="1b9f9-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="1b9f9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b9f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b9f9-105">複数のテーブル行を削除します。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="1b9f9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1b9f9-106">Parameters</span></span>

 <span data-ttu-id="1b9f9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b9f9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1b9f9-108">[in]削除を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="1b9f9-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="1b9f9-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="1b9f9-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="1b9f9-111">テーブルと対応するビューからすべての行を削除し、1 つのビュー TABLE_RELOADします。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="1b9f9-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="1b9f9-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="1b9f9-113">[in]削除する行を記述する行セットへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="1b9f9-114">_lprowsetToDelete_ パラメーターは _、ulFlags_ パラメーター TAD_ALL_ROWSフラグが設定されている場合は NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1b9f9-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="1b9f9-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="1b9f9-116">[out]削除された行の数。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b9f9-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="1b9f9-117">Return value</span></span>

<span data-ttu-id="1b9f9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b9f9-118">S_OK</span></span> 
  
> <span data-ttu-id="1b9f9-119">テーブル行が正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b9f9-120">注釈</span><span class="sxs-lookup"><span data-stu-id="1b9f9-120">Remarks</span></span>

<span data-ttu-id="1b9f9-121">**ITableData::HrDeleteRows** メソッドは、行セット内の各 **aRow** エントリの **lpProps** メンバーが指すプロパティに一致する列を含むテーブル行を検索して削除します。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="1b9f9-122">インデックス列は、各行を識別するために使用されます。この列には [、CreateTable](createtable.md)関数の呼び出しで _ulPropTagIndexColumn_ パラメーターに渡されるプロパティ タグと同じプロパティ タグが必要です。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="1b9f9-123">実際に削除された行の数は  _、cRowsDeleted で返されます_。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="1b9f9-124">1 つ以上の行が見つからない場合、エラーは返されません。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="1b9f9-125">行が削除された後、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md) メソッドを呼び出して通知を登録しているすべてのクライアントまたはサービス プロバイダーに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="1b9f9-126">行を削除しても、削除された行が特定の列の値を持つ最後の行である場合でも、既存のテーブル ビューまたは後で開いたテーブル ビューで使用できる列は減らされません。</span><span class="sxs-lookup"><span data-stu-id="1b9f9-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b9f9-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b9f9-127">See also</span></span>



[<span data-ttu-id="1b9f9-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="1b9f9-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="1b9f9-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="1b9f9-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="1b9f9-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="1b9f9-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="1b9f9-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="1b9f9-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="1b9f9-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1b9f9-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="1b9f9-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b9f9-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

