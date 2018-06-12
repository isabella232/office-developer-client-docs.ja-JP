---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- tempactiverow function [excel 2007],TempActiveRow12 function [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798942"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
��ƒ��̃V�[�g�̍s�S�̂̊O���Q�Ƃ�܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐� 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>�p�����[�^�[

 _row_
  
�Q�Ƃ����s�B1 �s�ڂ� 0 �œn�����悤�ɍs�̈����� 0 ����n�܂�܂��BMicrosoft Office Excel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s����J�n���� Excel 2007 �ȍ~�ł́A�ő�l�́A65,535 = 2^16 - 1 �ł���AWORD �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 1,048,575 = 2^20 - 1 �ł��BRW �́AXLCALL.H�� 32 �r�b�g�����t�������Ƃ��Ē�`����܂��B
  
## <a name="return-value"></a>�߂�l

�n�����s�̃Z���� **xltypeRef** �O���Q�Ƃ��Ԃ�܂��B 
  
## <a name="example"></a>��

���̗�ł́A **TempActiveRow12** �֐���g�p���čs 113 ��I����܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

