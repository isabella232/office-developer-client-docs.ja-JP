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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408727"
---
# <a name="callerrelease"></a><span data-ttu-id="d72e8-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="d72e8-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="d72e8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d72e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d72e8-105">テーブルビューが解放されているときに、テーブルデータオブジェクトを解放できるコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="d72e8-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d72e8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d72e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="d72e8-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="d72e8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d72e8-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="d72e8-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="d72e8-109">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="d72e8-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="d72e8-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="d72e8-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="d72e8-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d72e8-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="d72e8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d72e8-112">Parameters</span></span>

 <span data-ttu-id="d72e8-113">_ulcallerdata_</span><span class="sxs-lookup"><span data-stu-id="d72e8-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="d72e8-114">順番MAPI によってテーブルビューで保存され、 **callerrelease**ベースのコールバック関数に渡される発信者データ。</span><span class="sxs-lookup"><span data-stu-id="d72e8-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="d72e8-115">このデータは、リリースされるテーブルビューに関するコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="d72e8-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="d72e8-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="d72e8-116">_lpTblData_</span></span>
  
> <span data-ttu-id="d72e8-117">順番[itabledata](itabledataiunknown.md)へのポインター: 解放されるテーブルビューの基になるテーブルデータオブジェクトの IUnknown インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="d72e8-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="d72e8-118">_lpvue_</span><span class="sxs-lookup"><span data-stu-id="d72e8-118">_lpVue_</span></span>
  
> <span data-ttu-id="d72e8-119">順番リリースされるテーブルビューの[IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d72e8-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="d72e8-120">これは、解放するオブジェクトを作成した[itabledata:: hrgetview](itabledata-hrgetview.md)メソッドの_lppMAPITable_パラメーターで返される table オブジェクトのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="d72e8-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d72e8-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="d72e8-121">Return value</span></span>

<span data-ttu-id="d72e8-122">なし</span><span class="sxs-lookup"><span data-stu-id="d72e8-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d72e8-123">注釈</span><span class="sxs-lookup"><span data-stu-id="d72e8-123">Remarks</span></span>

<span data-ttu-id="d72e8-124">テーブルデータオブジェクトを設定したクライアントアプリケーションまたはサービスプロバイダーは、 [itabledata:: hrgetview](itabledata-hrgetview.md)を呼び出して、読み取り専用で並べ替えられたテーブルのビューを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d72e8-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="d72e8-125">**hrgetview**の呼び出しでは、 **callerrelease**ベースのコールバック関数へのポインターが渡されます。また、テーブルビューと共に保存されるコンテキストもあります。</span><span class="sxs-lookup"><span data-stu-id="d72e8-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="d72e8-126">テーブルビューの参照カウントが0に戻り、ビューが解放されるとき、 **IMAPITable**実装はコールバック関数を呼び出し、 _ulcallerdata_パラメーターにコンテキストを渡します。</span><span class="sxs-lookup"><span data-stu-id="d72e8-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="d72e8-127">**callerrelease**ベースのコールバック関数の一般的な使用方法は、基になるテーブルのデータオブジェクトを解放することで、以降の処理中にそのオブジェクトを追跡する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d72e8-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

