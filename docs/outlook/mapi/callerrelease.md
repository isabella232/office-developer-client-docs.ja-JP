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
# <a name="callerrelease"></a><span data-ttu-id="2669a-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="2669a-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="2669a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2669a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2669a-105">テーブル ビューのリリース時にテーブル データ オブジェクトを解放できるコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2669a-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2669a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2669a-106">Header file:</span></span>  <br/> |<span data-ttu-id="2669a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2669a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2669a-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="2669a-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="2669a-109">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2669a-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="2669a-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="2669a-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="2669a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="2669a-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="2669a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2669a-112">Parameters</span></span>

 <span data-ttu-id="2669a-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="2669a-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="2669a-114">[in]テーブル ビューを使用して MAPI によって保存され **、CALLERRELEASE** ベースのコールバック関数に渡される呼び出し元データ。</span><span class="sxs-lookup"><span data-stu-id="2669a-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="2669a-115">データは、リリースされるテーブル ビューに関するコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="2669a-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="2669a-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="2669a-116">_lpTblData_</span></span>
  
> <span data-ttu-id="2669a-117">[in] [ITableData へのポインター: 解放](itabledataiunknown.md) されるテーブル ビューの基になるテーブル データ オブジェクトの IUnknown インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="2669a-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="2669a-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="2669a-118">_lpVue_</span></span>
  
> <span data-ttu-id="2669a-119">[in] [IMAPITable へのポインター: 解放されるテーブル ビューの IUnknown](imapitableiunknown.md) インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="2669a-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="2669a-120">これは、解放するオブジェクトを作成した [ITableData::HrGetView](itabledata-hrgetview.md)メソッドの _lppMAPITable_ パラメーターで返されるテーブル オブジェクトのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="2669a-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2669a-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="2669a-121">Return value</span></span>

<span data-ttu-id="2669a-122">なし</span><span class="sxs-lookup"><span data-stu-id="2669a-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2669a-123">注釈</span><span class="sxs-lookup"><span data-stu-id="2669a-123">Remarks</span></span>

<span data-ttu-id="2669a-124">テーブル データ オブジェクトを設定したクライアント アプリケーションまたはサービス プロバイダーは [、ITableData::HrGetView](itabledata-hrgetview.md) を呼び出して、テーブルの読み取り専用で並べ替えたビューを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2669a-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="2669a-125">**HrGetView の呼び** 出しは **、CALLERRELEASE** ベースのコールバック関数へのポインターと、テーブル ビューに保存されるコンテキストを渡します。</span><span class="sxs-lookup"><span data-stu-id="2669a-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="2669a-126">テーブル ビューの参照カウントが 0 に戻り、ビューが解放されると **、IMAPITable** 実装はコールバック関数を呼び出し  _、ulCallerData_ パラメーターでコンテキストを渡します。</span><span class="sxs-lookup"><span data-stu-id="2669a-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="2669a-127">**CALLERRELEASE** ベースのコールバック関数の一般的な使用は、基になるテーブル データ オブジェクトを解放し、後続の処理中に追跡する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2669a-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

