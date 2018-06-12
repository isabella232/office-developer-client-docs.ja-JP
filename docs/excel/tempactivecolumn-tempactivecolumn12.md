---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- tempactivecolumn12 function [excel 2007],TempActiveColumn function [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798947"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
��ƒ��̃V�[�g�̗�S�̂̊O���Q�Ƃ�܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>�p�����[�^�[

 _col_(**バイト**)
  
�Q�Ƃ�����B�� A �� 0 �œn�����悤�ɁA���̒l�� 0 ����n�܂�l�ɂȂ��Ă��܂��BMicrosoft Office Excel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s����J�n���� Excel 2007 �ȍ~�ł́A�ő�l�� 255 = 2^8 - 1 �ł���ABYTE �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 16,383 = 2^14 - 1 �ł��BCOL �́AXLCALL.H�� 32 �r�b�g�����t�������Ƃ��Ē�`����܂��B
  
## <a name="return-value"></a>�߂�l

�n������� **xltypeRef** �O���Q�Ƃ�Ԃ��܂��B 
  
## <a name="example"></a>��

���̗�ł́A **TempActiveColumn12** ��g�p���āA�� B �S�̂�I����܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

