---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlgethwnd function [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798995"
---
# <a name="xlgethwnd"></a><span data-ttu-id="94d14-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="94d14-104">xlGetHwnd</span></span>

<span data-ttu-id="94d14-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="94d14-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="94d14-106">Microsoft Excel �E�B���h�E�̍ŏ�ʂ̃E�B���h�E �n���h����Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="94d14-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="94d14-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="94d14-107">Parameters</span></span>

<span data-ttu-id="94d14-108">���̊֐��ɂ͈����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="94d14-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="94d14-109">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="94d14-109">Property value/Return value</span></span>

<span data-ttu-id="94d14-110">[ **Val.w** ] フィールドには、ウィンドウ ハンドル (**xltypeInt**) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="94d14-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="94d14-111">����</span><span class="sxs-lookup"><span data-stu-id="94d14-111">Remarks</span></span>

<span data-ttu-id="94d14-112">���̊֐��́AWindows API �̃R�[�h��L�q���邽�߂ɖ𗧂��܂��B</span><span class="sxs-lookup"><span data-stu-id="94d14-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="94d14-p101">[Excel4](excel4-excel12.md) �܂��� [Excel4v](excel4v-excel12v.md) ��g�p���āA���̊֐���Ăяo���ƁA�Ԃ���� XLOPER �����ϐ��́A16 �r�b�g�����t�� short int �ɂȂ�܂��B���̏ꍇ�ɓ���邱�Ƃ��ł���̂́A32 �r�b�g Windows �n���h���̉��� 16 �r�b�g�݂̂ł��B��ʕ������������ɂ́A���ׂĂ̊J�����E�B���h�E��ʂ��ăR�[�h��J��Ԃ��K�p���āA���ʕ����Ƃ̈�v���������K�v������܂��BExcel 2007 �ȍ~�A **XLOPER12** �̐����ϐ��� 32 �r�b�g int �ɂȂ������߁A�n���h���S�̂�܂߂邱�Ƃ��ł��A���ׂĂ̊J���Ă���E�B���h�E�𔽕���������K�v���Ȃ�Ȃ�܂����B</span><span class="sxs-lookup"><span data-stu-id="94d14-p101">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle. To find the high part, your code must iterate through all open windows looking for a match with the low part. Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="94d14-116">��</span><span class="sxs-lookup"><span data-stu-id="94d14-116">Example</span></span>

<span data-ttu-id="94d14-117">[](fshowdialog.md) �� `SAMPLES\GENERIC\GENERIC.C` �ɂ��ẮA�R�[�h��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="94d14-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94d14-118">�֘A����</span><span class="sxs-lookup"><span data-stu-id="94d14-118">See also</span></span>

- [<span data-ttu-id="94d14-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="94d14-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="94d14-120">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="94d14-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

