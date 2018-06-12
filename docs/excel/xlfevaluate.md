---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- xlfevaluate function [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798970"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel �̃p�[�T�[�Ɗ֐��G�o�����G�[�^�[��g�p���āA���[�N�V�[�g�̃Z���ɓ��͂ł���C�ӂ̎���]�����܂��B
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxFormulaText (xltypeStr)_
  
�]�����镶����ł��B�擪�̓��� (=) �͏ȗ��\�ł��B������͔C�ӂ̃e�L�X�g�ɂł��܂��B����͐����ɁA���[�N�V�[�g�܂��̓}�N�� �V�[�g�̃Z���ɓ��͂ł��܂��B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

������̕]�����ʂ�Ԃ��܂��B����� **xltypeNum**�A **xltypeStr**�A **xltypeBool**�A **xltypeErr**�A **xltypeNil**�A **xltypeMulti** �̂����ꂩ�ɂȂ�܂��B
  
## <a name="remarks"></a>����

������ɂ͊֐��݂̂�܂߂邱�Ƃ��ł��܂��B�R�}���h�͑Ή����܂���B����́A�����o�[�� **F9** ��������ꍇ�Ɠ����ł��B **xlfEvaluate** ���X���b�h �Z�[�t�Ƃ��ēo�^���ꂽ XLL ���[�N�V�[�g�֐�����Ăяo���ꂽ�ꍇ�A���ɂ̓X���b�h�Z�[�t�֐��݂̂�܂߂�K�v������܂��B 
  
**XlfEvaluate**関数の主な用途は、シートのいずれかの方法が定義された名前に割り当てられた値または DLL 内で定義されている非表示の名前を確認する Dll をできるようにすることです。 DLL または XLL 内でワークシート名付けます少なくとも感嘆符 (!)、DLL の外部で解釈されることを確認するのには注意してください。 詳細については、[名前の評価とその他のワークシートの数式の表現](evaluating-names-and-other-worksheet-formula-expressions.md)を参照してください。
  
 **xlfEvaluate** �́A�J����Ă��Ȃ��O���V�[�g�ւ̎Q�Ƃ̕]���ɂ͎g�p�ł��܂���B 
  
## <a name="example"></a>��

���̗�ł́A **xlfEvaluate** ��g�p���ċ����I�Ƀe�L�X�g "!B38" ��Z�� B38 �̓�e�ɂ��܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. この関数は、コマンド マクロ (**xlcAlert**) を呼び出し、マクロ シートまたはマクロ コマンドとして呼び出されたときにのみ正常に動作します。
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a>関連項目

- [�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)

