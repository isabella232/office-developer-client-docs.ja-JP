---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e97e1d5302d8247cb09ce7cb1b581582405300a5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568130"
---
# <a name="callerrelease"></a><span data-ttu-id="1fb04-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="1fb04-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="1fb04-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fb04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fb04-105">テーブル ビューがリリースされたとき、テーブルのデータ オブジェクトをリリースできるコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="1fb04-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fb04-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1fb04-106">Header file:</span></span>  <br/> |<span data-ttu-id="1fb04-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1fb04-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1fb04-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="1fb04-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="1fb04-109">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1fb04-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="1fb04-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="1fb04-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="1fb04-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="1fb04-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="1fb04-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1fb04-112">Parameters</span></span>

 <span data-ttu-id="1fb04-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="1fb04-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="1fb04-114">[in]コールバック関数を表形式ビューで、MAPI によって保存され、 **CALLERRELEASE**に渡される呼び出し元のデータに基づいています。</span><span class="sxs-lookup"><span data-stu-id="1fb04-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="1fb04-115">データでは、リリースされている表形式のビューのコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="1fb04-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="1fb04-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="1fb04-116">_lpTblData_</span></span>
  
> <span data-ttu-id="1fb04-117">[in]ポインター、 [ITableData: IUnknown](itabledataiunknown.md)リリースされている表形式のビューの基になるテーブルのデータ オブジェクトのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="1fb04-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="1fb04-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="1fb04-118">_lpVue_</span></span>
  
> <span data-ttu-id="1fb04-119">[in]ポインター、 [IMAPITable: IUnknown](imapitableiunknown.md)リリースされている表形式のビューのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="1fb04-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="1fb04-120">これは、リリースするオブジェクトを作成した[ITableData::HrGetView](itabledata-hrgetview.md)メソッドの_lppMAPITable_パラメーターで返される table オブジェクトのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="1fb04-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1fb04-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="1fb04-121">Return value</span></span>

<span data-ttu-id="1fb04-122">なし</span><span class="sxs-lookup"><span data-stu-id="1fb04-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1fb04-123">注釈</span><span class="sxs-lookup"><span data-stu-id="1fb04-123">Remarks</span></span>

<span data-ttu-id="1fb04-124">クライアント アプリケーションまたはサービス プロバイダーのテーブルのデータ オブジェクトにデータを設定するには、読み取り専用で、並べ替えられたテーブルのビューを作成する[ITableData::HrGetView](itabledata-hrgetview.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="1fb04-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="1fb04-125">**HrGetView**への呼び出しは、 **CALLERRELEASE**ベースのコールバック関数とテーブル ・ ビューを保存するコンテキストへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="1fb04-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="1fb04-126">テーブル ビューの参照カウントがゼロに戻ります、ビューがリリースされている、 **IMAPITable**実装は、コンテキストを_ulCallerData_パラメーターに渡して、コールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1fb04-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="1fb04-127">**CALLERRELEASE**ベースのコールバック関数の一般的な用途では、基になるテーブルのデータ オブジェクトを解放していないを追跡するため、後続の処理中にします。</span><span class="sxs-lookup"><span data-stu-id="1fb04-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

