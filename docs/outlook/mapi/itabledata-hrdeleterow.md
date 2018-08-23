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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 989c6872e78ef78e5e0b18149a186d4f920ca603
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563465"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="5f13c-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="5f13c-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="5f13c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f13c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f13c-105">テーブルの行を削除します。</span><span class="sxs-lookup"><span data-stu-id="5f13c-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="5f13c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5f13c-106">Parameters</span></span>

 <span data-ttu-id="5f13c-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="5f13c-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="5f13c-108">[in]削除する行のインデックス列を説明するプロパティ値の構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5f13c-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="5f13c-109">プロパティ値の構造体の**ulPropTag**メンバーは、 [CreateTable](createtable.md)関数への呼び出しの_ulPropTagIndexColumn_パラメーターと同じプロパティ タグを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f13c-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5f13c-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5f13c-110">Return value</span></span>

<span data-ttu-id="5f13c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f13c-111">S_OK</span></span> 
  
> <span data-ttu-id="5f13c-112">行が正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="5f13c-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="5f13c-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5f13c-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5f13c-114">_LpSPropValue_パラメーターで指定されたプロパティは、テーブル内の行を識別しません。</span><span class="sxs-lookup"><span data-stu-id="5f13c-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5f13c-115">注釈</span><span class="sxs-lookup"><span data-stu-id="5f13c-115">Remarks</span></span>

<span data-ttu-id="5f13c-116">**ITableData::HrDeleteRow**メソッドは、 _lpSPropValue_パラメーターで指定されたプロパティに一致する列を含むテーブルの行を削除します。</span><span class="sxs-lookup"><span data-stu-id="5f13c-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="5f13c-117">行のデータが削除され、行は、開いているすべてのビューから削除されます。</span><span class="sxs-lookup"><span data-stu-id="5f13c-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="5f13c-118">行が削除されると、すべてのクライアントやテーブルのビューがあるし、の通知を登録するテーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出すことが、サービス プロバイダーに通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="5f13c-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="5f13c-119">行の削除は減りません列セットが既存のビューを使用するか、ビューを開いた後で削除された行が特定の列の値を持つ最後の行の場合でも。</span><span class="sxs-lookup"><span data-stu-id="5f13c-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f13c-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f13c-120">See also</span></span>



[<span data-ttu-id="5f13c-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="5f13c-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="5f13c-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="5f13c-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="5f13c-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="5f13c-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="5f13c-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5f13c-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="5f13c-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5f13c-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="5f13c-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f13c-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

