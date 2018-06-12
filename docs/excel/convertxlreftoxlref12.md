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
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798777"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**XLREF** �� **XLREF12** �ɕϊ����悤�Ƃ��� Framework �֐��B
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxRef_(**LPXLREF**)
  
�\�[�X�̎Q�ƍ\���̂ւ̃|�C���^�[�B
  
 _pxRef12_(**LPXLREF12**)
  
�ϊ������l���z�u�����^�[�Q�b�g�̎Q�ƍ\���̂ւ̃|�C���^�[�B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

 �ϊ������������ꍇ�� **TRUE**�B����ȊO�̏ꍇ�� **FALSE**�B 
  
## <a name="remarks"></a>����

�n���ꂽ **XLREF** ���L���ȏꍇ�́A���̑���͏�ɐ�������͂��ł��B���΂ɁA�������ꂽ�Q�Ƃ��ȑO�̃o�[�W�����ŃT�|�[�g����Ă��Ȃ� Excel 2007 ���[�N�V�[�g�̈ꕔ��Q�Ƃ��Ă���ꍇ�́A **ConvertXLRef12ToXLRef** ���s�� **XLREF12** ���� [XLREF](convertxlref12toxlref.md) �ւ̕ϊ��͎��s���܂��B
  
## <a name="example"></a>��

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

## <a name="see-also"></a>関連項目



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

