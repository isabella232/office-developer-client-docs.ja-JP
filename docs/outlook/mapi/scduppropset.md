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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351269"
---
# <a name="scduppropset"></a><span data-ttu-id="7e34d-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="7e34d-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="7e34d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e34d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e34d-105">[sccopyprops](sccopyprops.md)関数と[sccopyprops](sccountprops.md)関数の操作を組み合わせて、1つの MAPI メモリブロックでプロパティ値配列を複製します。</span><span class="sxs-lookup"><span data-stu-id="7e34d-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e34d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7e34d-106">Header file:</span></span>  <br/> |<span data-ttu-id="7e34d-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="7e34d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7e34d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="7e34d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7e34d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7e34d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7e34d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="7e34d-110">Called by:</span></span>  <br/> |<span data-ttu-id="7e34d-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="7e34d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="7e34d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e34d-112">Parameters</span></span>

 <span data-ttu-id="7e34d-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="7e34d-113">_cprop_</span></span>
  
> <span data-ttu-id="7e34d-114">順番_rgprop_パラメーターで指定された、配列内のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="7e34d-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="7e34d-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="7e34d-115">_rgprop_</span></span>
  
> <span data-ttu-id="7e34d-116">順番複製するプロパティ値を定義する[spropvalue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7e34d-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="7e34d-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="7e34d-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="7e34d-118">順番複製された配列のメモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7e34d-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="7e34d-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="7e34d-119">_prgprop_</span></span>
  
> <span data-ttu-id="7e34d-120">読み上げ返された**spropvalue**構造体の配列が格納されている、メモリ内の初期位置へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7e34d-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7e34d-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="7e34d-121">Return value</span></span>

<span data-ttu-id="7e34d-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e34d-122">S_OK</span></span> 
  
> <span data-ttu-id="7e34d-123">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="7e34d-123">The call succeeded and has returned the expected value or values.</span></span>
    

