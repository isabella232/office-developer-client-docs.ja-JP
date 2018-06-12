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
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a><span data-ttu-id="c0704-104">名およびその他のワークシートの数式の式を評価します。</span><span class="sxs-lookup"><span data-stu-id="c0704-104">Evaluating names and other worksheet formula expressions</span></span>

<span data-ttu-id="c0704-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c0704-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c0704-p101">Excel ���AC API �Ō��J����ł�d�v�ȋ@�\�� 1 �́A���[�N�V�[�g�ɍ��@�I�ɓ��͂ł��镶���񎮂�P��̒l��l�̔z��ɕϊ�����@�\�ł��B����́A��\`���ꂽ���O�̃R���e���c��ǂݎ��K�v������ XLL �֐��ƃR�}���h�ȂǂɂƂ��ĕs���ł��B���̋@�\�́A�ȉ��̗�Ɏ����悤�ɁA[xlfEvaluate �֐�](xlfevaluate.md)�Ō��J����܂��B</span><span class="sxs-lookup"><span data-stu-id="c0704-p101">One of the most important features that Excel exposes through the C API is the ability to convert any string formula that can legally be entered into a worksheet to a value, or array of values. This is essential for XLL functions and commands that must read the contents of defined names, for example. This ability is exposed through the [xlfEvaluate function](xlfevaluate.md), as shown in this example.</span></span>
  
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

<span data-ttu-id="c0704-p102">���[�N�V�[�g����A���ꎩ�̂����ŕ]������ꍇ�A���Ȃ��Ƃ�A���O�� �e!�f �Ƃ����v���t�B�b�N�X�Ŏn�߂�K�v������܂��B�������Ȃ��ƁAExcel �� Dll �p�ɗ\�񂳂�Ă����\���̖��O��ԓ�ł��̖��O������悤�Ƃ��܂��B[xlfSetName �֐�](xlfsetname.md)��g���āA��\���� DLL ���̍쐬�ƍ폜���ł��܂��B��\���� DLL �������[�N�V�[�g�����Ɋ֌W�Ȃ��A [xlfGetDef](xlfsetname.md) �֐���g���āA��**** �ł�擾�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="c0704-p102">Note that when you are evaluating a worksheet name, either on its own or in a formula, you must prefix the name with '!', at least. Otherwise, Excel tries to find the name in a hidden namespace reserved for DLLs. You can create and delete hidden DLL names using the [xlfSetName function](xlfsetname.md). You can get the definition of any defined name, whether it is a hidden DLL name or a worksheet name, using the **xlfGetDef** function.</span></span> 
  
<span data-ttu-id="c0704-113">���[�N�V�[�g���S�̂̎w��́A���̂悤�Ȍ\`���ł��B</span><span class="sxs-lookup"><span data-stu-id="c0704-113">The full specification for a worksheet name takes the following form:</span></span>
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
<span data-ttu-id="c0704-p103">Excel 2007 �ł́A�������̐V�����t�@�C���g���q����������܂����B���� Excel �Z�b�V�����ŊJ���Ă���u�b�N�Ԃɂ����܂��ȉӏ����Ȃ��ꍇ�́A�p�X�A�u�b�N���A�V�[�g����ȗ����邱�Ƃ��ł��܂�</span><span class="sxs-lookup"><span data-stu-id="c0704-p103">Note that Excel 2007 introduced a number of new file extensions. You can omit the path, the workbook name, and the sheet name where there is no ambiguity among the open workbooks in this Excel session.</span></span> 
  
<span data-ttu-id="c0704-p104">���̗�́A��ƒ��̃��[�N�V�[�g�̎�  `COUNT(A1:IV65536)` ��]�����āA���ʂ�\�����܂��B�͈̓A�h���X�� '!' �Ƃ����v���t�B�b�N�X�Ŏn�߂�K�v�����邱�Ƃɒ��ӂ��Ă��������B����́AXLM �}�N�� �V�[�g�͈͎̔Q�Ƃ̋K���ƈ�v���Ă��܂��BC API XLM �́A���̋K���ɏ]���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="c0704-p104">The next example evaluates the formula  `COUNT(A1:IV65536)` for the active worksheet and displays the result. Note the need to prefix the range address with '!', which is consistent with the range reference convention on XLM macro sheets. The C API XLM follows this convention:</span></span> 
  
- <span data-ttu-id="c0704-p105">`=A1` ���݂̃}�N�� �V�[�g�̃Z�� A1 �ւ̎Q�ƁB(XLL �ɂ��Ă͒�\`����Ă��܂���)�B</span><span class="sxs-lookup"><span data-stu-id="c0704-p105">`=A1` A reference to cell A1 on the current macro sheet. (Not defined for XLLs).</span></span> 
  
- <span data-ttu-id="c0704-121">`=!A1` ��ƒ��̃V�[�g (���[�N�V�[�g���}�N�� �V�[�g��w��ł��܂�) �̃Z�� A1 �ւ̎Q�ƁB</span><span class="sxs-lookup"><span data-stu-id="c0704-121">`=!A1` A reference to cell A1 on the active sheet (which could be a worksheet or macro sheet)</span></span> 
  
- <span data-ttu-id="c0704-122">`=Sheet1!A1` �w�肳�ꂽ�V�[�g (���̏ꍇ�� Sheet1) �̃Z�� A1 �ւ̎Q�ƁB</span><span class="sxs-lookup"><span data-stu-id="c0704-122">`=Sheet1!A1` A reference to cell A1 on the specified sheet, Sheet1 in this case.</span></span> 
  
- <span data-ttu-id="c0704-123">`=[Book1.xls]Sheet1!A1` �w�肳�ꂽ�u�b�N�̎w�肳�ꂽ�V�[�g�̃Z�� A1 �ւ̎Q�ƁB</span><span class="sxs-lookup"><span data-stu-id="c0704-123">`=[Book1.xls]Sheet1!A1` A reference to cell A1 on the specified sheet in the specified workbook.</span></span> 
  
<span data-ttu-id="c0704-124">XLL は、値の先頭感嘆符 (**!**) に参照を変換できません。</span><span class="sxs-lookup"><span data-stu-id="c0704-124">In an XLL, a reference without a leading exclamation point (**!**) cannot be converted to a value.</span></span> <span data-ttu-id="c0704-125">ないため、現在のマクロ シートがないためです。</span><span class="sxs-lookup"><span data-stu-id="c0704-125">It has no meaning because there is no current macro sheet.</span></span> <span data-ttu-id="c0704-126">メモの先頭の等号記号 (**=**) オプションで、次の例では省略するとします。</span><span class="sxs-lookup"><span data-stu-id="c0704-126">Note that a leading equals sign (**=**) is optional and is omitted in the next example.</span></span>
  
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

<span data-ttu-id="c0704-127">�܂��A **xlfEvaluate** �֐���g���āAXLL �֐��̓o�^ ID ��o�^����Ă��閼�O����擾���܂��B���̌�A [xlUDF �֐�](xludf.md)��g���Ă��̊֐���Ăяo�����߂ɁA�擾���� XLL �֐��̓o�^ ID ��g�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="c0704-127">You can also use the **xlfEvaluate** function to retrieve the registration ID of an XLL function from its registered name, which can then be used to call that function using the [xlUDF function](xludf.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="c0704-p107">[!����] �o�^����Ă��閼�O�́A **xlUDF** �֐��ɒ��ړn�����Ƃ��ł��܂��B�܂�A���O��]������ ID ��擾�����ɁA **xlUDF** ��Ăяo�����Ƃ��ł���Ƃ������Ƃł��B�������A�֐�����x��Ăяo���ꍇ�A�o�^ ID ��g���ČĂяo���ق��������Ȃ�܂��B</span><span class="sxs-lookup"><span data-stu-id="c0704-p107">The registered name can be passed directly to the **xlUDF** function. This means that you can avoid having to evaluate the name to get the ID before calling **xlUDF**. However, if the function is to be called many times, calling it by using the registration ID is faster.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0704-131">�֘A����</span><span class="sxs-lookup"><span data-stu-id="c0704-131">See also</span></span>

- <span data-ttu-id="c0704-132">[Excel ���[�N�V�[�g�Ǝ��̕]��](excel-worksheet-and-expression-evaluation.md)</span><span class="sxs-lookup"><span data-stu-id="c0704-132">[Excel Worksheet and Expression Evaluation](excel-worksheet-and-expression-evaluation.md)</span></span>
- <span data-ttu-id="c0704-133">[���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f�������](permitting-user-breaks-in-lengthy-operations.md)</span><span class="sxs-lookup"><span data-stu-id="c0704-133">[Permitting User Breaks in Lengthy Operations](permitting-user-breaks-in-lengthy-operations.md)</span></span>
- [<span data-ttu-id="c0704-134">Excel XLL SDK �̊T�v</span><span class="sxs-lookup"><span data-stu-id="c0704-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

