---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- tempactiverow function [excel 2007],TempActiveRow12 function [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798942"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="798a6-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="798a6-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="798a6-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="798a6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="798a6-106">��ƒ��̃V�[�g�̍s�S�̂̊O���Q�Ƃ�܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐�</span><span class="sxs-lookup"><span data-stu-id="798a6-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="798a6-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="798a6-107">Parameters</span></span>

 <span data-ttu-id="798a6-108">_row_</span><span class="sxs-lookup"><span data-stu-id="798a6-108">_row_</span></span>
  
<span data-ttu-id="798a6-p101">�Q�Ƃ����s�B1 �s�ڂ� 0 �œn�����悤�ɍs�̈����� 0 ����n�܂�܂��BMicrosoft Office Excel 2003 �ȑO�̃o�[�W�����ƁA�݊����[�h�Ńu�b�N����s����J�n���� Excel 2007 �ȍ~�ł́A�ő�l�́A65,535 = 2^16 - 1 �ł���AWORD �̐����l�Ŏw��ł���ő�l�ɂȂ�܂��B�u�b�N����s���� Excel 2007 �ȍ~�ł́A�ő�l�� 1,048,575 = 2^20 - 1 �ł��BRW �́AXLCALL.H�� 32 �r�b�g�����t�������Ƃ��Ē�\`����܂��B</span><span class="sxs-lookup"><span data-stu-id="798a6-p101">The row to be referenced. Row arguments are zero-based so that row 1 is passed as 0. In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer. Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1. RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="798a6-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="798a6-114">Return value</span></span>

<span data-ttu-id="798a6-115">�n�����s�̃Z���� **xltypeRef** �O���Q�Ƃ��Ԃ�܂��B</span><span class="sxs-lookup"><span data-stu-id="798a6-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="798a6-116">��</span><span class="sxs-lookup"><span data-stu-id="798a6-116">Example</span></span>

<span data-ttu-id="798a6-117">���̗�ł́A **TempActiveRow12** �֐���g�p���čs 113 ��I����܂��B</span><span class="sxs-lookup"><span data-stu-id="798a6-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="798a6-118">�֘A����</span><span class="sxs-lookup"><span data-stu-id="798a6-118">See also</span></span>



<span data-ttu-id="798a6-119">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="798a6-119">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

