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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0eb0374788da629c4c28eff2fce93536cf65a4ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582988"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="86522-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="86522-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="86522-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86522-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86522-105">[IMAPITable](imapitableiunknown.md)実装へのポインターを返す表形式ビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="86522-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="86522-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="86522-106">Parameters</span></span>

 <span data-ttu-id="86522-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="86522-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="86522-108">[in]テーブル ビューの並べ替え順序を記述する並べ替え順序の構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="86522-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="86522-109">_LpSSortOrderSet_パラメーターに NULL を渡した場合、ビューは並べ替えられません。</span><span class="sxs-lookup"><span data-stu-id="86522-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="86522-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="86522-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="86522-111">[in]MAPI がビューを解放するときに呼び出す[CALLERRELEASE](callerrelease.md)プロトタイプに基づいてコールバック関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="86522-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="86522-112">_LpfCallerRelease_パラメーターに NULL を渡した場合、ビューのリリースで関数は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="86522-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="86522-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="86522-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="86522-114">[in]_LpfCallerRelease_が指すデータを新しいビューを保存し、コールバック関数に渡される必要があります。</span><span class="sxs-lookup"><span data-stu-id="86522-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="86522-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="86522-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="86522-116">[out]新しく作成されたビューへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="86522-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="86522-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="86522-117">Return value</span></span>

<span data-ttu-id="86522-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="86522-118">S_OK</span></span> 
  
> <span data-ttu-id="86522-119">ビューは正しく作成されました。</span><span class="sxs-lookup"><span data-stu-id="86522-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="86522-120">注釈</span><span class="sxs-lookup"><span data-stu-id="86522-120">Remarks</span></span>

<span data-ttu-id="86522-121">**ITableData::HrGetView**メソッドは、 _lpSSortOrderSet_パラメーターで指定された順序で並べ替え、テーブルのデータの読み取り専用ビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="86522-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="86522-122">カーソルは、ビューの最初の行の先頭に配置されます。</span><span class="sxs-lookup"><span data-stu-id="86522-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="86522-123">ビューにアクセスするため**IMAPITable**インターフェイスの実装が返されます。</span><span class="sxs-lookup"><span data-stu-id="86522-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="86522-124">サービス プロバイダーは、テーブルにクライアントのアクセスを提供する必要があるときに**HrGetView**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="86522-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="86522-125">**HrGetView**では、ビューを作成し、 **IMAPITable**ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="86522-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="86522-126">サービス プロバイダーは、クライアントへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="86522-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="86522-127">クライアントでは、テーブルを使用した後し、その[リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)のメソッドを呼び出して、 **HrGetView**は、 _lpfCallerRelease_パラメーターで指定されたコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="86522-127">When the client is finished using the table and calls its [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="86522-128">サービス プロバイダーは、設定、カスタマイズされた列を持つビューをクライアントに返す必要があるか、制限、プロバイダー メソッドを呼び出して、ビューの[IMAPITable::SetColumns](imapitable-setcolumns.md)と[IMAPITable::Restrict](imapitable-restrict.md)のクライアント アクセスを許可する前にします。</span><span class="sxs-lookup"><span data-stu-id="86522-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86522-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="86522-129">See also</span></span>



[<span data-ttu-id="86522-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="86522-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="86522-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86522-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="86522-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="86522-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="86522-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86522-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

