---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- tempactiveref function [excel 2007],TempActiveRef12 function [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798944"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="67a78-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="67a78-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="67a78-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67a78-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="67a78-106">��ƒ��̃��[�N�V�[�g��ɂ��钷���\`�̃u���b�N�̃Z���ւ̊O���Q�Ƃ�܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B</span><span class="sxs-lookup"><span data-stu-id="67a78-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="67a78-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="67a78-107">Parameters</span></span>

 <span data-ttu-id="67a78-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="67a78-108">_rwFirst_</span></span>
  
<span data-ttu-id="67a78-109">�Q�Ƃ̊J�n�s�B</span><span class="sxs-lookup"><span data-stu-id="67a78-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="67a78-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="67a78-110">_rwLast_</span></span>
  
<span data-ttu-id="67a78-111">�Q�Ƃ̏I���s�B</span><span class="sxs-lookup"><span data-stu-id="67a78-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="67a78-p101">�s�̈����� 0 ����n�܂�A1 �s�ڂ� 0 �Ƃ��ēn����܂��BMicrosoft Office Excel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�́A65,535 = 2^16 - 1 �ł���A���ꂪ WORD �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 1,048,575 = 2^20 - 1 �ł��BRW �́AXLCALL.H�� 32 �r�b�g�����t�������Ƃ��Ē�\`����܂��B</span><span class="sxs-lookup"><span data-stu-id="67a78-p101">Row arguments are zero-based so that row 1 is passed as 0. In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer. Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1. RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="67a78-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="67a78-116">_colFirst_</span></span>
  
<span data-ttu-id="67a78-117">�Q�Ƃ̊J�n��ԍ��B</span><span class="sxs-lookup"><span data-stu-id="67a78-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="67a78-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="67a78-118">_colLast_</span></span>
  
<span data-ttu-id="67a78-119">�Q�Ƃ̏I����ԍ��B</span><span class="sxs-lookup"><span data-stu-id="67a78-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="67a78-p102">��̈����� 0 ����n�܂�A�� A �� 0 �Ƃ��ēn����܂��BExcel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�́A255 = 2^8 - 1 �ł���A���ꂪ BYTE �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 16,383 = 2^14 - 1 �ł��BCOL �́AXLCALL.H�� 32 �r�b�g�����t�������Ƃ��Ē�\`����܂��B</span><span class="sxs-lookup"><span data-stu-id="67a78-p102">Column arguments are zero-based so that column A is passed as 0. In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer. Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1. COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="67a78-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="67a78-124">Return value</span></span>

<span data-ttu-id="67a78-125">�n����钷���\`�̃u���b�N�̃Z���ւ� **xltypeRef** �O���Q�Ƃ�Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="67a78-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="67a78-126">��</span><span class="sxs-lookup"><span data-stu-id="67a78-126">Example</span></span>

<span data-ttu-id="67a78-127">���̗�ł́A **TempActiveRef12** �֐���g�p���� A105:C110 �̃Z����I����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="67a78-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="67a78-128">�֘A����</span><span class="sxs-lookup"><span data-stu-id="67a78-128">See also</span></span>



<span data-ttu-id="67a78-129">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="67a78-129">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

