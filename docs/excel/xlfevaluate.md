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
# <a name="xlfevaluate"></a><span data-ttu-id="d5755-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="d5755-104">xlfEvaluate</span></span>

 <span data-ttu-id="d5755-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d5755-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d5755-106">Microsoft Excel �̃p�[�T�[�Ɗ֐��G�o�����G�[�^�[��g�p���āA���[�N�V�[�g�̃Z���ɓ��͂ł���C�ӂ̎���]�����܂��B</span><span class="sxs-lookup"><span data-stu-id="d5755-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="d5755-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="d5755-107">Parameters</span></span>

 <span data-ttu-id="d5755-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="d5755-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="d5755-p101">�]�����镶����ł��B�擪�̓��� (=) �͏ȗ��\�ł��B������͔C�ӂ̃e�L�X�g�ɂł��܂��B����͐����ɁA���[�N�V�[�g�܂��̓}�N�� �V�[�g�̃Z���ɓ��͂ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="d5755-p101">The string to be evaluated. A leading equal sign (=) is optional. The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d5755-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="d5755-112">Property value/Return value</span></span>

<span data-ttu-id="d5755-113">������̕]�����ʂ�Ԃ��܂��B����� **xltypeNum**�A **xltypeStr**�A **xltypeBool**�A **xltypeErr**�A **xltypeNil**�A **xltypeMulti** �̂����ꂩ�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="d5755-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5755-114">����</span><span class="sxs-lookup"><span data-stu-id="d5755-114">Remarks</span></span>

<span data-ttu-id="d5755-p102">������ɂ͊֐��݂̂�܂߂邱�Ƃ��ł��܂��B�R�}���h�͑Ή����܂���B����́A�����o�[�� **F9** ��������ꍇ�Ɠ����ł��B **xlfEvaluate** ���X���b�h �Z�[�t�Ƃ��ēo�^���ꂽ XLL ���[�N�V�[�g�֐�����Ăяo���ꂽ�ꍇ�A���ɂ̓X���b�h�Z�[�t�֐��݂̂�܂߂�K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="d5755-p102">The string can contain only functions, not command equivalents. It is equivalent to pressing **F9** from the formula bar. If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="d5755-118">**XlfEvaluate**関数の主な用途は、シートのいずれかの方法が定義された名前に割り当てられた値または DLL 内で定義されている非表示の名前を確認する Dll をできるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="d5755-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL.</span></span> <span data-ttu-id="d5755-119">DLL または XLL 内でワークシート名付けます少なくとも感嘆符 (!)、DLL の外部で解釈されることを確認するのには注意してください。</span><span class="sxs-lookup"><span data-stu-id="d5755-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="d5755-120">詳細については、[名前の評価とその他のワークシートの数式の表現](evaluating-names-and-other-worksheet-formula-expressions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5755-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="d5755-121">**xlfEvaluate** �́A�J����Ă��Ȃ��O���V�[�g�ւ̎Q�Ƃ̕]���ɂ͎g�p�ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="d5755-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d5755-122">��</span><span class="sxs-lookup"><span data-stu-id="d5755-122">Example</span></span>

<span data-ttu-id="d5755-123">���̗�ł́A **xlfEvaluate** ��g�p���ċ����I�Ƀe�L�X�g "!B38" ��Z�� B38 �̓�e�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="d5755-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="d5755-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="d5755-124"></span></span> <span data-ttu-id="d5755-125">この関数は、コマンド マクロ (**xlcAlert**) を呼び出し、マクロ シートまたはマクロ コマンドとして呼び出されたときにのみ正常に動作します。</span><span class="sxs-lookup"><span data-stu-id="d5755-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="d5755-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5755-126">See also</span></span>

- [<span data-ttu-id="d5755-127">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="d5755-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

