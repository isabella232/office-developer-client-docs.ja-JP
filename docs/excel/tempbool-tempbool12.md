---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- tempbool function [excel 2007],TempBool12 function [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798946"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**Boolean** /  �� **FALSE** ��܂ވꎞ **XLOPER********XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>�p�����[�^�[

 _b_ (**int**)
  
**FALSE** ��Ԃ��ɂ� 0 ��g�p���܂��B **TRUE** ��Ԃ��ɂ͂���ȊO�̒l��g�p���܂��B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

�n���ꂽ�_���l��܂� **xltypeBool** **Boolean** ��Ԃ��܂��B 
  
## <a name="example"></a>��

���̗�ł́A **TempBool12** �֐���g�p���ăX�e�[�^�X �o�[��������܂��B [Excel/Excel12f](excel-excel12f.md) �֐����Ăяo�����ƁA�ꎞ���������������܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

