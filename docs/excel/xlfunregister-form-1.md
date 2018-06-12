---
title: xlfUnregister (�`�� 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister function [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798981"
---
# <a name="xlfunregister-form-1"></a><span data-ttu-id="e7f22-104">xlfUnregister (�\`�� 1)</span><span class="sxs-lookup"><span data-stu-id="e7f22-104">xlfUnregister (Form 1)</span></span>

<span data-ttu-id="e7f22-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e7f22-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e7f22-p101">Microsoft Excel �ɂ���Ă��ꎩ�̂��Ăяo����� DLL �� XLL �R�}���h����Ăяo�����Ƃ��ł��܂��B����́A **UNREGISTER** �� Excel XLM �}�N�� �V�[�g����Ăяo���̂Ɠ����ł��B</span><span class="sxs-lookup"><span data-stu-id="e7f22-p101">Can be called from a DLL or XLL command that has itself been called by Microsoft Excel. This is equivalent to calling **UNREGISTER** from an Excel XLM macro sheet.</span></span> 
  
<span data-ttu-id="e7f22-108">**xlfUnregister** �́A2 �̌\`���ŌĂяo�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="e7f22-108">**xlfUnregister** can be called in two forms:</span></span> 
  
- <span data-ttu-id="e7f22-109">�\`�� 1:�X�̃R�}���h��֐��̓o�^�������܂��B</span><span class="sxs-lookup"><span data-stu-id="e7f22-109">Form 1: Unregisters an individual command or function.</span></span>
    
- <span data-ttu-id="e7f22-110">�\`�� 2XLL �̃A�����[�h�Ɣ�A�N�e�B�u����s���܂��B</span><span class="sxs-lookup"><span data-stu-id="e7f22-110">Form 2: Unloads and deactivates an XLL.</span></span>
    
<span data-ttu-id="e7f22-p102">�\`�� 1 �ŌĂяo�����ƁA���̊֐��́A **xlfRegister** �܂��� **REGISTER** ��g�p���Ċ��ɓo�^����Ă��� DLL �֐��܂��̓R�}���h�̎g�p�J�E���g����炵�܂��B���Ɏg�p�J�E���gDLL ��̂��ׂĂ̊֐��̎g�p�J�E���g�� 0 �ɂȂ�ƁADLL �̓���������A�����[�h����܂��B</span><span class="sxs-lookup"><span data-stu-id="e7f22-p102">Called in Form 1, this function reduces the use count of a DLL function or command that was previously registered using **xlfRegister** or **REGISTER**. If the usage count is already zero, this function has no effect. When the use count of all the functions in a DLL reaches zero, the DLL is unloaded from memory.</span></span>
  
<span data-ttu-id="e7f22-p103">**xlfRegister** (�__ ���܂��B�֐��̓o�^��������ꍇ�́A�֐��E�B�U�[�h�ɂ��̊֐��̖��O���\������Ȃ��Ȃ�悤�ɁA **xlfSetName** ��g�p���Ă��̖��O��폜����K�v������܂��B�ڂ����́u [Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B</span><span class="sxs-lookup"><span data-stu-id="e7f22-p103">**xlfRegister** (Form 1) also defines a hidden name which is the function text argument,  _pxFunctionText_, and which evaluates to the function or command's registration ID. When unregistering the function, this name should be deleted using **xlfSetName** so that the function name is no longer listed by the Function Wizard. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a><span data-ttu-id="e7f22-117">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="e7f22-117">Parameters</span></span>

<span data-ttu-id="e7f22-118">_pxRegisterId_(**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="e7f22-118">_pxRegisterId_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="e7f22-119">�o�^��������֐��̓o�^ ID�B</span><span class="sxs-lookup"><span data-stu-id="e7f22-119">The registration ID of the function to be unregistered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e7f22-120">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="e7f22-120">Property value/Return value</span></span>

<span data-ttu-id="e7f22-121">成功した場合を返します**TRUE** (**xltypeBool**)、それ以外の場合は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="e7f22-121">If successful, returns **TRUE** (**xltypeBool**), otherwise it returns FALSE.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7f22-122">����</span><span class="sxs-lookup"><span data-stu-id="e7f22-122">Remarks</span></span>

<span data-ttu-id="e7f22-p104">�֐��̓o�^ ID �́A�֐��̍ŏ��̓o�^���� **xlfRegister** �ɂ���ĕԂ���܂��B�܂��A [xlfRegisterId �֐�](xlfregisterid.md) �܂��� [xlfEvaluate �֐�](xlfevaluate.md)��Ăяo���Ď擾���邱�Ƃ�ł��܂��B�֐����܂��o�^����Ă��Ȃ��ꍇ�́AxlfRegisterId �͂��̊֐���o�^���悤�Ƃ��邱�Ƃɂ����ӂ��������B���̂��߁A�P�Ɋ֐��̓o�^��������ړI�� ID ��擾���悤�Ƃ��Ă���̂ł���΁A�o�^���ꂽ���O�� **xlfEvaluate** �ɓn���� ID ��擾���邱�Ƃ�����߂��܂��B�֐����o�^����Ă��Ȃ��ꍇ�A **xlfEvaluate** �� #NAME? �G���[�Ŏ��s���܂��B</span><span class="sxs-lookup"><span data-stu-id="e7f22-p104">The registration ID of the function is returned by **xlfRegister** when the function is first registered. It can also be obtained by calling the [xlfRegisterId function](xlfregisterid.md) or the [xlfEvaluate function](xlfevaluate.md). Note that xlfRegisterId tries to register the function if it has not already been registered. For this reason, if you are only trying to get the ID so that you can unregister the function, it is better to obtain it by passing the registered name to **xlfEvaluate**. If the function has not been registered, **xlfEvaluate** fails with a #NAME? error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e7f22-128">��</span><span class="sxs-lookup"><span data-stu-id="e7f22-128">Example</span></span>

<span data-ttu-id="e7f22-129">**** �� `\SAMPLES\GENERIC\GENERIC.C` �֐��̃R�[�h����Q�Ƃ��������B</span><span class="sxs-lookup"><span data-stu-id="e7f22-129">See the code for the **fExit** function in  `\SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a><span data-ttu-id="e7f22-130">�֘A����</span><span class="sxs-lookup"><span data-stu-id="e7f22-130">See also</span></span>

- [<span data-ttu-id="e7f22-131">xlfRegister (�\`�� 1)</span><span class="sxs-lookup"><span data-stu-id="e7f22-131">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="e7f22-132">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="e7f22-132">xlfRegisterId</span></span>](xlfregisterid.md)
- [<span data-ttu-id="e7f22-133">xlfUnregister (�\`�� 2)</span><span class="sxs-lookup"><span data-stu-id="e7f22-133">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
- [<span data-ttu-id="e7f22-134">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="e7f22-134">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

