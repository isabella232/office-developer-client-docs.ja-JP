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
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: b7411bc51770dadc7c2d4a5c2c65d2d546f6025f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798885"
---
# <a name="freexlopertfreexloper12t"></a><span data-ttu-id="fc02e-104">FreeXLOperT/FreeXLOper12T</span><span class="sxs-lookup"><span data-stu-id="fc02e-104">FreeXLOperT/FreeXLOper12T</span></span>

 <span data-ttu-id="fc02e-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fc02e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fc02e-p101">**XLOPER**/ **XLOPER12** �Ɋ֘A�t�����Ă����������������� Framework �֐��B���̊֐��́ADLL ��ł� malloc �̌Ăяo���Ń����������蓖�Ă�ꂽ���Ƃ�O��Ƃ��Ă��܂��BMicrosoft Excel�A���̑��̉��炩�̕��@�A�܂��͑��̃v���Z�X�ɂ�胁���������蓖�Ă�ꂽ�ꍇ�́A���̊֐���g�p���ă������������ׂ��ł͂���܂���B [xlFree](xlfree.md) ��g�p���āA **XLOPER**/ **XLOPER12** �� Excel �����蓖�Ă��������������܂��B</span><span class="sxs-lookup"><span data-stu-id="fc02e-p101">Framework function that frees memory associated with an **XLOPER**/ **XLOPER12**. The function assumes that the memory was allocated with calls to malloc within the DLL. If the memory was allocated by Microsoft Excel or in some other way or by some other process, this function should not be used to free the memory. Use [xlFree](xlfree.md) to free memory allocated by Excel for **XLOPER**/ **XLOPER12**s.</span></span> 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="fc02e-110">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="fc02e-110">Parameters</span></span>

 <span data-ttu-id="fc02e-111">_pxloper_(**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="fc02e-111">_pxloper_ (**LPXLOPER**)</span></span>
  
 <span data-ttu-id="fc02e-112">_pxloper12_(**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="fc02e-112">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="fc02e-113">����Ώۂ� **XLOPER**/ **XLOPER12** �ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="fc02e-113">Pointer to the **XLOPER**/ **XLOPER12** to be freed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fc02e-114">��</span><span class="sxs-lookup"><span data-stu-id="fc02e-114">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fc02e-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc02e-115">See also</span></span>



<span data-ttu-id="fc02e-116">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="fc02e-116">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

