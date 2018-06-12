---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- tempactivecell12 function [excel 2007],TempActiveCell function [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798941"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="ccf67-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="ccf67-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="ccf67-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ccf67-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ccf67-106">��ƒ��̃V�[�g�̃Z���ւ̊O���Q�Ƃ�܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐�</span><span class="sxs-lookup"><span data-stu-id="ccf67-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="ccf67-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="ccf67-107">Parameters</span></span>

 <span data-ttu-id="ccf67-108">_row_</span><span class="sxs-lookup"><span data-stu-id="ccf67-108">_row_</span></span>
  
<span data-ttu-id="ccf67-p101">�Q�Ƃ����s�B1 �s�ڂ� 0 �œn�����悤�ɍs�̈����� 0 ����n�܂�܂��BMicrosoft Office Excel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s����J�n���� Excel 2007 �ȍ~�ł́A�ő�l�́A65,535 = 2^16 - 1 �ł���AWORD �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 1,048,575 = 2^20 - 1 �ł��BRW �́AXLCALL.H�� 32 �r�b�g�����t�������Ƃ��Ē�\`����܂��B</span><span class="sxs-lookup"><span data-stu-id="ccf67-p101">The row to be referenced. Row arguments are zero-based so that row 1 is passed as 0. In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer. Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1. RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="ccf67-114">_col_</span><span class="sxs-lookup"><span data-stu-id="ccf67-114">_col_</span></span>
  
<span data-ttu-id="ccf67-p102">�Q�Ƃ�����B�� A �� 0 �œn�����悤�ɁA���̒l�� 0 ����n�܂�l�ɂȂ��Ă��܂��BExcel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s����J�n���� Excel 2007 �ȍ~�ł́A�ő�l�́A255 = 2^8 - 1 �ł���ABYTE �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 16,383 = 2^14 - 1 �ł��BCOL �́AXLCALL.H�� 32 �r�b�g�̕����t�������Ƃ��Ē�\`����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="ccf67-p102">The column to be referenced. This is zero-based so that column A is passed as 0. In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer. Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1. COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="ccf67-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ccf67-120">Return value</span></span>

<span data-ttu-id="ccf67-121">�n�����Z���� **xltypeRef** �O���Q�Ƃ��Ԃ�܂��B</span><span class="sxs-lookup"><span data-stu-id="ccf67-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ccf67-122">��</span><span class="sxs-lookup"><span data-stu-id="ccf67-122">Example</span></span>

<span data-ttu-id="ccf67-123">���̗�ł́A **TempActiveCell12** ��g�p���� B94 �̓�e���ƒ��̃V�[�g�ɕ\�����܂��B</span><span class="sxs-lookup"><span data-stu-id="ccf67-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ccf67-124">�֘A����</span><span class="sxs-lookup"><span data-stu-id="ccf67-124">See also</span></span>



<span data-ttu-id="ccf67-125">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="ccf67-125">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

