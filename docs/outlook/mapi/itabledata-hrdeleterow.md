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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421677"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="98aa1-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="98aa1-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="98aa1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98aa1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98aa1-105">テーブル行を削除します。</span><span class="sxs-lookup"><span data-stu-id="98aa1-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="98aa1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="98aa1-106">Parameters</span></span>

 <span data-ttu-id="98aa1-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="98aa1-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="98aa1-108">[in]削除する行のインデックス列を記述するプロパティ値構造へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98aa1-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="98aa1-109">プロパティ **値構造体の ulPropTag** メンバーには、CreateTable 関数の呼び出しから  _ulPropTagIndexColumn_ パラメーターと同じプロパティ タグを [含む必要](createtable.md) があります。</span><span class="sxs-lookup"><span data-stu-id="98aa1-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98aa1-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="98aa1-110">Return value</span></span>

<span data-ttu-id="98aa1-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="98aa1-111">S_OK</span></span> 
  
> <span data-ttu-id="98aa1-112">行が正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="98aa1-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="98aa1-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="98aa1-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="98aa1-114">_lpSPropValue_ パラメーターが示すプロパティは、テーブル内の行を識別します。</span><span class="sxs-lookup"><span data-stu-id="98aa1-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="98aa1-115">注釈</span><span class="sxs-lookup"><span data-stu-id="98aa1-115">Remarks</span></span>

<span data-ttu-id="98aa1-116">**ITableData::HrDeleteRow** メソッドは _、lpSPropValue_ パラメーターが指すプロパティに一致する列を含むテーブル行を削除します。</span><span class="sxs-lookup"><span data-stu-id="98aa1-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="98aa1-117">行のデータが削除され、開いているすべてのビューから行が削除されます。</span><span class="sxs-lookup"><span data-stu-id="98aa1-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="98aa1-118">行が削除された後、テーブルのビューを持ち、テーブルの [IMAPITable::Advise](imapitable-advise.md) メソッドを呼び出して通知を登録しているすべてのクライアントまたはサービス プロバイダーに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="98aa1-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="98aa1-119">行を削除しても、削除された行が特定の列の値を持つ最後の行である場合でも、既存のビューまたは後で開いたビューで使用できる列セットは減らされません。</span><span class="sxs-lookup"><span data-stu-id="98aa1-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98aa1-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="98aa1-120">See also</span></span>



[<span data-ttu-id="98aa1-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="98aa1-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="98aa1-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="98aa1-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="98aa1-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="98aa1-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="98aa1-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="98aa1-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="98aa1-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="98aa1-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="98aa1-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98aa1-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

