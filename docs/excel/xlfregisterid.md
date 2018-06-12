---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid function [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798986"
---
# <a name="xlfregisterid"></a><span data-ttu-id="33830-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="33830-104">xlfRegisterId</span></span>

<span data-ttu-id="33830-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="33830-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="33830-p101">Microsoft Excel ����Ăяo���ꂽ DLL �R�}���h����Ăяo�����Ƃ��ł��܂��B�֐������ɓo�^����Ă���ꍇ�́A���̊֐���ēo�^���Ȃ��ŁA�֐��̊����̓o�^ ID ��Ԃ��܂��B�֐����܂��o�^����Ă��Ȃ��ꍇ�́A���̊֐���o�^���āA�o�^ ID ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="33830-p101">Can be called from a DLL that has itself been called by Microsoft Excel. If a function is already registered, it returns the existing register ID for that function without reregistering it. If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="33830-109">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="33830-109">Parameters</span></span>

<span data-ttu-id="33830-110">_pxModuleText_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="33830-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="33830-111">�֐����܂܂�Ă��� DLL �̖��O�B</span><span class="sxs-lookup"><span data-stu-id="33830-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="33830-112">_pxProcedure_(**xltypeStr**または**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="33830-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="33830-p102">������̏ꍇ�́A�Ăяo���֐��̖��O�ł��B�����̏ꍇ�́A�Ăяo���֐��̃G�N�X�|�[�g�̏����ԍ��ł��B���m�Ō��S�ɂ��邽�߂ɁA��ɕ�����\`����g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="33830-p102">If a string, the name of the function to call. If a number, the ordinal export number of the function to call. For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="33830-116">_pxTypeText_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="33830-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="33830-p103">�֐��ւ̂��ׂĂ̈����̌^�Ɗ֐��̖߂�l�̌^��w�肷��A�ȗ��\�ȕ�����B�ڂ����́A�u���v�Z�N�V������Q�Ƃ��Ă��������B **xlAutoRegister** ���\`����X�^���h�A���� DLL (XLL) �ł́A���̈�����ȗ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="33830-p103">An optional string specifying the types of all the arguments to the function and the type of the return value of the function. For more information, see the "Remarks" section. This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="33830-120">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="33830-120">Property value/Return value</span></span>

<span data-ttu-id="33830-121">**XlfUnregister**以降の呼び出しで使用できる関数 (**xltypeNum**) のレジスタ ID を返します。</span><span class="sxs-lookup"><span data-stu-id="33830-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="33830-122">����</span><span class="sxs-lookup"><span data-stu-id="33830-122">Remarks</span></span>

<span data-ttu-id="33830-p104">�o�^ ID �͌�œo�^�������ۂɕK�v�ɂȂ邪�A�ێ��̂��߂ɋC��g�������Ȃ��A�Ƃ����ꍇ�ɁA���̊֐����𗧂��܂��B�܂��A���蓖�Ă�֐��� DLL �ɂ���ꍇ�́A���j���[�A�c�[���A����у{�^���ւ̊��蓖�Ăɂ�𗧂��܂��B</span><span class="sxs-lookup"><span data-stu-id="33830-p104">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering. It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="33830-125">_xlfRegister_ �Ɏw�肳�ꂽ�L����  **pxFunctionText** ������g�p���� DLL �܂��� XLL �֐����o�^����Ă���ꍇ�́A�֐� _xlfEvaluate_ ��  **pxFunctionText** ��n�����ƂŁA���̓o�^ ID ��擾���邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="33830-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33830-126">�֘A����</span><span class="sxs-lookup"><span data-stu-id="33830-126">See also</span></span>

- [<span data-ttu-id="33830-127">REGISTER</span><span class="sxs-lookup"><span data-stu-id="33830-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="33830-128">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="33830-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="33830-129">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="33830-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

