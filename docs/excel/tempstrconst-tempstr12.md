---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- tempstr12 function [excel 2007],TempStrConst function [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798958"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="82545-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="82545-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="82545-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="82545-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="82545-p101">**xltypeStr** �������܂ވꎞ�I�� **XLOPER/XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B���͂Ƃ��� Null �ŏI������\�[�X�̕������󂯎��܂��B���̊֐��́A�V���������� �o�b�t�@�[����蓖�ĂāA���̃o�b�t�@�[�ɓn���ꂽ�������R�s�[���܂��B���͕�����͕ύX����Ȃ����߁A **const** �Ƃ��Đ錾����܂��B</span><span class="sxs-lookup"><span data-stu-id="82545-p101">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input. The function allocates a new memory buffer and copies the passed-in string into it. The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="82545-109">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="82545-109">Parameters</span></span>

 <span data-ttu-id="82545-110">_str_</span><span class="sxs-lookup"><span data-stu-id="82545-110">_str_</span></span>
  
<span data-ttu-id="82545-p102">Null �ŏI������\�[�X�̕�����ւ̃|�C���^�[�B **XLOPER** �̏ꍇ�ATempStrConst �� 255 �o�C�g��蒷���������؂�̂Ă܂��B **XLOPER12** �̏ꍇ�ATempStr12Const �� 32,767 Unicode ������蒷���������؂�̂Ă܂��B</span><span class="sxs-lookup"><span data-stu-id="82545-p102">A pointer to the null-terminated source string. In the case of **XLOPER**s, TempStrConst truncates strings that are longer than 255 bytes. In the case of **XLOPER12**s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="82545-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="82545-114">Return value</span></span>

<span data-ttu-id="82545-115">�n���ꂽ������o�b�t�@�[�̃R�s�[��i�[���Ă��� **xltypeStr** �������Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="82545-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="82545-116">����</span><span class="sxs-lookup"><span data-stu-id="82545-116">Remarks</span></span>

<span data-ttu-id="82545-p103">**XLOPER** ������̃t���[�����[�N�֐� **TempStr** �̓���͈قȂ�܂��B�w�肳�ꂽ������̍ŏ��̕�����㑱�̕�����̒����ŏ㏑�����悤�Ƃ��邽�߁A���ӂ��K�v�ł��B����͏�Ɉ��S�Ƃ����킯�ł͂���܂���B�ǂݎ���p�̕������n���ƁAMicrosoft Excel ���N���b�V������\��������܂��B���̕��@�ɂ��ꎞ�I�ȕ�����̍쐬�́A **TempStrConst** �� **TempStr12** �̗����œ��삷����@�Ƃ��Ă͐�������Ȃ��Ȃ�܂����B���������āA���͕�����̍ŏ��̕����́A������̐擪�Ƃ��� (�܂�A������\�������܂��͒�����\�������p�̃X�y�[�X�Ƃ��Ăł͂Ȃ�) ��������܂��B�e�����\���ł��Ȃ����߁A�J�n���ɃG���R�[�h���ꂽ������\�������̂��镶����͓n���Ȃ��ł��������B</span><span class="sxs-lookup"><span data-stu-id="82545-p103">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length. This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string. This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work. Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character. You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="82545-122">��</span><span class="sxs-lookup"><span data-stu-id="82545-122">Example</span></span>

<span data-ttu-id="82545-123">���̗�ł́A **TempStr12** �֐���g�p���ă��b�Z�[�W �{�b�N�X�̕������쐬���܂��B</span><span class="sxs-lookup"><span data-stu-id="82545-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="82545-124">�֘A����</span><span class="sxs-lookup"><span data-stu-id="82545-124">See also</span></span>



<span data-ttu-id="82545-125">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="82545-125">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

