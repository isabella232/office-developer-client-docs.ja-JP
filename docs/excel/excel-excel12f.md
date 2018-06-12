---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- excel function [excel 2007],Excel12f function [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798809"
---
# <a name="excelexcel12f"></a><span data-ttu-id="76a23-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="76a23-104">Excel/Excel12f</span></span>

 <span data-ttu-id="76a23-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="76a23-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="76a23-106">フレームワーク ライブラリの機能です。</span><span class="sxs-lookup"><span data-stu-id="76a23-106">Framework library functions.</span></span> <span data-ttu-id="76a23-107">**Excel**は、 [Excel4](excel4-excel12.md)関数のラッパーです。</span><span class="sxs-lookup"><span data-stu-id="76a23-107">**Excel** is a wrapper for the [Excel4](excel4-excel12.md) function.</span></span> <span data-ttu-id="76a23-108">**Excel12f**は、 [Excel12](excel4-excel12.md)関数のラッパーです。</span><span class="sxs-lookup"><span data-stu-id="76a23-108">**Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function.</span></span> <span data-ttu-id="76a23-109">それぞれは、どの引数が 0 で、一時**XLOPER**または**XLOPER12**の作成が失敗したことを示すであることを確認するを確認します。</span><span class="sxs-lookup"><span data-stu-id="76a23-109">Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed.</span></span> <span data-ttu-id="76a23-110">エラーが発生する場合は、各デバッグ メッセージを出力します。</span><span class="sxs-lookup"><span data-stu-id="76a23-110">If an error occurs, each prints a debug message.</span></span> <span data-ttu-id="76a23-111">完了したら、各一時**XLOPER**と**XLOPER12**の作成されている可能性があるすべての一時的なメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="76a23-111">When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="76a23-p102">**Excel12f** �́AExcel 2007 C API ���C�u�����ȍ~�� DLL ����̂݌Ăяo�����Ƃ��ł��܂��B����ɁAExcel 2007 �ȍ~�ŋN�������Ƃ��̂ݓ��삵�A����ȊO�� **xlretFailed** �Ŏ��s���܂��B</span><span class="sxs-lookup"><span data-stu-id="76a23-p102">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library. Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="76a23-114">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="76a23-114">Parameters</span></span>

 <span data-ttu-id="76a23-115">_iFunction_(**int**)</span><span class="sxs-lookup"><span data-stu-id="76a23-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="76a23-p103">�Ăяo���R�}���h�܂��͊֐���������l�B�ڍׂɂ��ẮA[Excel4�AExcel12](excel4-excel12.md) ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="76a23-p103">A number indicating the command or function you want to call. For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="76a23-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="76a23-118">_pxRes_</span></span>
  
<span data-ttu-id="76a23-p104">�]�����ꂽ�֐��̌��ʂ̃|�C���^�B���ʂɎ�����郁�����͂��ׂāAExcel �ɂ���Ċ��蓖�Ă��A�s�v�ɂȂ����� [xlFree](xlfree.md) ��Ăяo���ĉ�����邩�A�܂��� Excel �ɖ߂��ꍇ�� **xlbitXLFree** ��ݒ肵�ĉ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="76a23-p104">A pointer to result of the evaluated function. Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="76a23-121">_iCount_(**int**)</span><span class="sxs-lookup"><span data-stu-id="76a23-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="76a23-p105">�֐��ɓn���������̐��BExcel 2007 �ȍ~�A������ 255 �ɐ�������Ă��܂��B����ȑO�̃o�[�W�����̐����l�� 30 �ł��B</span><span class="sxs-lookup"><span data-stu-id="76a23-p105">The number of arguments that will be passed to the function. Starting in Excel 2007, the limit is 255 arguments. In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="76a23-125">_argument1, ..._</span><span class="sxs-lookup"><span data-stu-id="76a23-125">_argument1, ..._</span></span>
  
<span data-ttu-id="76a23-p106">�ȗ��\�ȁA�֐��̈����B���ׂĂ̈����́A **Excel** �̏ꍇ�� **XLOPER** �ւ̃|�C���^�[�A **Excel12f** �̏ꍇ�� **XLOPER12** �ւ̃|�C���^�[�ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="76a23-p106">The optional arguments to the function. All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="76a23-128">�߂�l</span><span class="sxs-lookup"><span data-stu-id="76a23-128">Return value</span></span>

<span data-ttu-id="76a23-129">どちらの関数は、同じエラーが発生し、 **Excel4**、 **Excel4v**、 **Excel12**、および**Excel12v**としての成功コードを返します。</span><span class="sxs-lookup"><span data-stu-id="76a23-129">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**.</span></span> <span data-ttu-id="76a23-130">これらのコードの詳細については、 [Excel4/Excel12](excel4-excel12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76a23-130">See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes.</span></span> <span data-ttu-id="76a23-131">さらに、これらのフレームワークの機能は、パラメーターに NULL ポインターの場合は、C API を呼び出さずに**xlretFailed**が検出されたを返します。</span><span class="sxs-lookup"><span data-stu-id="76a23-131">In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="76a23-132">��</span><span class="sxs-lookup"><span data-stu-id="76a23-132">Example</span></span>

<span data-ttu-id="76a23-133">���̗�ł́A�s���Ȉ����� **Excel12f** �֐��ɓn���āA�f�o�b�K�[�Ƀ��b�Z�[�W�𑗐M���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="76a23-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="76a23-134">�֘A����</span><span class="sxs-lookup"><span data-stu-id="76a23-134">See also</span></span>



[<span data-ttu-id="76a23-135">Excel4�AExcel12</span><span class="sxs-lookup"><span data-stu-id="76a23-135">Excel4/Excel12</span></span>](excel4-excel12.md)


<span data-ttu-id="76a23-136">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="76a23-136">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

