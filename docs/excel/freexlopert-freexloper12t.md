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
# <a name="freexlopertfreexloper12t"></a>FreeXLOperT/FreeXLOper12T

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**XLOPER**/ **XLOPER12** �Ɋ֘A�t�����Ă����������������� Framework �֐��B���̊֐��́ADLL ��ł� malloc �̌Ăяo���Ń����������蓖�Ă�ꂽ���Ƃ�O��Ƃ��Ă��܂��BMicrosoft Excel�A���̑��̉��炩�̕��@�A�܂��͑��̃v���Z�X�ɂ�胁���������蓖�Ă�ꂽ�ꍇ�́A���̊֐���g�p���ă������������ׂ��ł͂���܂���B [xlFree](xlfree.md) ��g�p���āA **XLOPER**/ **XLOPER12** �� Excel �����蓖�Ă��������������܂��B 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxloper_(**LPXLOPER**)
  
 _pxloper12_(**LPXLOPER12**)
  
����Ώۂ� **XLOPER**/ **XLOPER12** �ւ̃|�C���^�[�B 
  
## <a name="example"></a>��

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

## <a name="see-also"></a>関連項目



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

