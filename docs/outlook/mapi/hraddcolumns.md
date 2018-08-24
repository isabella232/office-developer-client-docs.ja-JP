---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ffc47e924b7a0f94db66adbffe01b2cdc619dc8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580734"
---
# <a name="hraddcolumns"></a><span data-ttu-id="7bb91-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="7bb91-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="7bb91-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bb91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bb91-105">追加または既存のテーブルの先頭に列を移動します。</span><span class="sxs-lookup"><span data-stu-id="7bb91-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7bb91-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7bb91-106">Header file:</span></span>  <br/> |<span data-ttu-id="7bb91-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7bb91-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7bb91-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="7bb91-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7bb91-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7bb91-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7bb91-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7bb91-110">Called by:</span></span>  <br/> |<span data-ttu-id="7bb91-111">クライアント アプリケーションとサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="7bb91-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="7bb91-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7bb91-112">Parameters</span></span>

 <span data-ttu-id="7bb91-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="7bb91-113">_lptbl_</span></span>
  
> <span data-ttu-id="7bb91-114">[in]影響を MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7bb91-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="7bb91-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="7bb91-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="7bb91-116">[in]追加されたり、テーブルの先頭に移動するにはプロパティのプロパティ タグの配列を含む**SPropTagArray**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7bb91-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="7bb91-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="7bb91-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="7bb91-118">[in]**MAPIAllocateBuffer**関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7bb91-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="7bb91-119">メモリの割り当てに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bb91-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="7bb91-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="7bb91-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="7bb91-121">[in]**MAPIFreeBuffer**関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7bb91-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="7bb91-122">メモリを解放するために使用します。</span><span class="sxs-lookup"><span data-stu-id="7bb91-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7bb91-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="7bb91-123">Return value</span></span>

 <span data-ttu-id="7bb91-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="7bb91-124">**S_OK**</span></span>
  
> <span data-ttu-id="7bb91-125">呼び出しが成功し、指定された列の移動先または追加されました。</span><span class="sxs-lookup"><span data-stu-id="7bb91-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7bb91-126">注釈</span><span class="sxs-lookup"><span data-stu-id="7bb91-126">Remarks</span></span>

<span data-ttu-id="7bb91-127">**HrAddColumns**関数では、 _lpfnFilterColumns_を NULL に設定で**HrAddColumnsEx**を使用するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="7bb91-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7bb91-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bb91-128">See also</span></span>



[<span data-ttu-id="7bb91-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="7bb91-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="7bb91-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="7bb91-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="7bb91-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7bb91-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7bb91-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="7bb91-132">SPropTagArray</span></span>](sproptagarray.md)

