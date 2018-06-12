---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- xlautoclose function [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798977"
---
# <a name="xlautoclose"></a><span data-ttu-id="3060c-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="3060c-104">xlAutoClose</span></span>

 <span data-ttu-id="3060c-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3060c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3060c-p101">XLL �t�@�C������A�N�e�B�u�ɂȂ邽�тɁAMicrosoft Excel �ɌĂяo����܂��BExcel �Z�b�V����������ɏI������ƁA�A�h�C���͔�A�N�e�B�u�ɂȂ�܂��B�A�h�C���́AExcel �Z�b�V�������Ƀ��[�U�[�ɂ���Ĕ�A�N�e�B�u�������ꍇ������܂��B���̊֐��͂��̏ꍇ�ɌĂяo����܂��B</span><span class="sxs-lookup"><span data-stu-id="3060c-p101">Called by Microsoft Excel whenever the XLL is deactivated. The add-in is deactivated when an Excel session ends normally. The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="3060c-p102">�֐��ƃR�}���h�̓o�^����A���\�[�X�̉���A�J�X�^�}�C�Y����ɖ߂����ƂȂǂ� XLL �����s�ł���悤���邽�߂ɓK�؂Ȃ��Ƃł͂���܂����AExcel �͂��̊֐���������G�N�X�|�[�g����̂ɁAXLL ��K�v�Ƃ��܂���B�֐��ƃR�}���h�� XLL �������I�ɓo�^������Ȃ��ꍇ�A **xlAutoClose** �֐���Ăяo������AExcel �͂������s���܂��B</span><span class="sxs-lookup"><span data-stu-id="3060c-p102">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on. If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="3060c-111">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="3060c-111">Parameters</span></span>

<span data-ttu-id="3060c-112">���̊֐��Ɉ����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="3060c-112">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3060c-113">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="3060c-113">Property value/Return value</span></span>

<span data-ttu-id="3060c-114">この関数の実装では、1 (**int**) を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3060c-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3060c-115">����</span><span class="sxs-lookup"><span data-stu-id="3060c-115">Remarks</span></span>

<span data-ttu-id="3060c-p103">XLL ����A�N�e�B�u�ɂȂ�A�܂胁��������A�����[�h����邽�тɁAExcel �� **xlAutoClose** �֐���Ăяo���܂��B�ȉ��̏󋵂ŁAXLL �͔�A�N�e�B�u�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="3060c-p103">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory. The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="3060c-118">�Z�b�V�������ɃA�N�e�B�u�ȏꍇ�ɁAExcel �Z�b�V����������ɏI���������_�B</span><span class="sxs-lookup"><span data-stu-id="3060c-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="3060c-119">Excel �Z�b�V�������ɖ����I�ɃA�����[�h���ꂽ�ꍇ�B</span><span class="sxs-lookup"><span data-stu-id="3060c-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="3060c-120">XLL �͈ȉ��̂������̕��@�ŃA�����[�h�����\��������܂��B</span><span class="sxs-lookup"><span data-stu-id="3060c-120">An XLL can be unloaded in several ways:</span></span>
    
- <span data-ttu-id="3060c-121">�A�h�C�� �}�l�[�W���[��g�p����B</span><span class="sxs-lookup"><span data-stu-id="3060c-121">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="3060c-122">���� DLL �̖��O��B��̈����Ƃ��� [xlfUnregister](xlfunregister-form-1.md) ��Ăяo���ʂ� XLL ����B</span><span class="sxs-lookup"><span data-stu-id="3060c-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="3060c-123">���� DLL �̖��O��B��̈����Ƃ��� [UNREGISTER](xlfunregister-form-1.md) ��Ăяo�� XLM �}�N�� �V�[�g����B</span><span class="sxs-lookup"><span data-stu-id="3060c-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="3060c-124">���̊֐��́A�ȉ�����s���܂��B</span><span class="sxs-lookup"><span data-stu-id="3060c-124">This function should do the following:</span></span>
  
- <span data-ttu-id="3060c-125">XLL ���ǉ������C�ӂ̃��j���[�܂��̓��j���[���ڂ�폜����B</span><span class="sxs-lookup"><span data-stu-id="3060c-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="3060c-126">�C�ӂ̕K�v�ȃO���[�o�� �N���[���A�b�v����s����B</span><span class="sxs-lookup"><span data-stu-id="3060c-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="3060c-p104">�쐬���ꂽ�C�ӂ̖��O�A���ɃG�N�X�|�[�g���ꂽ�֐��̖��O��폜����B **REGISTER** �ւ� 4 �Ԗڂ̈��������݂���ꍇ�A�֐��̓o�^���������̖��O��쐬���錴���ɂȂ�ꍇ�����邱�Ƃɂ����ӂ��������B</span><span class="sxs-lookup"><span data-stu-id="3060c-p104">Delete any names that were created, especially names of exported functions. Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="3060c-129">��</span><span class="sxs-lookup"><span data-stu-id="3060c-129">Example</span></span>

<span data-ttu-id="3060c-p105">���̊֐��̎���������  `SAMPLES\EXAMPLE\EXAMPLE.C` �t�@�C����  `SAMPLES\GENERIC\GENERIC.C` �t�@�C����Q�Ƃ��Ă��������B���̃R�[�h�́A  `SAMPLES\GENERIC\GENERIC.C` �ɂ���܂��B</span><span class="sxs-lookup"><span data-stu-id="3060c-p105">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function. The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="3060c-132">�֘A����</span><span class="sxs-lookup"><span data-stu-id="3060c-132">See also</span></span>



[<span data-ttu-id="3060c-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="3060c-133">xlAutoOpen</span></span>](xlautoopen.md)


<span data-ttu-id="3060c-134">[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)</span><span class="sxs-lookup"><span data-stu-id="3060c-134">[Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)</span></span>

