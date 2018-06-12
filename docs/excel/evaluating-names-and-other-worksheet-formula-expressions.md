---
title: 名およびその他のワークシートの数式の式を評価します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],worksheets [Excel 2007], name evaluation,evaluating expressions [Excel 2007],evaluating worksheet names [Excel 2007],expressions [Excel 2007], evaluating,names [Excel 2007], evaluating,name evaluation [Excel 2007],strings [Excel 2007], converting to values,xlfEvaluate function [Excel 2007],worksheets [Excel 2007], expression evaluation
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 9d726d89c859e2f7428b459971d5d13586f144e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798796"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>名およびその他のワークシートの数式の式を評価します。

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Excel ���AC API �Ō��J����ł�d�v�ȋ@�\�� 1 �́A���[�N�V�[�g�ɍ��@�I�ɓ��͂ł��镶���񎮂�P��̒l��l�̔z��ɕϊ�����@�\�ł��B����́A��`���ꂽ���O�̃R���e���c��ǂݎ��K�v������ XLL �֐��ƃR�}���h�ȂǂɂƂ��ĕs���ł��B���̋@�\�́A�ȉ��̗�Ɏ����悤�ɁA[xlfEvaluate �֐�](xlfevaluate.md)�Ō��J����܂��B
  
```C
int WINAPI evaluate_name_example(void)
{
  wchar_t *expression = L"\016!MyDefinedName";
  XLOPER12 xNameText, xNameValue;
  xNameText.xltype = xltypeStr;
  xNameText.val.str = expression;
// Try to evaluate the name. Will fail with a #NAME? error
// if MyDefinedName is not defined in the active workbook.
  Excel12(xlfEvaluate, &xNameValue, 1, &xNameText);
// Attempt to convert the value to a string and display it in
// an alert dialog. This fails if xNameValue is an error value.
  Excel12(xlcAlert, 0, 1, &xNameValue);
// Must free xNameValue in case MyDefinedName evaluated to a string
  Excel12(xlFree, 0, 1, &xNameValue);
  return 1;
}
```

���[�N�V�[�g����A���ꎩ�̂����ŕ]������ꍇ�A���Ȃ��Ƃ�A���O�� �e!�f �Ƃ����v���t�B�b�N�X�Ŏn�߂�K�v������܂��B�������Ȃ��ƁAExcel �� Dll �p�ɗ\�񂳂�Ă����\���̖��O��ԓ�ł��̖��O������悤�Ƃ��܂��B[xlfSetName �֐�](xlfsetname.md)��g���āA��\���� DLL ���̍쐬�ƍ폜���ł��܂��B��\���� DLL �������[�N�V�[�g�����Ɋ֌W�Ȃ��A [xlfGetDef](xlfsetname.md) �֐���g���āA��**** �ł�擾�ł��܂��B 
  
���[�N�V�[�g���S�̂̎w��́A���̂悤�Ȍ`���ł��B
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Excel 2007 �ł́A�������̐V�����t�@�C���g���q����������܂����B���� Excel �Z�b�V�����ŊJ���Ă���u�b�N�Ԃɂ����܂��ȉӏ����Ȃ��ꍇ�́A�p�X�A�u�b�N���A�V�[�g����ȗ����邱�Ƃ��ł��܂� 
  
���̗�́A��ƒ��̃��[�N�V�[�g�̎�  `COUNT(A1:IV65536)` ��]�����āA���ʂ�\�����܂��B�͈̓A�h���X�� '!' �Ƃ����v���t�B�b�N�X�Ŏn�߂�K�v�����邱�Ƃɒ��ӂ��Ă��������B����́AXLM �}�N�� �V�[�g�͈͎̔Q�Ƃ̋K���ƈ�v���Ă��܂��BC API XLM �́A���̋K���ɏ]���Ă��܂��B 
  
- `=A1` ���݂̃}�N�� �V�[�g�̃Z�� A1 �ւ̎Q�ƁB(XLL �ɂ��Ă͒�`����Ă��܂���)�B 
  
- `=!A1` ��ƒ��̃V�[�g (���[�N�V�[�g���}�N�� �V�[�g��w��ł��܂�) �̃Z�� A1 �ւ̎Q�ƁB 
  
- `=Sheet1!A1` �w�肳�ꂽ�V�[�g (���̏ꍇ�� Sheet1) �̃Z�� A1 �ւ̎Q�ƁB 
  
- `=[Book1.xls]Sheet1!A1` �w�肳�ꂽ�u�b�N�̎w�肳�ꂽ�V�[�g�̃Z�� A1 �ւ̎Q�ƁB 
  
XLL は、値の先頭感嘆符 (**!**) に参照を変換できません。 ないため、現在のマクロ シートがないためです。 メモの先頭の等号記号 (**=**) オプションで、次の例では省略するとします。
  
```C
int WINAPI evaluate_expression_example(void)
{
    wchar_t *expression = L"\022COUNT(!A1:IV65536)";
    XLOPER12 xExprText, xExprValue;
    xExprText.xltype = xltypeStr;
    xExprText.val.str = expression;
// Try to evaluate the formula.
    Excel12(xlfEvaluate, &xExprValue, 1, &xExprText);
// Attempt to convert the value to a string and display it in
// an alert dialog. Will fail if xExprValue is an error.
    Excel12(xlcAlert, 0, 1, &xExprValue);
// Not strictly necessary, as COUNT never returns a string
// but does no harm.
    Excel12(xlFree, 0, 1, &xExprValue);
    return 1;
}
```

�܂��A **xlfEvaluate** �֐���g���āAXLL �֐��̓o�^ ID ��o�^����Ă��閼�O����擾���܂��B���̌�A [xlUDF �֐�](xludf.md)��g���Ă��̊֐���Ăяo�����߂ɁA�擾���� XLL �֐��̓o�^ ID ��g�����Ƃ��ł��܂��B
  
> [!NOTE]
> [!����] �o�^����Ă��閼�O�́A **xlUDF** �֐��ɒ��ړn�����Ƃ��ł��܂��B�܂�A���O��]������ ID ��擾�����ɁA **xlUDF** ��Ăяo�����Ƃ��ł���Ƃ������Ƃł��B�������A�֐�����x��Ăяo���ꍇ�A�o�^ ID ��g���ČĂяo���ق��������Ȃ�܂��B 
  
## <a name="see-also"></a>�֘A����

- [Excel ���[�N�V�[�g�Ǝ��̕]��](excel-worksheet-and-expression-evaluation.md)
- [���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f�������](permitting-user-breaks-in-lengthy-operations.md)
- [Excel XLL SDK �̊T�v](getting-started-with-the-excel-xll-sdk.md)

