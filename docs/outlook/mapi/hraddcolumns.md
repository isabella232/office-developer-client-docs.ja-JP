---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422475"
---
# <a name="hraddcolumns"></a><span data-ttu-id="da3fd-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="da3fd-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="da3fd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da3fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da3fd-105">既存のテーブルの先頭に列を追加または移動します。</span><span class="sxs-lookup"><span data-stu-id="da3fd-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da3fd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="da3fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="da3fd-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="da3fd-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="da3fd-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="da3fd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="da3fd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="da3fd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="da3fd-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="da3fd-110">Called by:</span></span>  <br/> |<span data-ttu-id="da3fd-111">クライアント アプリケーションとサービス プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="da3fd-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="da3fd-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="da3fd-112">Parameters</span></span>

 <span data-ttu-id="da3fd-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="da3fd-113">_lptbl_</span></span>
  
> <span data-ttu-id="da3fd-114">[in]影響を受ける MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="da3fd-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="da3fd-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="da3fd-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="da3fd-116">[in]テーブルの先頭に追加または移動するプロパティのプロパティ タグの配列を含む **SPropTagArray** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="da3fd-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="da3fd-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="da3fd-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="da3fd-118">[in] **MAPIAllocateBuffer 関数への** ポインター。</span><span class="sxs-lookup"><span data-stu-id="da3fd-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="da3fd-119">メモリの割り当てに使用されます。</span><span class="sxs-lookup"><span data-stu-id="da3fd-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="da3fd-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="da3fd-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="da3fd-121">[in] **MAPIFreeBuffer 関数への** ポインター。</span><span class="sxs-lookup"><span data-stu-id="da3fd-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="da3fd-122">メモリを解放するために使用します。</span><span class="sxs-lookup"><span data-stu-id="da3fd-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="da3fd-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="da3fd-123">Return value</span></span>

 <span data-ttu-id="da3fd-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="da3fd-124">**S_OK**</span></span>
  
> <span data-ttu-id="da3fd-125">呼び出しが成功し、指定された列が移動または追加されました。</span><span class="sxs-lookup"><span data-stu-id="da3fd-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da3fd-126">注釈</span><span class="sxs-lookup"><span data-stu-id="da3fd-126">Remarks</span></span>

<span data-ttu-id="da3fd-127">**HrAddColumns 関数** は _、lpfnFilterColumns_ が NULL に設定された **HrAddColumnsEx** を使用するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="da3fd-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da3fd-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="da3fd-128">See also</span></span>



[<span data-ttu-id="da3fd-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="da3fd-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="da3fd-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="da3fd-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="da3fd-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="da3fd-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="da3fd-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="da3fd-132">SPropTagArray</span></span>](sproptagarray.md)

