---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- xlstack function [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798990"
---
# <a name="xlstack"></a><span data-ttu-id="48ba3-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="48ba3-104">xlStack</span></span>

<span data-ttu-id="48ba3-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="48ba3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="48ba3-106">�X�^�b�N��̋󂫗̈��m�F���܂��B</span><span class="sxs-lookup"><span data-stu-id="48ba3-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="48ba3-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="48ba3-107">Parameters</span></span>

<span data-ttu-id="48ba3-108">���̊֐��Ɉ����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="48ba3-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="48ba3-109">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="48ba3-109">Property value/Return value</span></span>

<span data-ttu-id="48ba3-110">スタックに残っているバイト数 (**xltypeInt**) の数を返します。</span><span class="sxs-lookup"><span data-stu-id="48ba3-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48ba3-111">����</span><span class="sxs-lookup"><span data-stu-id="48ba3-111">Remarks</span></span>

<span data-ttu-id="48ba3-p101">�ŋ߂̃o�[�W�����̎g�p�\�ȃX�^�b�N�̈�̗e�ʂ́A **XLOPER** �� 16 �r�b�g�̕����t�������Ɏ��܂�܂���B�܂�A **xlStack** �� **XLOPER** ����� **Excel4** �܂��� **Excel4v** ��g�p���ČĂяo�����Ƃ��� -32767 ���� 32768 �̊Ԃ̒l��Ԃ����Ƃ��ł���A�Ƃ������Ƃł��B���̏ꍇ�ɐ������l��擾����ɂ́A�߂�l�� unsigned short �^�ɃL���X�g���܂��B</span><span class="sxs-lookup"><span data-stu-id="48ba3-p101">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**. This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER**s and **Excel4** or **Excel4v**. To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="48ba3-115">Excel 2007 �ȍ~�ł́A **XLOPER12** ����� **Excel12** �܂��� **Excel12v** ��g�p���āA���̊֐���Ăяo���K�v������܂��B���̏ꍇ�A�߂�l�͎g�p�\�ȃX�^�b�N�̈�̗e�ʂ��A64 KB �̂����ꂩ���������ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="48ba3-115">Starting in Excel 2007, you should call this function using **XLOPER12**s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="48ba3-p102">Excel �ł́A�X�^�b�N��̋󂫗̈�ɐ���������܂��B���̗e�ʂ𒴂��Ȃ��悤�ɒ��ӂ���K�v������܂��B���ɑ傫�ȃf�[�^�\����z�u������A�\�Ȍ��葽���̃��[�J���ϐ���ÓI�ɂ��Ă͂����܂���B�֐���ċA�I�ɌĂяo���Ȃ��悤�ɂ��Ă��������B�����s���ƁA�X�^�b�N�������ɂ����ς��ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="48ba3-p102">Excel has a limited amount of space on the stack, and you should take care not to overrun this space. Never put very large data structures on the stack, and make as many local variables as possible static. Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="48ba3-119">�X�^�b�N��I�[�o�[�������Ă���^��������ꍇ�́A���̊֐���p�ɂɌĂяo���āA�X�^�b�N�̈悪�ǂ̒��x�c���Ă��邩�m�F���܂��B</span><span class="sxs-lookup"><span data-stu-id="48ba3-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="48ba3-120">��</span><span class="sxs-lookup"><span data-stu-id="48ba3-120">Example</span></span>

<span data-ttu-id="48ba3-p103">�ŏ��̗�ł́A�X�^�b�N�̋󂫗̈�̗e�ʂ������ꂽ�x�����b�Z�[�W���\������܂��B�����  `\SAMPLES\EXAMPLE\EXAMPLE.C` �Ɋi�[����Ă��܂��B2 �Ԗڂ̗�����������܂� ( **XLOPER** ��g�p)�B����� SDK �̃R�[�h��ɂ͊܂܂�Ă��܂���B</span><span class="sxs-lookup"><span data-stu-id="48ba3-p103">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`. The second example does the same thing, working with **XLOPER**s and is not contained in the SDK example code.</span></span>
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="48ba3-123">�֘A����</span><span class="sxs-lookup"><span data-stu-id="48ba3-123">See also</span></span>

- [<span data-ttu-id="48ba3-124">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="48ba3-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

