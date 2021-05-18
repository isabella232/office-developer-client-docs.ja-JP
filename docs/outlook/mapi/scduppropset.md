---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406018"
---
# <a name="scduppropset"></a><span data-ttu-id="391ba-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="391ba-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="391ba-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="391ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="391ba-105">[ScCopyProps](sccopyprops.md)関数と[ScCountProps](sccountprops.md)関数の操作を組み合わせた MAPI メモリの 1 つのブロック内のプロパティ値配列を複製します。</span><span class="sxs-lookup"><span data-stu-id="391ba-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="391ba-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="391ba-106">Header file:</span></span>  <br/> |<span data-ttu-id="391ba-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="391ba-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="391ba-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="391ba-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="391ba-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="391ba-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="391ba-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="391ba-110">Called by:</span></span>  <br/> |<span data-ttu-id="391ba-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="391ba-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="391ba-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="391ba-112">Parameters</span></span>

 <span data-ttu-id="391ba-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="391ba-113">_cprop_</span></span>
  
> <span data-ttu-id="391ba-114">[in]rgprop パラメーターで示される配列内の  _プロパティ値の_ 数。</span><span class="sxs-lookup"><span data-stu-id="391ba-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="391ba-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="391ba-115">_rgprop_</span></span>
  
> <span data-ttu-id="391ba-116">[in]重複するプロパティ値を [定義する SPropValue](spropvalue.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="391ba-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="391ba-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="391ba-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="391ba-118">[in]重複した配列のメモリを割り当てるのに使用する [MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="391ba-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="391ba-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="391ba-119">_prgprop_</span></span>
  
> <span data-ttu-id="391ba-120">[out] **SPropValue** 構造体の返された重複配列が格納されているメモリ内の最初の位置へのポインター。</span><span class="sxs-lookup"><span data-stu-id="391ba-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="391ba-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="391ba-121">Return value</span></span>

<span data-ttu-id="391ba-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="391ba-122">S_OK</span></span> 
  
> <span data-ttu-id="391ba-123">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="391ba-123">The call succeeded and has returned the expected value or values.</span></span>
    

