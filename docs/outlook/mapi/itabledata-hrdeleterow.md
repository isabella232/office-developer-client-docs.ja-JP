---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278861"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="084aa-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="084aa-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="084aa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="084aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="084aa-105">表の行を削除します。</span><span class="sxs-lookup"><span data-stu-id="084aa-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="084aa-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="084aa-106">Parameters</span></span>

 <span data-ttu-id="084aa-107">_lpspropvalue_</span><span class="sxs-lookup"><span data-stu-id="084aa-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="084aa-108">順番削除する行のインデックス列を記述するプロパティ値構造へのポインター。</span><span class="sxs-lookup"><span data-stu-id="084aa-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="084aa-109">プロパティ値構造の**ulPropTag**メンバーには、 [CreateTable](createtable.md)関数の呼び出しの_ulPropTagIndexColumn_パラメーターと同じプロパティタグが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="084aa-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="084aa-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="084aa-110">Return value</span></span>

<span data-ttu-id="084aa-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="084aa-111">S_OK</span></span> 
  
> <span data-ttu-id="084aa-112">行が正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="084aa-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="084aa-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="084aa-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="084aa-114">_lpspropvalue_パラメーターによって示されるプロパティは、テーブル内の行を識別しません。</span><span class="sxs-lookup"><span data-stu-id="084aa-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="084aa-115">解説</span><span class="sxs-lookup"><span data-stu-id="084aa-115">Remarks</span></span>

<span data-ttu-id="084aa-116">**itabledata:: HrDeleteRow**メソッドは、 _lpspropvalue_パラメーターによって示されるプロパティに一致する列を含むテーブル行を削除します。</span><span class="sxs-lookup"><span data-stu-id="084aa-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="084aa-117">行のデータが削除され、開いているすべてのビューからその行が削除されます。</span><span class="sxs-lookup"><span data-stu-id="084aa-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="084aa-118">行が削除されると、テーブルのビューを持つすべてのクライアントまたはサービスプロバイダーに通知が送信され、通知を登録するためにテーブルの[IMAPITable:: Advise](imapitable-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="084aa-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="084aa-119">行を削除しても、削除された行が、特定の列の値を持つ最後の行であっても、既存のビューまたは後で開くことができる列セットは縮小されません。</span><span class="sxs-lookup"><span data-stu-id="084aa-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="084aa-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="084aa-120">See also</span></span>



[<span data-ttu-id="084aa-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="084aa-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="084aa-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="084aa-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="084aa-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="084aa-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="084aa-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="084aa-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="084aa-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="084aa-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="084aa-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="084aa-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

