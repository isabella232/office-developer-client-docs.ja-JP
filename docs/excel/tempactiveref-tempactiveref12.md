---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- tempactiveref function [excel 2007],TempActiveRef12 function [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798944"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
��ƒ��̃��[�N�V�[�g��ɂ��钷���`�̃u���b�N�̃Z���ւ̊O���Q�Ƃ�܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>�p�����[�^�[

 _rwFirst_
  
�Q�Ƃ̊J�n�s�B
  
 _rwLast_
  
�Q�Ƃ̏I���s�B
  
�s�̈����� 0 ����n�܂�A1 �s�ڂ� 0 �Ƃ��ēn����܂��BMicrosoft Office Excel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�́A65,535 = 2^16 - 1 �ł���A���ꂪ WORD �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 1,048,575 = 2^20 - 1 �ł��BRW �́AXLCALL.H�� 32 �r�b�g�����t�������Ƃ��Ē�`����܂��B
  
 _colFirst_
  
�Q�Ƃ̊J�n��ԍ��B
  
 _colLast_
  
�Q�Ƃ̏I����ԍ��B
  
��̈����� 0 ����n�܂�A�� A �� 0 �Ƃ��ēn����܂��BExcel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�́A255 = 2^8 - 1 �ł���A���ꂪ BYTE �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 16,383 = 2^14 - 1 �ł��BCOL �́AXLCALL.H�� 32 �r�b�g�����t�������Ƃ��Ē�`����܂��B
  
## <a name="return-value"></a>�߂�l

�n����钷���`�̃u���b�N�̃Z���ւ� **xltypeRef** �O���Q�Ƃ�Ԃ��܂��B 
  
## <a name="example"></a>��

���̗�ł́A **TempActiveRef12** �֐���g�p���� A105:C110 �̃Z����I����Ă��܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

