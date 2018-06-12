---
title: ���[�N�V�[�g�̎Q��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- references [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: b7089fb891c96be9182189e3a5f30057721cebbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798966"
---
# <a name="worksheet-references"></a><span data-ttu-id="57975-104">���[�N�V�[�g�̎Q��</span><span class="sxs-lookup"><span data-stu-id="57975-104">Worksheet References</span></span>

 <span data-ttu-id="57975-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="57975-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="57975-106">Microsoft Excel での参照は、セルの (1 つのセルを指定できます)、または、場合によってはいくつかの非結合セルのブロックの長方形のブロックを参照するデータ型です。</span><span class="sxs-lookup"><span data-stu-id="57975-106">A reference in Microsoft Excel is a data type that refers to a rectangular block of cells (which can be just one cell), or in some cases, a number of disjoint blocks of cells.</span></span> <span data-ttu-id="57975-107">内部的には、内部参照と呼ばれる、現在のシート上のセルの 1 つの参照型が使用されます。</span><span class="sxs-lookup"><span data-stu-id="57975-107">Internally, Excel uses one reference type for cells on the current sheet, known as an internal reference.</span></span> <span data-ttu-id="57975-108">現在のシートに含まれていない任意のセルは、外部参照と呼ばれる参照の別の型で表されます。</span><span class="sxs-lookup"><span data-stu-id="57975-108">Any cell that is not on the current sheet is described by another type of reference known as an external reference.</span></span> <span data-ttu-id="57975-109">現在の定義の次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="57975-109">See the next section for the definition of active and current.</span></span>
  
## <a name="active-vs-current"></a><span data-ttu-id="57975-110">��ƒ��ƌ���</span><span class="sxs-lookup"><span data-stu-id="57975-110">Active vs. Current</span></span>

<span data-ttu-id="57975-p102">Excel ��ŁA��ƒ��Ƃ����p��́A���[�U�[���\�����̂�̂�\���܂��B��ƒ��̃u�b�N��V�[�g�́A���[�U�[�����݉{�����̃u�b�N�⃏�[�N�V�[�g�A�܂��� Excel ����ʃA�v���P�[�V�����Ƀt�H�[�J�X���ڂ����ꍇ�ɂ́AExcel �ōŌ�Ƀt�H�[�J�X���Ă����ۂɕ\�����Ă����u�b�N�⃏�[�N�V�[�g��w���܂��B��ƒ��̃V�[�g�́A�K����ƒ��̃u�b�N��ɂ���܂��B��ƒ��̃V�[�g��ŕ����̃Z�����I�����Ă���ꍇ�́A�A�N�e�B�u �Z���Ƃ��ĔF������܂��B���ߍ��݃I�u�W�F�N�g�Ƀt�H�[�J�X����Ă���ꍇ�́A�Ō�ɑI������Z�������������A�N�e�B�u�ƂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="57975-p102">In Excel, the term active refers to what the user is viewing. The active workbook and worksheet are those that the user is currently looking at, or, if Excel has lost focus to another application, was looking at when Excel last had focus. The active sheet is always in the active workbook. The one or more cells that are selected in the active sheet are known as the active cells. If an embedded object has focus, the last-selected cells are still active.</span></span> 
  
<span data-ttu-id="57975-p103">�����Ƃ�����́AExcel ���Čv�Z���Ă����̂�\���܂��B���݂̃u�b�N�ƃ��[�N�V�[�g�́A���ݍČv�Z��s���Ă���u�b�N�⃏�[�N�V�[�g��w���܂��B���݂̃V�[�g�́A�K�����݂̃u�b�N��ɂ���܂��B�Čv�Z����Ă���Z���͌��݂̃Z���ƌĂ΂�܂��B�܂��A�z�񐔎����Čv�Z����Ă���ꍇ��A���݂̃Z���ƌĂ΂�܂��B</span><span class="sxs-lookup"><span data-stu-id="57975-p103">The term current refers to what Excel is recalculating. The current workbook and worksheet are those that are currently being recalculated. The current sheet is always in the current workbook. The cell being recalculated is known as the current cell, or, in the case of an array formula being recalculated, the current cells.</span></span> 
  
<span data-ttu-id="57975-120">�o���Ă����ׂ��d�v�ȃ|�C���g�͎��̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="57975-120">The important points to remember are as follows:</span></span>
  
- <span data-ttu-id="57975-121">��ƒ��̃u�b�N��V�[�g�A�Z�����A�K��������݂̃u�b�N��V�[�g�A�Z���ɂȂ�킯�ł͂���܂��� (���݂̂�̂ł���ꍇ�����܂�)�B</span><span class="sxs-lookup"><span data-stu-id="57975-121">The active workbook/worksheet/cell is not generally the current one, although it can be.</span></span>
    
- <span data-ttu-id="57975-122">Visual Basic for Applications (VBA) ���W���[���� �ADLL �܂��� XLL �ɂ����āA�A�h�C���֐��́A���݂̃V�[�g��ɂ��錻�݂̃Z������Ăяo����܂��B�}���\` �X���b�h�Čv�Z (MTR) �̏ꍇ�́A�����̂����ꂩ����Ăяo����܂��B</span><span class="sxs-lookup"><span data-stu-id="57975-122">An add-in function, whether in a Visual Basic for Applications (VBA) module or a DLL or XLL, is always called from the current cell on the current sheet, or one of them in the case of multithreaded recalculation (MTR).</span></span>
    
<span data-ttu-id="57975-p104">�u�b�N��̃Z���A�Z���͈́A�V�[�g�ɂ��Ă̏���񋟂��鑽���� Excel �̊֐��́A��ƒ��̃u�b�N�A�V�[�g�A�Z���ƁA���݂̃u�b�N�A�V�[�g�A�Z���Ƃ��ʂ��܂��B�����̑���_�́A���̃Z�N�V�����ɋL�ڂ���Ă���Ƃ���A�Z�� �u���b�N�̎Q�Ƃ�\�����߂Ɏg�p����f�[�^�^�ɂ���f����܂��B</span><span class="sxs-lookup"><span data-stu-id="57975-p104">Many Excel functions that provide information about a cell, a range of cells, or a sheet in a workbook distinguish between the active workbook, sheet, or cell and the current workbook, sheet, or cell. This difference is reflected in the data types used to describe references to blocks of cells, as described in the following section.</span></span>
  
## <a name="internal-and-external-worksheet-references"></a><span data-ttu-id="57975-125">������[�N�V�[�g����ъO�����[�N�V�[�g�̎Q��</span><span class="sxs-lookup"><span data-stu-id="57975-125">Internal and External Worksheet References</span></span>

<span data-ttu-id="57975-p105">����Q�ƂƊO���Q�Ƃ̎�ȈႢ�́A�O���Q�Ƃ̃f�[�^�^�ɂ́A���[�N�V�[�g ID �ɉ����āA�Q�Ɛ�Z���̋L�q���܂܂�Ă��邱�Ƃł��B����Q�Ƃɂ̓V�[�g�ւ̎Q�Ƃ��܂܂�Ă��܂���B�V�[�g�����݂̃V�[�g�ł��邱�Ƃ�ÖٓI�Ɏ����܂��B</span><span class="sxs-lookup"><span data-stu-id="57975-p105">The key difference between internal and external references is that the external reference data type contains an ID for the worksheet and also a description of which cells are referred to. An internal reference contains no reference to the sheet—it is implicit that the sheet is the current sheet.</span></span> 
  
<span data-ttu-id="57975-128">C API 関数の多くは、参照を返すか、参照の引数を受け取る。</span><span class="sxs-lookup"><span data-stu-id="57975-128">Many C API functions return references or take reference arguments.</span></span> <span data-ttu-id="57975-129">引数を参照するすべての C API 関数は、 **xlSheetNm**関数は、外部参照を必要とする場合を除き、内部または外部のいずれかの参照を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="57975-129">Any C API function that takes reference arguments accepts either internal or external references, except the **xlSheetNm** function, which requires an external reference.</span></span> <span data-ttu-id="57975-130">いくつかの関数は、内部または外部のいずれかの参照のみを返します。</span><span class="sxs-lookup"><span data-stu-id="57975-130">Some functions only return either internal or external references.</span></span> <span data-ttu-id="57975-131">たとえば、C API 関数[xlfCaller](xlfcaller.md)は、定義では、現在のシートに、呼び出し元のセルへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="57975-131">For example, the C API function [xlfCaller](xlfcaller.md) returns a reference to the calling cells, by definition, on the current sheet.</span></span> <span data-ttu-id="57975-132">返される参照は常に内部の参照、関数は非参照型を返すことができます、関数がワークシートのセルから呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="57975-132">The returned reference is always an internal reference, although the function can return non-reference types where the function is not called from a worksheet cell.</span></span> <span data-ttu-id="57975-133">C API 関数[xlSheetId](xlsheetid.md)は、常に外部参照のデータ型に含まれるワークシートの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="57975-133">The C API function [xlSheetId](xlsheetid.md) always returns the ID of a worksheet contained within an external reference data type.</span></span> 
  
<span data-ttu-id="57975-p107">����Q�ƌ^�ƊO���Q�ƌ^�̊Ԃ̂����̎�ȈႢ�́A�O���Q�Ƃ̃f�[�^�^�́A�����V�[�g��̕����̗��U�����Z�� �u���b�N��\�����Ƃ��\�ł���_�ł��B����Q�Ƃł́A���݂̃V�[�g�� 1 �u���b�N�݂̂�\�����Ƃ��ł��܂��B���U�����Q�Ƃ́A�͈͂̈�������C�ӂ̊֐��ɓn�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="57975-p107">The other key difference between the internal and external reference types is that the external reference data type can describe multiple disjoint blocks of cells on the same sheet. Internal references can describe only a single block on the current sheet. Disjoint references can be passed to any function that takes a range argument.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57975-137">�֘A����</span><span class="sxs-lookup"><span data-stu-id="57975-137">See also</span></span>



[<span data-ttu-id="57975-138">Excel �v���O���~���O�̊T�O</span><span class="sxs-lookup"><span data-stu-id="57975-138">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
<span data-ttu-id="57975-139">[���O�Ƒ��̃��[�N�V�[�g�̎���]������](evaluating-names-and-other-worksheet-formula-expressions.md)</span><span class="sxs-lookup"><span data-stu-id="57975-139">[Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md)</span></span>
  
<span data-ttu-id="57975-140">[Excel ���[�N�V�[�g�Ǝ��̕]��](excel-worksheet-and-expression-evaluation.md)</span><span class="sxs-lookup"><span data-stu-id="57975-140">[Excel Worksheet and Expression Evaluation](excel-worksheet-and-expression-evaluation.md)</span></span>

