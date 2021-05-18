---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278716"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="49392-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="49392-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="49392-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49392-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49392-105">IMAPITable 実装へのポインターを返すテーブル [ビューを作成](imapitableiunknown.md) します。</span><span class="sxs-lookup"><span data-stu-id="49392-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="49392-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49392-106">Parameters</span></span>

 <span data-ttu-id="49392-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="49392-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="49392-108">[in]テーブル ビューの並べ替え順序を表す並べ替え順序構造へのポインター。</span><span class="sxs-lookup"><span data-stu-id="49392-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="49392-109">_lpSSortOrderSet_ パラメーターで NULL が渡された場合、ビューは並べ替えされません。</span><span class="sxs-lookup"><span data-stu-id="49392-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="49392-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="49392-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="49392-111">[in]MAPI がビューを解放するときに呼び出す [CALLERRELEASE](callerrelease.md) プロトタイプに基づくコールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="49392-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="49392-112">_lpfCallerRelease_ パラメーターで NULL が渡された場合、ビューのリリース時に関数は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="49392-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="49392-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="49392-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="49392-114">[in]新しいビューで保存し  _、lpfCallerRelease_ が指すコールバック関数に渡す必要があるデータ。</span><span class="sxs-lookup"><span data-stu-id="49392-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="49392-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="49392-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="49392-116">[out]新しく作成されたビューへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="49392-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="49392-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="49392-117">Return value</span></span>

<span data-ttu-id="49392-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="49392-118">S_OK</span></span> 
  
> <span data-ttu-id="49392-119">ビューが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="49392-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49392-120">注釈</span><span class="sxs-lookup"><span data-stu-id="49392-120">Remarks</span></span>

<span data-ttu-id="49392-121">**ITableData::HrGetView** メソッドは _、lpSSortOrderSet_ パラメーターが指す順序で並べ替え、テーブル内のデータの読み取り専用ビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="49392-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="49392-122">カーソルは、ビューの最初の行の先頭に配置されます。</span><span class="sxs-lookup"><span data-stu-id="49392-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="49392-123">ビュー **にアクセスする IMAPITable** インターフェイス実装が返されます。</span><span class="sxs-lookup"><span data-stu-id="49392-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="49392-124">サービス プロバイダーは、 **クライアントにテーブルへの** アクセス権を与える必要がある場合に HrGetView を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49392-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="49392-125">**HrGetView は** ビューを作成し **、IMAPITable ポインターを返** します。</span><span class="sxs-lookup"><span data-stu-id="49392-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="49392-126">サービス プロバイダーは、クライアントにポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="49392-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="49392-127">クライアントがテーブルの使用を終了し、 [その IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) メソッドを呼び出す場合 **、HrGetView** は  _lpfCallerRelease_ パラメーターが指すコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49392-127">When the client is finished using the table and calls its [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="49392-128">サービス プロバイダーがカスタマイズされた列セットまたは制限を持つビューをクライアントに返す必要がある場合、プロバイダーは、クライアント アクセスを許可する前に、ビューの [IMAPITable::SetColumns](imapitable-setcolumns.md) メソッドと [IMAPITable::Restrict](imapitable-restrict.md) メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="49392-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49392-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="49392-129">See also</span></span>



[<span data-ttu-id="49392-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="49392-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="49392-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49392-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="49392-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="49392-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="49392-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49392-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

