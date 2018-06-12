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
# <a name="xludf"></a><span data-ttu-id="9c86d-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="9c86d-104">xlUDF</span></span>

<span data-ttu-id="9c86d-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9c86d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9c86d-p101">ユーザー定義関数 (UDF) を呼び出します。この関数により、DLL は Visual Basic for Applications (VBA) のユーザー定義関数、XLM マクロ言語の関数、およびその他のアドインに含まれる登録済みの関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="9c86d-p101">Calls a user-defined function (UDF). This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="9c86d-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="9c86d-108">Parameters</span></span>

<span data-ttu-id="9c86d-109">_pxFnRef_(**xltypeRef**、 **xltypeSRef**、 **xltypeStr**または**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="9c86d-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="9c86d-p102">�Ăяo���֐��̎Q�ƁB����̓}�N�� �V�[�g�̃Z���̎Q�ƁA������Ƃ��Ă̊֐��̓o�^���A�܂��͊֐��̓o�^ ID �ɂȂ�܂��B������  **pxFunctionText** ��w�肵�� **xlfRegister** �܂��� _REGISTER_ ��g�p���ēo�^���ꂽ XLL �A�h�C���֐��̏ꍇ�A **xlfEvaluate** ��g�p���Ė��O���������� ID ��擾�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="9c86d-p102">The reference of the function you want to call. This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function. For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="9c86d-113">_pxArg1, ..._</span><span class="sxs-lookup"><span data-stu-id="9c86d-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="9c86d-p103">���[�U�[��\`�֐��ɓn����� 0 �ȏ�̈����BExcel 2007 ���O�̃o�[�W�����ł́A���̊֐���Ăяo���Ƃ��ɁA�ő� 29 �� ( _pxFnRef_ ��܂߂� 30��) �̒ǉ��̈�����n���܂��BExcel 2007 �ȍ~�ł́A���̐����� 254 �� (  _pxFnRef_ ��܂߂� 255 ��) �ɂ܂Ŋɘa����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="9c86d-p103">Zero or more arguments to the user-defined function. When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_. Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="9c86d-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9c86d-117">Return value</span></span>

<span data-ttu-id="9c86d-118">���[�U�[��\`�֐����Ԃ��l��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="9c86d-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="9c86d-119">��</span><span class="sxs-lookup"><span data-stu-id="9c86d-119">Example</span></span>

<span data-ttu-id="9c86d-p104">���̗�ł́ABOOK1.XLS �̃V�[�g Macro1 �� **TestMacro** ����s���܂��B�}�N���� Macro1 �Ƃ������O�̃V�[�g��ɂ��邱�Ƃ�m�F���Ă��������B</span><span class="sxs-lookup"><span data-stu-id="9c86d-p104">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS. Make sure that the macro is on a sheet named Macro1.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="9c86d-122">�֘A����</span><span class="sxs-lookup"><span data-stu-id="9c86d-122">See also</span></span>

- [<span data-ttu-id="9c86d-123">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="9c86d-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

