---
title: �t���[�����[�N ���C�u�����̊֐�
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- framework library functions [excel 2007],functions [Excel 2007], Framework library
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798893"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="f94bd-104">�t���[�����[�N ���C�u�����̊֐�</span><span class="sxs-lookup"><span data-stu-id="f94bd-104">Functions in the Framework Library</span></span>

<span data-ttu-id="f94bd-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f94bd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f94bd-106">フレームワーク ライブラリは、Xll を簡単に記述するために作成されました。</span><span class="sxs-lookup"><span data-stu-id="f94bd-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="f94bd-107">**XLOPER**を管理するための単純な関数が含まれています/ 一時**XLOPER**を作成、**XLOPER12**メモリ/ **XLOPER12**、堅牢 (**Excel4**、 **Excel4v** Microsoft Excel の関数を呼び出す、* * Excel12 * *、* * Excel12v * *) と印刷は、接続されている端末上の文字列をデバッグします。</span><span class="sxs-lookup"><span data-stu-id="f94bd-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, ** Excel12 **, ** Excel12v **) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="f94bd-108">���̃��C�u�����Ɋ܂܂�Ă���֐��́A���̂悤�ȃR�[�h�̈ꕔ��ȗ�������̂ɖ𗧂��܂��B</span><span class="sxs-lookup"><span data-stu-id="f94bd-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="f94bd-109">�ȗ������ꂽ�R�[�h�͎��̗�̂悤�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="f94bd-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="f94bd-110">���̊֐����t���[�����[�N ���C�u�����Ɋ܂܂�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="f94bd-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="f94bd-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="f94bd-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="f94bd-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="f94bd-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="f94bd-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="f94bd-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="f94bd-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="f94bd-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="f94bd-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="f94bd-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="f94bd-116">**XLOPER �Ŏg�p����֐�**</span><span class="sxs-lookup"><span data-stu-id="f94bd-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="f94bd-117">**XLOPER12 �Ŏg�p����֐�**</span><span class="sxs-lookup"><span data-stu-id="f94bd-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f94bd-118">Excel</span><span class="sxs-lookup"><span data-stu-id="f94bd-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="f94bd-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="f94bd-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="f94bd-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="f94bd-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="f94bd-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="f94bd-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="f94bd-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="f94bd-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="f94bd-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="f94bd-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="f94bd-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="f94bd-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="f94bd-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="f94bd-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="f94bd-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="f94bd-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="f94bd-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="f94bd-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="f94bd-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="f94bd-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="f94bd-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="f94bd-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="f94bd-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="f94bd-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="f94bd-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="f94bd-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="f94bd-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="f94bd-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="f94bd-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="f94bd-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="f94bd-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="f94bd-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="f94bd-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="f94bd-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="f94bd-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="f94bd-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="f94bd-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="f94bd-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="f94bd-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="f94bd-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="f94bd-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="f94bd-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="f94bd-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="f94bd-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="f94bd-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="f94bd-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="f94bd-p102">�����̊֐���g�p����ƁADLL �܂��� XLL ��L�q���邽�߂ɕK�v�Ȏ��Ԃ�Z���ł��܂��B�܂��A�T���v�� �A�v���P�[�V���� GENERIC ����J����J�n���Ă�J�����Ԃ�Z�k�ł��܂��BGENERIC.C ��e���v���[�g�Ƃ��Ďg�p���āAXLL �̃t���[�����[�N��Z�b�g�A�b�v���Ă���A�����̃R�[�h��Ǝ��̃R�[�h�ɒu�������邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="f94bd-p102">Use of these functions shortens the amount of time required to write a DLL or XLL. Starting development from the sample application GENERIC also shortens development time. Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="f94bd-p103">�ꎞ�I�� **XLOPER**/ **XLOPER12** �֐��́A�t���[�����[�N ���C�u�����ɂ���ĊǗ�����郍�[�J�� �q�[�v�̃�������g�p���� **XLOPER**/ **XLOPER12** �l��쐬���܂��B **FreeAllTempMemory** �֐��A������� /  �֐��܂��� **Excel12f** �֐��̂����ꂩ��Ăяo���܂ŁA **XLOPER********XLOPER12** �̒l�͗L���Ȃ܂܈ێ�����܂��B( **Excel** �֐��� **Excel12f** �֐��́A���ʂ�Ԃ��O�ɂ��ׂĂ̈ꎞ�������������܂��B)</span><span class="sxs-lookup"><span data-stu-id="f94bd-p103">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library. The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions. (The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="f94bd-148">�t���[�����[�N ���C�u�����̊֐���g�p����ɂ́AFRAMEWRK.H �t�@�C���� C �R�[�h�Ɋ܂߁AFRAMEWRK.C �t�@�C���܂��� FRMWRK32.LIB �t�@�C����R�[�h �v���W�F�N�g�ɒǉ�����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="f94bd-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f94bd-149">�֘A����</span><span class="sxs-lookup"><span data-stu-id="f94bd-149">See also</span></span>

- [<span data-ttu-id="f94bd-150">Excel XLL SDK API �֐����t�@�����X</span><span class="sxs-lookup"><span data-stu-id="f94bd-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

