---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- tempactivecolumn12 function [excel 2007],TempActiveColumn function [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798947"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="3984e-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="3984e-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="3984e-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3984e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3984e-106">��ƒ��̃V�[�g�̗�S�̂̊O���Q�Ƃ�܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B</span><span class="sxs-lookup"><span data-stu-id="3984e-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="3984e-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="3984e-107">Parameters</span></span>

 <span data-ttu-id="3984e-108">_col_(**バイト**)</span><span class="sxs-lookup"><span data-stu-id="3984e-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="3984e-p101">�Q�Ƃ�����B�� A �� 0 �œn�����悤�ɁA���̒l�� 0 ����n�܂�l�ɂȂ��Ă��܂��BMicrosoft Office Excel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s����J�n���� Excel 2007 �ȍ~�ł́A�ő�l�� 255 = 2^8 - 1 �ł���ABYTE �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 16,383 = 2^14 - 1 �ł��BCOL �́AXLCALL.H�� 32 �r�b�g�����t�������Ƃ��Ē�\`����܂��B</span><span class="sxs-lookup"><span data-stu-id="3984e-p101">The column to be referenced. This is zero-based so that column A is passed as 0. In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer. Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1. COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3984e-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3984e-114">Return value</span></span>

<span data-ttu-id="3984e-115">�n������� **xltypeRef** �O���Q�Ƃ�Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="3984e-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3984e-116">��</span><span class="sxs-lookup"><span data-stu-id="3984e-116">Example</span></span>

<span data-ttu-id="3984e-117">���̗�ł́A **TempActiveColumn12** ��g�p���āA�� B �S�̂�I����܂��B</span><span class="sxs-lookup"><span data-stu-id="3984e-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="3984e-118">�֘A����</span><span class="sxs-lookup"><span data-stu-id="3984e-118">See also</span></span>



<span data-ttu-id="3984e-119">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="3984e-119">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

