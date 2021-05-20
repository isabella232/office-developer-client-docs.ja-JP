---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- convertxlreftoxlref12 function [excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 530cb9cce5b0023318ff6b8a0ff73472f8250aa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432031"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="2fb23-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="2fb23-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="2fb23-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2fb23-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2fb23-106">**XLREF** を **XLREF12** に変換しようとする Framework 関数。</span><span class="sxs-lookup"><span data-stu-id="2fb23-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="2fb23-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2fb23-107">Parameters</span></span>

 <span data-ttu-id="2fb23-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="2fb23-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="2fb23-109">ソースの参照構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2fb23-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="2fb23-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="2fb23-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="2fb23-111">変換した値が配置されるターゲットの参照構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2fb23-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2fb23-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="2fb23-112">Property value/Return value</span></span>

 <span data-ttu-id="2fb23-113">変換が成功した場合は **TRUE**。それ以外の場合は **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2fb23-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2fb23-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2fb23-114">Remarks</span></span>

<span data-ttu-id="2fb23-p101">渡された **XLREF** が有効な場合、この操作は常に成功します。それとは対照的に、[ConvertXLRef12ToXLRef](convertxlref12toxlref.md) で実行する **XLREF12** から **XLREF** への逆の変換では、指定された参照が、前のバージョンでサポートされていない Excel 2007 ワークシートの一部を参照している場合、変換操作は失敗します。</span><span class="sxs-lookup"><span data-stu-id="2fb23-p101">Provided that the passed-in **XLREF** is valid, this operation should always be successful. In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="2fb23-117">例</span><span class="sxs-lookup"><span data-stu-id="2fb23-117">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxref, LPXLREF12 pxref12)
{
   if (pxref->rwLast >= pxref->rwFirst && pxref->colLast >= pxref->colFirst)
   {
      if (pxref->rwFirst >= 0 && pxref->colFirst >= 0)
      {
         pxref12->rwFirst = pxref->rwFirst;
         pxref12->rwLast = pxref->rwLast;
         pxref12->colFirst = pxref->colFirst;
         pxref12->colLast = pxref->colLast;
         return TRUE;
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="2fb23-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="2fb23-118">See also</span></span>



[<span data-ttu-id="2fb23-119">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="2fb23-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

