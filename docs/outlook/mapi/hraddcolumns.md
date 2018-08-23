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
ms.openlocfilehash: dc7fa8b546783819b701604a5e489f0fd030ae86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800267"
---
# <a name="hraddcolumns"></a><span data-ttu-id="4dcc7-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="4dcc7-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="4dcc7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4dcc7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4dcc7-105">追加または既存のテーブルの先頭に列を移動します。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4dcc7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4dcc7-106">Header file:</span></span>  <br/> |<span data-ttu-id="4dcc7-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4dcc7-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4dcc7-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4dcc7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4dcc7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4dcc7-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-110">Called by:</span></span>  <br/> |<span data-ttu-id="4dcc7-111">クライアント アプリケーションとサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="4dcc7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4dcc7-112">Parameters</span></span>

 <span data-ttu-id="4dcc7-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="4dcc7-113">_lptbl_</span></span>
  
> <span data-ttu-id="4dcc7-114">[in]影響を MAPI テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="4dcc7-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="4dcc7-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="4dcc7-116">[in]追加されたり、テーブルの先頭に移動するにはプロパティのプロパティ タグの配列を含む**SPropTagArray**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="4dcc7-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="4dcc7-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="4dcc7-118">[in]**MAPIAllocateBuffer**関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="4dcc7-119">メモリの割り当てに使用されます。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="4dcc7-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="4dcc7-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="4dcc7-121">[in]**MAPIFreeBuffer**関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="4dcc7-122">メモリを解放するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4dcc7-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="4dcc7-123">Return value</span></span>

 <span data-ttu-id="4dcc7-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="4dcc7-124">**S_OK**</span></span>
  
> <span data-ttu-id="4dcc7-125">呼び出しが成功し、指定された列の移動先または追加されました。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4dcc7-126">注釈</span><span class="sxs-lookup"><span data-stu-id="4dcc7-126">Remarks</span></span>

<span data-ttu-id="4dcc7-127">**HrAddColumns**関数では、 _lpfnFilterColumns_を NULL に設定で**HrAddColumnsEx**を使用するのと同じです。</span><span class="sxs-lookup"><span data-stu-id="4dcc7-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4dcc7-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="4dcc7-128">See also</span></span>



[<span data-ttu-id="4dcc7-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="4dcc7-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="4dcc7-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4dcc7-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="4dcc7-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4dcc7-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4dcc7-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="4dcc7-132">SPropTagArray</span></span>](sproptagarray.md)

