---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- xlgetinst function [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798982"
---
# <a name="xlgetinst"></a><span data-ttu-id="d2a0a-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="d2a0a-104">xlGetInst</span></span>

 <span data-ttu-id="d2a0a-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d2a0a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d2a0a-106">���� DLL ��Ăяo���Ă��� Microsoft Excel �C���X�^���X�̃C���X�^���X �n���h����Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="d2a0a-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="d2a0a-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="d2a0a-107">Parameters</span></span>

<span data-ttu-id="d2a0a-108">���̊֐��ɂ͈����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="d2a0a-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d2a0a-109">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="d2a0a-109">Property value/Return value</span></span>

<span data-ttu-id="d2a0a-110">インスタンス ハンドル (**xltypeInt**) は、 **val.w**フィールドになります。</span><span class="sxs-lookup"><span data-stu-id="d2a0a-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d2a0a-111">����</span><span class="sxs-lookup"><span data-stu-id="d2a0a-111">Remarks</span></span>

<span data-ttu-id="d2a0a-112">���̊֐���g�p����ƁADLL ��Ăяo���Ă��� Excel �� �����̎��s���C���X�^���X�����ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="d2a0a-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="d2a0a-p101">[Excel4](excel4-excel12.md) �܂��� [Excel4v](excel4v-excel12v.md) ��g�p���Ă��̊֐���Ăяo���ƁA�Ԃ���� XLOPER �����ϐ��́A16 �r�b�g�����t�� short int �ɂȂ�܂��B���̏ꍇ�ɓ���邱�Ƃ��ł���̂́A32 �r�b�g Windows �n���h���̉��� 16 �r�b�g�݂̂ł��BExcel 2007 �ȍ~�A **XLOPER12** �̐����ϐ��� 32 �r�b�g�����t�� int �ɂȂ������߁A�n���h���S�̂�܂߂邱�Ƃ��ł��A���ׂĂ̊J���Ă���E�B���h�E�𔽕���������K�v���Ȃ�Ȃ�܂����B</span><span class="sxs-lookup"><span data-stu-id="d2a0a-p101">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle. Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d2a0a-p102">**xlGetInst** �֐��� 64 �r�b�g�ł� Microsoft Excel �Ŏg�p����ƁA���s���܂��B����́A **xltypeInt** �l�̌^�̑傫�����AExcel �ɂ���ĕԂ���� 64 �r�b�g���̃n���h����ێ��ł��Ȃ����߂ł��B���̂��߁AExcel 2010 �ł� [xlGetInstPtr](xlgetinstptr.md) �Ƃ������O�̐V�����֐�����������܂����B���̊֐��́A32 �r�b�g�� 64 �r�b�g�̂ǂ���̃o�[�W������ Excel �ł����ɓ��삵�܂��B</span><span class="sxs-lookup"><span data-stu-id="d2a0a-p102">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail. This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case. For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d2a0a-118">��</span><span class="sxs-lookup"><span data-stu-id="d2a0a-118">Example</span></span>

<span data-ttu-id="d2a0a-p103">���̎g�p��ł́A�Ō�ɌĂяo���� Excel �R�s�[ �C���X�^���X��A���݌Ăяo���Ă��� Excel �R�s�[�Ɣ�r���܂��B�����ꍇ�ɂ� 1 ��Ԃ��A�قȂ�ꍇ�ɂ� 0 ��Ԃ��܂��B�֐������s����ƁA-1 ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="d2a0a-p103">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it. If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="d2a0a-121">�֘A����</span><span class="sxs-lookup"><span data-stu-id="d2a0a-121">See also</span></span>



[<span data-ttu-id="d2a0a-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="d2a0a-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="d2a0a-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="d2a0a-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="d2a0a-124">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="d2a0a-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

