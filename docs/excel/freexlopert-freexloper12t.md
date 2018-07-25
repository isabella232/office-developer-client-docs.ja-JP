---
title: FreeXLOperT/FreeXLOper12T
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FreeXLOper12T
- FreeXLOperT
keywords:
- freexlopert function [excel 2007],FreeXLOper12T function [Excel 2007]
localization_priority: Normal
ms.assetid: 8fb3fdfd-8a43-4c50-82ff-e701fed3d83f
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b7411bc51770dadc7c2d4a5c2c65d2d546f6025f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798885"
---
# <a name="freexlopertfreexloper12t"></a><span data-ttu-id="a9ee7-104">FreeXLOperT/FreeXLOper12T</span><span class="sxs-lookup"><span data-stu-id="a9ee7-104">FreeXLOperT/FreeXLOper12T</span></span>

 <span data-ttu-id="a9ee7-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a9ee7-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a9ee7-p101">**XLOPER**/ **XLOPER12** に関連付けられているメモリを解放するフレームワーク関数。この関数は、DLL 内での malloc の呼び出しでメモリが割り当てられたことを前提としています。Microsoft Excel、その他の何らかの方法、または他のプロセスによりメモリが割り当てられた場合は、この関数を使用してメモリを解放すべきではありません。Excel によって **XLOPER**/ **XLOPER12** に割り当てられたメモリを解放するには、[xlFree](xlfree.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="a9ee7-p101">Framework function that frees memory associated with an **XLOPER**/ **XLOPER12**. The function assumes that the memory was allocated with calls to malloc within the DLL. If the memory was allocated by Microsoft Excel or in some other way or by some other process, this function should not be used to free the memory. Use [xlFree](xlfree.md) to free memory allocated by Excel for **XLOPER**/ **XLOPER12**s.</span></span> 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="a9ee7-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a9ee7-110">Parameters</span></span>

 <span data-ttu-id="a9ee7-111">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="a9ee7-111">_pxloper_ (**LPXLOPER**)</span></span>
  
 <span data-ttu-id="a9ee7-112">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="a9ee7-112">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="a9ee7-113">解放する **XLOPER**/ **XLOPER12** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9ee7-113">Pointer to the **XLOPER**/ **XLOPER12** to be freed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a9ee7-114">例</span><span class="sxs-lookup"><span data-stu-id="a9ee7-114">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
void FreeXLOper12T(LPXLOPER12 pxloper12)
{
   DWORD xltype;
   int cxloper12;
   LPXLOPER12 pxloper12Free;
   xltype = pxloper12->xltype;
   switch (xltype)
   {
   case xltypeStr:
      if (pxloper12->val.str != NULL)
         free(pxloper12->val.str);
      break;
   case xltypeRef:
      if (pxloper12->val.mref.lpmref != NULL)
         free(pxloper12->val.mref.lpmref);
      break;
   case xltypeMulti:
      cxloper12 = pxloper12->val.array.rows * pxloper12->val.array.columns;
      if (pxloper12->val.array.lparray)
      {
         pxloper12Free = pxloper12->val.array.lparray;
         while (cxloper12 > 0)
         {
            FreeXLOper12T(pxloper12Free);
            pxloper12Free++;
            cxloper12--;
         }
         free(pxloper12->val.array.lparray);
      }
      break;
   case xltypeBigData:
      if (pxloper12->val.bigdata.h.lpbData != NULL)
         free(pxloper12->val.bigdata.h.lpbData);
      break;
   }
}
```

## <a name="see-also"></a><span data-ttu-id="a9ee7-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9ee7-115">See also</span></span>



[<span data-ttu-id="a9ee7-116">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="a9ee7-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

