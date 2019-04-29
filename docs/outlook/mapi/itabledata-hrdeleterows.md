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
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="f5a7f-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="f5a7f-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="f5a7f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5a7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5a7f-105">複数の表の行を削除します。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="f5a7f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f5a7f-106">Parameters</span></span>

 <span data-ttu-id="f5a7f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f5a7f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f5a7f-108">順番削除を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="f5a7f-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f5a7f-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="f5a7f-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="f5a7f-111">1つの TABLE_RELOAD 通知を送信して、テーブルおよび対応するすべてのビューからすべての行を削除します。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="f5a7f-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="f5a7f-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="f5a7f-113">順番削除する行を説明する行セットへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="f5a7f-114">TAD_ALL_ROWS フラグが_ulflags_パラメーターで設定されている場合は、 _lprowsetToDelete_パラメーターを NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f5a7f-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="f5a7f-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="f5a7f-116">読み上げ削除された行のカウント。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f5a7f-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="f5a7f-117">Return value</span></span>

<span data-ttu-id="f5a7f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5a7f-118">S_OK</span></span> 
  
> <span data-ttu-id="f5a7f-119">テーブルの行が正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f5a7f-120">注釈</span><span class="sxs-lookup"><span data-stu-id="f5a7f-120">Remarks</span></span>

<span data-ttu-id="f5a7f-121">**itabledata:: HrDeleteRows**メソッドは、行セット内の各**arow**エントリの**lpprops**メンバーによって示されるプロパティに一致する列を含むテーブル行を検索して削除します。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="f5a7f-122">インデックス列は、各行を識別するために使用されます。この列は、 [CreateTable](createtable.md)関数の呼び出しで_ulPropTagIndexColumn_パラメーターで渡されたプロパティタグと同じプロパティタグを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="f5a7f-123">実際に削除された行の数は、 _cRowsDeleted_で返されます。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="f5a7f-124">1つまたは複数の行が見つからない場合、エラーは返されません。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="f5a7f-125">行が削除されると、テーブルのビューを持つすべてのクライアントまたはサービスプロバイダーに通知が送信され、通知を登録するためにテーブルの[IMAPITable:: Advise](imapitable-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="f5a7f-126">行を削除しても、削除された行が特定の列の値を持つ最後の行であっても、既存のテーブルビューまたは後で開くテーブルビューで使用可能な列は減少しません。</span><span class="sxs-lookup"><span data-stu-id="f5a7f-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f5a7f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5a7f-127">See also</span></span>



[<span data-ttu-id="f5a7f-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="f5a7f-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="f5a7f-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="f5a7f-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="f5a7f-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="f5a7f-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="f5a7f-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="f5a7f-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="f5a7f-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f5a7f-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="f5a7f-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5a7f-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

