---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- convertxlref12toxlref function [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 826428edb57eba9e17d601164aa8b4b797fc8929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798770"
---
# <a name="convertxlref12toxlref"></a>ConvertXLRef12ToXLRef

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**XLREF12** ���� **XLREF** �ւ̕ϊ�����s���܂��B
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxRef12_(**LPXLREF12**)
  
�\�[�X�̎Q�ƍ\���̂ւ̃|�C���^�[�B
  
 _pxRef_(**LPXLREF**)
  
�ϊ������l���z�u�����^�[�Q�b�g�̎Q�ƍ\���̂ւ̃|�C���^�[�B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

 �ϊ������������ꍇ�� **TRUE**�B����ȊO�̏ꍇ�� **FALSE**�B 
  
## <a name="remarks"></a>����

�w�肵���Q�Ƃ��ȑO�̃o�[�W�����ł̓T�|�[�g����Ă��Ȃ� Excel 2007 ���[�N�V�[�g�̕�����Q�Ƃ��Ă���ꍇ�A **XLREF12** ���� **XLREF** �ւ̕ϊ��͎��s���܂��B 
  
## <a name="example"></a>��

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRef12ToXLRef(LPXLREF12 pxref12, LPXLREF pxref)
{
   if (pxref12->rwLast >= pxref12->rwFirst && pxref12->colLast >= pxref12->colFirst)
   {
      if (pxref12->rwFirst >=0 && pxref12->colFirst >= 0)
      {
         if (pxref12->rwLast < rwMaxO8 && pxref12->colLast < colMaxO8)
         {
            pxref->rwFirst = (WORD)pxref12->rwFirst;
            pxref->rwLast = (WORD)pxref12->rwLast;
            pxref->colFirst = (BYTE)pxref12->colFirst;
            pxref->colLast = (BYTE)pxref12->colLast;
            return TRUE;
         }
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a>関連項目



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

