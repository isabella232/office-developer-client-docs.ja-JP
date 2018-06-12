---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- tempstr function [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798955"
---
# <a name="tempstr"></a><span data-ttu-id="3bbb0-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="3bbb0-104">TempStr</span></span>

 <span data-ttu-id="3bbb0-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3bbb0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3bbb0-p101">**xltypeStr** �o�C�g�������i�[���Ă���ꎞ�I�� **XLOPER** ��쐬����A�񐄏��̃t���[�����[�N ���C�u�����֐��ł��B���͂Ƃ��āANULL �ŏI������\�[�X�������󂯎��܂��B�󂯎����������̍ŏ��̕�����㑱�̕�����̒����ŏ㏑�����悤�Ƃ��܂��B���̓���͈��S�łȂ����Ƃ�����A�ǂݎ���p�̕������n���ƁAMicrosoft Excel ���N���b�V������\��������܂��B</span><span class="sxs-lookup"><span data-stu-id="3bbb0-p101">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string. It takes a null-terminated source string as input. It tries to overwrite the first character of the supplied string with the subsequent string's length. This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="3bbb0-110">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="3bbb0-110">Parameters</span></span>

 <span data-ttu-id="3bbb0-111">_str_</span><span class="sxs-lookup"><span data-stu-id="3bbb0-111">_str_</span></span>
  
<span data-ttu-id="3bbb0-p102">NULL �ŏI������\�[�X������ւ̃|�C���^�[�B **TempStr** �� 255 �o�C�g��������������؂�l�߂܂��B</span><span class="sxs-lookup"><span data-stu-id="3bbb0-p102">A pointer to the null-terminated source string. **TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="3bbb0-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3bbb0-114">Return value</span></span>

<span data-ttu-id="3bbb0-115">�n���ꂽ������o�b�t�@�[�ւ̃|�C���^�[��i�[���Ă��� **xltypeStr** �������Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="3bbb0-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3bbb0-116">����</span><span class="sxs-lookup"><span data-stu-id="3bbb0-116">Remarks</span></span>

<span data-ttu-id="3bbb0-p103">���̕��@�ɂ��ꎞ�I�ȕ�����̍쐬�́A[TempStrConst �� TempStr12](tempstrconst-tempstr12.md) �̗����œ��삷����@�Ƃ��Ă͐�������Ȃ��Ȃ�܂����B�����̊֐��́A�V���������� �o�b�t�@�[����蓖�ĂāA���̃o�b�t�@�[�ɓn���ꂽ�������R�s�[���܂��B **TempStrConst** �� **TempStr12** �̓��͕�����͕ύX����Ȃ����߁A **const** �Ƃ��Đ錾����܂��B����ɑ΂��āA **TempStr** �ւ̓��͕�����͕ύX����邽�߁A **const** �Ƃ��Đ錾�ł��܂���B���͕�����̍ŏ��̕����́A���������̃X�y�[�X�Ƃ��Ĉ����A���̊֐��ɂ���ď㏑������܂��B</span><span class="sxs-lookup"><span data-stu-id="3bbb0-p103">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work. These functions allocate a new memory buffer and copy the passed-in string into it. The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**. In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**. The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3bbb0-122">�֘A����</span><span class="sxs-lookup"><span data-stu-id="3bbb0-122">See also</span></span>



<span data-ttu-id="3bbb0-123">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="3bbb0-123">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

