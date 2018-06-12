---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- xludf function [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799000"
---
# <a name="xludf"></a>xlUDF

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
ユーザー定義関数 (UDF) を呼び出します。この関数により、DLL は Visual Basic for Applications (VBA) のユーザー定義関数、XLM マクロ言語の関数、およびその他のアドインに含まれる登録済みの関数を呼び出すことができます。
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>�p�����[�^�[

_pxFnRef_(**xltypeRef**、 **xltypeSRef**、 **xltypeStr**または**xltypeNum**)
  
�Ăяo���֐��̎Q�ƁB����̓}�N�� �V�[�g�̃Z���̎Q�ƁA������Ƃ��Ă̊֐��̓o�^���A�܂��͊֐��̓o�^ ID �ɂȂ�܂��B������  **pxFunctionText** ��w�肵�� **xlfRegister** �܂��� _REGISTER_ ��g�p���ēo�^���ꂽ XLL �A�h�C���֐��̏ꍇ�A **xlfEvaluate** ��g�p���Ė��O���������� ID ��擾�ł��܂��B 
  
_pxArg1, ..._
  
���[�U�[��`�֐��ɓn����� 0 �ȏ�̈����BExcel 2007 ���O�̃o�[�W�����ł́A���̊֐���Ăяo���Ƃ��ɁA�ő� 29 �� ( _pxFnRef_ ��܂߂� 30��) �̒ǉ��̈�����n���܂��BExcel 2007 �ȍ~�ł́A���̐����� 254 �� (  _pxFnRef_ ��܂߂� 255 ��) �ɂ܂Ŋɘa����Ă��܂��B
  
## <a name="return-value"></a>�߂�l

���[�U�[��`�֐����Ԃ��l��Ԃ��܂��B
  
## <a name="example"></a>��

���̗�ł́ABOOK1.XLS �̃V�[�g Macro1 �� **TestMacro** ����s���܂��B�}�N���� Macro1 �Ƃ������O�̃V�[�g��ɂ��邱�Ƃ�m�F���Ă��������B 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a>�֘A����

- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

