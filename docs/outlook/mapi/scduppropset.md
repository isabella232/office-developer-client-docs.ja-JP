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
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581980"
---
# <a name="scduppropset"></a><span data-ttu-id="1bdf6-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="1bdf6-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="1bdf6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bdf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bdf6-105">MAPI のメモリ、 [ScCopyProps](sccopyprops.md)および[ScCountProps](sccountprops.md)関数の操作を組み合わせることの 1 つのブロックでは、プロパティ値の配列を複製します。</span><span class="sxs-lookup"><span data-stu-id="1bdf6-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bdf6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1bdf6-106">Header file:</span></span>  <br/> |<span data-ttu-id="1bdf6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1bdf6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1bdf6-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="1bdf6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1bdf6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1bdf6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1bdf6-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1bdf6-110">Called by:</span></span>  <br/> |<span data-ttu-id="1bdf6-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1bdf6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="1bdf6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1bdf6-112">Parameters</span></span>

 <span data-ttu-id="1bdf6-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="1bdf6-113">_cprop_</span></span>
  
> <span data-ttu-id="1bdf6-114">[in]_Rgprop_パラメーターで指定された配列内のプロパティ値の数。</span><span class="sxs-lookup"><span data-stu-id="1bdf6-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="1bdf6-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="1bdf6-115">_rgprop_</span></span>
  
> <span data-ttu-id="1bdf6-116">[in]重複するプロパティの値を定義する[SPropValue](spropvalue.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1bdf6-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="1bdf6-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="1bdf6-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="1bdf6-118">[in]重複配列のメモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1bdf6-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="1bdf6-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="1bdf6-119">_prgprop_</span></span>
  
> <span data-ttu-id="1bdf6-120">[out]返される複製された**SPropValue**構造体の配列が保存されているメモリ内の最初の位置へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1bdf6-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1bdf6-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1bdf6-121">Return value</span></span>

<span data-ttu-id="1bdf6-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="1bdf6-122">S_OK</span></span> 
  
> <span data-ttu-id="1bdf6-123">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="1bdf6-123">The call succeeded and has returned the expected value or values.</span></span>
    

