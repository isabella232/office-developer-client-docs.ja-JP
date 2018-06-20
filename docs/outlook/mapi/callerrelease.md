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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 69ee06ef8c8f5499dec41232d3dc7b374b15a744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799747"
---
# <a name="callerrelease"></a><span data-ttu-id="2e56c-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="2e56c-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="2e56c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e56c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e56c-105">テーブル ビューがリリースされたとき、テーブルのデータ オブジェクトをリリースできるコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2e56c-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e56c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2e56c-106">Header file:</span></span>  <br/> |<span data-ttu-id="2e56c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2e56c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2e56c-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="2e56c-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="2e56c-109">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2e56c-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="2e56c-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2e56c-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="2e56c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="2e56c-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="2e56c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="2e56c-112">Parameters</span></span>

 <span data-ttu-id="2e56c-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="2e56c-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="2e56c-114">[in]コールバック関数を表形式ビューで、MAPI によって保存され、 **CALLERRELEASE**に渡される呼び出し元のデータに基づいています。</span><span class="sxs-lookup"><span data-stu-id="2e56c-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="2e56c-115">データでは、リリースされている表形式のビューのコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="2e56c-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="2e56c-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="2e56c-116">_lpTblData_</span></span>
  
> <span data-ttu-id="2e56c-117">[in]ポインター、 [ITableData: IUnknown](itabledataiunknown.md)リリースされている表形式のビューの基になるテーブルのデータ オブジェクトのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="2e56c-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="2e56c-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="2e56c-118">_lpVue_</span></span>
  
> <span data-ttu-id="2e56c-119">[in]ポインター、 [IMAPITable: IUnknown](imapitableiunknown.md)リリースされている表形式のビューのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="2e56c-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="2e56c-120">これは、リリースするオブジェクトを作成した[ITableData::HrGetView](itabledata-hrgetview.md)メソッドの_lppMAPITable_パラメーターで返される table オブジェクトのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="2e56c-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2e56c-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2e56c-121">Return value</span></span>

<span data-ttu-id="2e56c-122">なし</span><span class="sxs-lookup"><span data-stu-id="2e56c-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2e56c-123">解説</span><span class="sxs-lookup"><span data-stu-id="2e56c-123">Remarks</span></span>

<span data-ttu-id="2e56c-124">クライアント アプリケーションまたはサービス プロバイダーのテーブルのデータ オブジェクトにデータを設定するには、読み取り専用で、並べ替えられたテーブルのビューを作成する[ITableData::HrGetView](itabledata-hrgetview.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="2e56c-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="2e56c-125">**HrGetView**への呼び出しは、 **CALLERRELEASE**ベースのコールバック関数とテーブル ・ ビューを保存するコンテキストへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="2e56c-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="2e56c-126">テーブル ビューの参照カウントがゼロに戻ります、ビューがリリースされている、 **IMAPITable**実装は、コンテキストを_ulCallerData_パラメーターに渡して、コールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2e56c-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="2e56c-127">**CALLERRELEASE**ベースのコールバック関数の一般的な用途では、基になるテーブルのデータ オブジェクトを解放していないを追跡するため、後続の処理中にします。</span><span class="sxs-lookup"><span data-stu-id="2e56c-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

