---
title: Excel �̃������Ǘ�
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 memory [excel 2007],managing memory in Excel,Excel stack,strings [Excel 2007], managing memory,memory management in Excel,XLOPER memory [Excel 2007],memory [Excel 2007], management guidelines
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 97c76d762fdc5e575c571804816e5581a7bec8bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798937"
---
# <a name="memory-management-in-excel"></a><span data-ttu-id="48b7f-104">Excel �̃������Ǘ�</span><span class="sxs-lookup"><span data-stu-id="48b7f-104">Memory Management in Excel</span></span>

 <span data-ttu-id="48b7f-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="48b7f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="48b7f-p101">�����I�ň��肵�� XLL ��쐬����ꍇ�ɂ́A�������Ǘ����ł�d�v�ȉۑ�ƂȂ�܂��B��������Ǘ��ł��Ȃ��� Microsoft Excel �ŗl�X�Ȗ�肪������\��������܂��B���Ƃ��΁A���������蓖�Ă⏉�����̌����������Ȃ�����A���K�͂ȃ����� ���[�N���������肷��Ƃ�������r�I�����Ȗ�肩��AExcel ���s����ɂȂ�Ƃ������傫�Ȗ��Ȃǂ��N���錴���ƂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p101">Memory management is the most important concern if you want to create efficient and stable XLLs. Failure to manage memory well can lead to a range of problems in Microsoft Excel—from minor problems such as inefficient memory allocation and initialization and small memory leaks, to major problems such as the destabilization of Excel.</span></span>
  
<span data-ttu-id="48b7f-p102">�A�h�C���֘A�̐[���Ȗ��̍ł��ʓI�Ȍ������A�������Ǘ��̎��s�ɂ���܂��B���������āA�v���W�F�N�g��r���h����ہA��ѐ�������A�\���ɍl�������������Ǘ��̐헪��g�p����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p102">Mismanagement of memory is the most common source of serious add-in-related problems. Therefore, you should build your project with a consistent and well-thought-through strategy on memory management.</span></span> 
  
<span data-ttu-id="48b7f-p103">Microsoft Office Excel 2007 �ł̓}���\`�X���b�h�̃u�b�N�Čv�Z�̓����ɔ����A�������Ǘ�������܂ňȏ�ɕ��G�ɂȂ�܂����B�X���b�h �Z�[�t�ȃ��[�N�V�[�g�֐���쐬���ăG�N�X�|�[�g����ꍇ�́A�����̃X���b�h���A�N�Z�X�Ɋւ��ċ�������Ƃ��ɐ�����\�������鋣����Ԃ�Ǘ����Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p103">Memory management became more complex in Microsoft Office Excel 2007 with the introduction of multithreaded workbook recalculation. If you want to create and export thread-safe worksheet functions, you must manage the resulting conflicts that can occur when multiple threads compete for access.</span></span>
  
<span data-ttu-id="48b7f-112">���� 3 �̃f�[�^�\���̌^�Ɋւ��郁�����̍l������������܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-112">There are memory considerations for the following three data structure types:</span></span>
  
- <span data-ttu-id="48b7f-113">**XLOPER** �� **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="48b7f-113">**XLOPER**s and **XLOPER12**s</span></span>
    
- <span data-ttu-id="48b7f-114">**XLOPER** �ł� **XLOPER12** �ł�Ȃ�������</span><span class="sxs-lookup"><span data-stu-id="48b7f-114">Strings that are not in an **XLOPER** or **XLOPER12**</span></span>
    
- <span data-ttu-id="48b7f-115">**FP** �z��� **FP12** �z��</span><span class="sxs-lookup"><span data-stu-id="48b7f-115">**FP** and **FP12** arrays</span></span> 
    
## <a name="xloperxloper12-memory"></a><span data-ttu-id="48b7f-116">XLOPER/XLOPER12 ������</span><span class="sxs-lookup"><span data-stu-id="48b7f-116">XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="48b7f-117">**XLOPER**/ **XLOPER12**のデータ構造体には、つまり文字列 (**xltypeStr**)、配列 (**xltypeMulti**) および外部参照 (**xltypeRef**) のメモリ ブロックへのポインターが含まれているいくつかのサブタイプです。</span><span class="sxs-lookup"><span data-stu-id="48b7f-117">The **XLOPER**/ **XLOPER12** data structure has a few sub-types that contain pointers to blocks of memory, namely strings (**xltypeStr**), arrays (**xltypeMulti**) and external references (**xltypeRef**).</span></span> <span data-ttu-id="48b7f-118">**XLOPER**の文字列を**xltypeMulti**配列に含められることにも注意してください/ **XLOPER12s**に他のメモリ ブロックを指す。</span><span class="sxs-lookup"><span data-stu-id="48b7f-118">Note also that **xltypeMulti** arrays can contain string **XLOPER**/ **XLOPER12s** that in turn point to other blocks of memory.</span></span> 
  
<span data-ttu-id="48b7f-119">**XLOPER**/ **XLOPER12** �́A���̂悤�ɂ������̕��@�ō쐬����܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-119">An **XLOPER**/ **XLOPER12** can be created in several ways:</span></span> 
  
- <span data-ttu-id="48b7f-120">Excel �ɂ���āBXLL �֐��ɓn�����������������Ƃ�</span><span class="sxs-lookup"><span data-stu-id="48b7f-120">By Excel when preparing arguments to be passed to an XLL function</span></span>
    
- <span data-ttu-id="48b7f-121">Excel �ɂ���āBC API �Ăяo���� **XLOPER** �܂��� **XLOPER12** ���Ԃ����Ƃ�</span><span class="sxs-lookup"><span data-stu-id="48b7f-121">By Excel when returning an **XLOPER** or **XLOPER12** in a C API call</span></span> 
    
- <span data-ttu-id="48b7f-122">DLL �ɂ���āBC API �Ăяo���ɓn����������쐬����Ƃ�</span><span class="sxs-lookup"><span data-stu-id="48b7f-122">By your DLL when creating arguments to be passed to a C API call</span></span>
    
- <span data-ttu-id="48b7f-123">DLL �ɂ���āBXLL �֐��̖߂�l��쐬����Ƃ�</span><span class="sxs-lookup"><span data-stu-id="48b7f-123">By your DLL when creating an XLL function return value</span></span>
    
<span data-ttu-id="48b7f-124">�����ꂩ�̃����� �|�C���g�^�̃����� �u���b�N�́A���̂������̕��@�Ŋ��蓖�Ă邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-124">A block of memory within one of the memory-pointing types can be allocated in several ways:</span></span>
  
- <span data-ttu-id="48b7f-125">�֐��R�[�h�O�� DLL �ŐÓI�u���b�N�Ƃ��邱�Ƃ��ł��܂��B���̏ꍇ�A����������蓖�Ă����������肷��K�v�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-125">It can be a static block within your DLL outside any function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="48b7f-126">�֐��R�[�h��� DLL �ŐÓI�u���b�N�Ƃ��邱�Ƃ��ł��܂��B���̏ꍇ�A����������蓖�Ă����������肷��K�v�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-126">It can be a static block within your DLL within some function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="48b7f-127">DLL �œ��I�Ɋ��蓖�Ă�����������ł��܂��B���̂��߂ɂ́A **malloc** �� **free**�A **new** �� **delete** �Ȃǂ̕��@������܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-127">It can be dynamically allocated and freed by your DLL in several possible ways: **malloc** and **free**, **new** and **delete**, and so on.</span></span>
    
- <span data-ttu-id="48b7f-128">Excel �œ��I�Ɋ��蓖�Ă邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-128">It can be dynamically allocated by Excel.</span></span>
    
<span data-ttu-id="48b7f-p105">���X���݂���\�������� **XLOPER**/ **XLOPER12** �������̐��� **XLOPER**/ **XLOPER12** �Ƀ����������蓖�Ă�ꂽ�󋵂̑��l���ɂ��čl������ƁA�ƂĂ������Ɏv���Ă����������܂���B�������A���ɋL���������̋K���ƃK�C�h���C���ɏ]���ƁA���G����啝�ɍ팸�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p105">Given the number of possible origins for **XLOPER**/ **XLOPER12** memory and the number of situations in which the **XLOPER**/ **XLOPER12** might have had that memory assigned, it is not surprising that this subject can seem very difficult. However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> 
  
### <a name="rules-for-working-with-xloperxloper12"></a><span data-ttu-id="48b7f-131">XLOPER/XLOPER12 ������Ƃ��̋K��</span><span class="sxs-lookup"><span data-stu-id="48b7f-131">Rules for Working with XLOPER/XLOPER12</span></span>

- <span data-ttu-id="48b7f-p106">����������������AXLL �֐��Ɉ����Ƃ��ēn����� **XLOPERs**/ **XLOPER12** ��㏑�����Ȃ��ł��������B�������������͓ǂݎ���p�ɂ���K�v������܂��B�ڂ����́A�u **Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��**�v�́u�C�� �v���[�X�̈�����ύX���� **XLOPER** �܂��� [XLOPER12](known-issues-in-excel-xll-development.md) ��Ԃ��v��������������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p106">Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12**s that are passed as arguments to your XLL function. You should treat such arguments as read-only. For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
    
- <span data-ttu-id="48b7f-135">C API �ւ̌Ăяo���ŁADLL �ɕԂ���� **XLOPER**/ **XLOPER12** �� Excel ������������蓖�Ă��ꍇ:</span><span class="sxs-lookup"><span data-stu-id="48b7f-135">If Excel has allocated memory for an **XLOPER**/ **XLOPER12** returned to your DLL in a call to the C API:</span></span> 
    
  - <span data-ttu-id="48b7f-p107">**XLOPER**/ **XLOPER12** ���s�v�ɂȂ�ꍇ�A [xlFree](xlfree.md) ��Ăяo���ă������������Ȃ���΂Ȃ�܂���B���̑��̕��@ (free�Adelete �Ȃ�) ��g�p���ă������������Ȃ��ł��������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p107">You must free the memory when you no longer need the **XLOPER**/ **XLOPER12** using a call to [xlFree](xlfree.md). Do not use any other method, such as free or delete, to release the memory.</span></span>
    
  - <span data-ttu-id="48b7f-138">�Ԃ����^�� **xltypeMulti** �̂Ƃ��A�z���� **XLOPER**/ **XLOPER12** ��㏑�����Ȃ��ł��������B���ɁA�����񂪊܂܂�Ă���ꍇ�A����ѕ�����ŏ㏑�����悤�Ƃ��Ă���̂ł͂Ȃ��ꍇ�ɒ��ӂ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-138">If the returned type is **xltypeMulti**, do not overwrite any **XLOPER**/ **XLOPER12**s within the array, especially if they contain strings, and especially not where you are trying to overwrite with a string.</span></span>
    
  - <span data-ttu-id="48b7f-139">DLL �֐��̖߂�l�Ƃ��� **XLOPER**/ **XLOPER12** �� Excel �ɕԂ��ꍇ�AExcel �ɑ΂��āA�s�v�ɂȂ�����������K�v�����郁���������݂��邱�Ƃ�ʒm���Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-139">If you want to return the **XLOPER**/ **XLOPER12** to Excel as your DLL function's return value, you must tell Excel that there is memory that Excel must release when done.</span></span> 
    
- <span data-ttu-id="48b7f-140">C API �Ăяo���ɑ΂���߂�l�Ƃ��č쐬���ꂽ **XLOPER******/  �ł� **xlFree** �݂̂�Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-140">You must only call **xlFree** on an **XLOPER**/ **XLOPER12** that was created as the return value to a C API call.</span></span> 
    
- <span data-ttu-id="48b7f-141">DLL �֐��̖߂�l�Ƃ��� Excel �ɕԂ� **XLOPER**/ **XLOPER12** �� DLL ������������蓖�Ă��ꍇ�ɂ́ADLL ���������K�v�����郁���������݂��邱�Ƃ� Excel �ɒʒm���Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-141">If your DLL has allocated memory for an **XLOPER**/ **XLOPER12** that you want to return to Excel as your DLL function's return value, you must tell Excel that there is memory that the DLL must release.</span></span> 
    
### <a name="guidelines-for-memory-management"></a><span data-ttu-id="48b7f-142">�������Ǘ��̃K�C�h���C��</span><span class="sxs-lookup"><span data-stu-id="48b7f-142">Guidelines for Memory Management</span></span>

- <span data-ttu-id="48b7f-p108">����������蓖�Ăĉ�����邽�߂Ɏg�p���郁�\�b�h�� DLL ��ň�т����܂��B�قȂ郁�\�b�h�����݂��Ȃ��悤�ɂ��܂��B������ �N���X�܂��͍\���̂Ŏg�p���郁�\�b�h����b�v���A�Ώۃ��\�b�h���g�p����Ă��鑽���̏ꏊ�ŃR�[�h��ς��Ȃ��Ă�ύX�ł���悤�ɂ��邱�Ƃ�����߂��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p108">Be consistent in your DLL in the method that you use to allocate and release memory. Avoid mixing methods. A good approach is to wrap the method that you are using up in a memory class or structure, within which you can change the method used without altering your code in many places.</span></span>
    
- <span data-ttu-id="48b7f-p109">DLL �� **xltypeMulti** �z���쐬����ꍇ�A������Ƀ���������蓖�Ă���@���т����Ă��������B�K���������𓮓I�Ɋ��蓖�Ă邩�A�K���ÓI��������g�p���邩�̂ǂ��炩�ɂ��Ă��������B�������Ă����΁A��������������Ƃ��ɁA�������K��������邩�A������Ă͂Ȃ�Ȃ�����������܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p109">When you create **xltypeMulti** arrays within your DLL, be consistent in the way that you allocate memory for strings: always dynamically allocate the memory for them or always use static memory. If you do this, when you are freeing the memory, you will know that you must either always or never free the strings.</span></span> 
    
- <span data-ttu-id="48b7f-148">Excel ���쐬���� **XLOPER**/ **XLOPER12** ��R�s�[����Ƃ��́AExcel �����蓖�Ă���������ڍ׃R�s�[���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-148">Make deep copies of Excel-allocated memory when you are copying an Excel-created **XLOPER**/ **XLOPER12**.</span></span>
    
- <span data-ttu-id="48b7f-p110">Excel �����蓖�Ă������� **XLOPER**/ **XLOPER12** �� **xltypeMulti** �z���ɔz�u���Ȃ��ł��������B������̏ڍ׃R�s�[��쐬���A���̃R�s�[�ւ̃|�C���^�[��z���Ɋi�[���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p110">Do not put Excel-allocated string **XLOPER**/ **XLOPER12**s within **xltypeMulti** arrays. Make deep copies of the strings and store pointers to the copies in the array.</span></span> 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a><span data-ttu-id="48b7f-151">Excel �����蓖�Ă� XLOPER/XLOPER12 ��������������</span><span class="sxs-lookup"><span data-stu-id="48b7f-151">Freeing Excel-Allocated XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="48b7f-152">���� XLL �R�}���h�ɂ��čl�����܂��B���̃R�}���h�́A **xlGetName** ��g�p���āADLL �̃p�X�ƃt�@�C������܂ޕ������擾���A **xlcAlert** ��g�p���Čx���_�C�A���O �{�b�N�X�ɕ\�����܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-152">Consider the following XLL command, which uses **xlGetName** to obtain a string containing the path and file name of the DLL and displays it in an alert dialog box using **xlcAlert**.</span></span>
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

<span data-ttu-id="48b7f-153">���̊֐��� **xDllName** �ɂ���ă|�C���g����Ă��郁������K�v�Ƃ��Ȃ��Ȃ����Ȃ�ADLL ��p C API �֐��� 1 �ł��� [xlFree �֐�](xlfree.md)�ւ̌Ăяo����g�p���ĉ���ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-153">When the function no longer needs the memory pointed to by **xDllName**, it can free it using a call to the [xlFree function](xlfree.md), one of the DLL-only C API functions.</span></span> 
  
<span data-ttu-id="48b7f-154">**xlFree** �֐��ɂ��Ă͊֐����t�@�����X �Z�N�V���� (�u [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)�v�������������) �ɏڍׂ��L����Ă��܂����A�ȉ��̓_�ɒ��ӂ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-154">The **xlFree** function is fully documented in the function reference section (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), but be aware of the following:</span></span>
  
- <span data-ttu-id="48b7f-155">**xlFree** �ւ� 1 ��̌Ăяo���ŕ����� / ******XLOPER12** �ւ̃|�C���^�[��n�����Ƃ��ł��܂��B�������A���s����Ă��� Excel �o�[�W�����ŃT�|�[�g����Ă��鐔�̊֐������Ɍ��肳��܂� (Excel 2003 �̏ꍇ�ɂ� 30�AExcel 2007 �ȍ~�ł� 255)�B</span><span class="sxs-lookup"><span data-stu-id="48b7f-155">You can pass pointers to more than one **XLOPER**/ **XLOPER12**s in a single call to **xlFree**, limited only by the number of function arguments supported in the running version of Excel (30 in Excel 2003, 255 starting in Excel 2007).</span></span>
    
- <span data-ttu-id="48b7f-p111">**xlFree** �͊܂܂�Ă���|�C���^�[�� **NULL** �ɐݒ肵�A���ɉ�����ꂽ **XLOPER**/ **XLOPER12** �������悤�Ƃ��Ă���S�ȏ�Ԃ�m�ۂ��܂��B **xlFree** �́A������ύX����B��� C API �֐��ł��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p111">**xlFree** sets the contained pointer to **NULL** to ensure that an attempt to free an **XLOPER**/ **XLOPER12** that has already been freed is safe. **xlFree** is the only C API function that modifies its arguments.</span></span> 
    
- <span data-ttu-id="48b7f-158">�������ւ̃|�C���^�[���܂܂�邩�ǂ����Ɋ֌W�Ȃ��AC API �ւ̌Ăяo���̖߂�l�Ɏg�p�����C�ӂ� **XLOPER******/  �� **xlFree** ����S�ɌĂяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-158">You can safely call **xlFree** on any **XLOPER**/ **XLOPER12** used for the return value of a call to the C API, regardless of whether it contains a pointer to memory.</span></span> 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a><span data-ttu-id="48b7f-159">Excel �ŉ������� XLOPER/XLOPER12 ��Ԃ�</span><span class="sxs-lookup"><span data-stu-id="48b7f-159">Returning XLOPER/XLOPER12s to be freed by Excel</span></span>

<span data-ttu-id="48b7f-p112">�O�̃Z�N�V�����ɋL����Ă���R�}���h���A **Boolean** **true** �������n�����Ƃ��ɂ� DLL �p�X�ƃt�@�C������Ԃ��A����ȊO�̏ꍇ�ɂ� **#N/A** ��Ԃ����[�N�V�[�g�֐��ɕύX����ꍇ�ɂ��čl���܂��BExcel �ɕԂ����O�� **xlFree** ��Ăяo���ĕ����񃁃��������ł��Ȃ����Ƃ͖����ł��B�������A�����ꂩ�̎��_�ŉ������Ȃ��ƁA�A�h�C���͊֐����Ăяo����邽�тɃ����� ���[�N��N�����܂��B���̖�������邽�߁Axlcall.h �� **xlbitXLFree** �Ƃ��Ē�\`����Ă���A **XLOPER**/ **XLOPER12** �� **xltype** �t�B�[���h�Ƀr�b�g��ݒ�ł��܂��B�����ݒ肷�邱�Ƃɂ���āA�l�̃R�s�[���I�������Ƃ��ɁA�Ԃ��ꂽ��������������K�v�����邱�Ƃ� Excel �ɒʒm���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p112">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise. Clearly you cannot call **xlFree** to release the string memory before returning it to Excel. However, if it is not freed at some point, the add-in will leak memory every time the function is called. To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h. Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span></span> 
  
### <a name="example"></a><span data-ttu-id="48b7f-165">��</span><span class="sxs-lookup"><span data-stu-id="48b7f-165">Example</span></span>

<span data-ttu-id="48b7f-166">���̃R�[�h��́AXLL ���[�N�V�[�g�֐��ɕϊ����ꂽ�A�O�̃Z�N�V������ XLL �R�}���h������Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-166">The following code example shows the XLL command in the previous section converted into an XLL worksheet function.</span></span>
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

<span data-ttu-id="48b7f-p113">**XLOPER**/ **XLOPER12** ��g�p���� XLL �֐��́A **XLOPER**/ **XLOPER12** �ւ̃|�C���^�[��擾���߂���̂Ƃ��Ē�\`����K�v������܂��B���̊֐���Ŏg�p����Ă���T���v���̐ÓI **XLOPER12** �̓X���b�h �Z�[�t�ł͂���܂���B�s�K�؂ɂ���̊֐���X���b�h �Z�[�t�Ƃ��ēo�^���邱�Ƃ͂ł��܂����A����X���b�h�� **xRtnValue** �̏�����I������O�ɕʂ̃X���b�h���㏑�����Ă��܂��Ƃ����댯�������܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p113">XLL functions that use **XLOPER**/ **XLOPER12**s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12**s. The use in this example of a static **XLOPER12** within the function is not thread safe. You could incorrectly register this function as thread safe, but you would risk **xRtnValue** being overwritten by one thread before another thread had finished with it.</span></span> 
  
<span data-ttu-id="48b7f-p114">**xlbitXLFree** �̐ݒ�́A���蓖�Ă�s�� Excel �R�[���o�b�N�ւ̌Ăяo����ɍs���K�v������܂��B�ݒ���ɍs���ƁA�㏑������āA�K�v�ȓ��삪�����܂���B�ʂ� C API �֐��ւ̌Ăяo���Œl������Ƃ��Ďg�p���Ă��烏�[�N�V�[�g�ɖ߂��ꍇ�ɂ́A���̂悤�ȌĂяo����ɂ��̃r�b�g��ݒ肵�Ă��������B���̂悤�ɂ��Ȃ��ƁA **XLOPER**/ **XLLOPER12** �^�̃\`�F�b�N����܂ŁA���̃r�b�g��}�X�N���Ȃ��֐����������Ă��܂��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p114">You must set **xlbitXLFree** after the call to the Excel callback that allocates it. If you set it before this, it is overwritten and does not have the effect that you want. If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call. Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type.</span></span> 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a><span data-ttu-id="48b7f-174">DLL �ŉ������� XLOPER/XLOPER12 ��Ԃ�</span><span class="sxs-lookup"><span data-stu-id="48b7f-174">Returning XLOPER/XLOPER12s to be freed by the DLL</span></span>

<span data-ttu-id="48b7f-p115">���l�̖�肪�A **XLOPER**/ **XLOPER12** �̃������� XLL �����蓖�ĂāAExcel �ɖ߂��ꍇ�ɐ����܂��BExcel �́Axlcall.h �� **xlbitDLLFree** �Ƃ��Ē�\`����Ă���A **XLOPER**/ **XLOPER12** �� **xltype** �t�B�[���h�ɐݒ�\�ȕʂ̃r�b�g��F�����܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p115">A similar problem to this occurs when your XLL has allocated memory for an **XLOPER**/ **XLOPER12** and wants to return it to Excel. Excel recognizes another bit that can be set in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitDLLFree** in xlcall.h.</span></span> 
  
<span data-ttu-id="48b7f-177">Excel が **、XLOPER**を受け取ると/ この**XLOPER12**ビットが設定、( **XLOPER**s) の[xlAutoFree](xlautofree-xlautofree12.md)または**XLOPER12**秒) ( **xlAutoFree12**と呼ばれる xll ファイルをエクスポートするようにする関数を呼び出すしようとします。</span><span class="sxs-lookup"><span data-stu-id="48b7f-177">When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s).</span></span> <span data-ttu-id="48b7f-178">この関数は、関数リファレンスで詳しく説明が ([マネージャー、XLL インターフェイスの関数](add-in-manager-and-xll-interface-functions.md)を参照)、ですが、最低限の実装例をここで指定します。</span><span class="sxs-lookup"><span data-stu-id="48b7f-178">This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here.</span></span> <span data-ttu-id="48b7f-179">**XLOPER**を解放するための目的は、/ 最初割り当てられた方法に一貫性のある方法でメモリを**XLOPER12** 。</span><span class="sxs-lookup"><span data-stu-id="48b7f-179">Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated.</span></span> 
  
### <a name="examples"></a><span data-ttu-id="48b7f-180">��</span><span class="sxs-lookup"><span data-stu-id="48b7f-180">Examples</span></span>

<span data-ttu-id="48b7f-181">���̊֐���́A�O�q�̊֐��Ɠ����ł��B��O�́ADLL ���̑O�ɁuThe full pathname for this DLL is�v�Ƃ����e�L�X�g���܂܂�Ă���_�ł��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-181">The following example function does the same as the previous function except that it includes the text "The full pathname for this DLL is " before the DLL name.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

<span data-ttu-id="48b7f-182">�O�q�̊֐���G�N�X�|�[�g�����AXLL �ɂ����� **xlAutoFree12** �̍ŏ����̎�������Ɏ����܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-182">A minimally sufficient implementation of **xlAutoFree12** in the XLL that exported the previous function would be as follows.</span></span> 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

<span data-ttu-id="48b7f-p117">���̎����́AXLL �� **XLOPER12** �����񂾂���߂��A�����̕������ **malloc** �݂̂�g�p���Ċ��蓖�Ă�ꍇ�Ɍ���g�p�ł��܂��B���̃e�X�g</span><span class="sxs-lookup"><span data-stu-id="48b7f-p117">This implementation is only sufficient if the XLL only returns **XLOPER12** strings, and those strings are only allocated using **malloc**. Note that the test</span></span> 
  
 ` if(p_oper->xltype == xltypeStr) `
  
<span data-ttu-id="48b7f-185">�͎��s���邱�Ƃɒ��ӂ��Ă��������B **xlbitDLLFree** ���ݒ肳��Ă��邽�߂ł�</span><span class="sxs-lookup"><span data-stu-id="48b7f-185">would fail in this case because **xlbitDLLFree** is set.</span></span> 
  
<span data-ttu-id="48b7f-186">��ʂɁA **xlAutoFree** �� **xlAutoFree12** ��������AXLL �쐬�� **xltypeMulti** �z��� **xltypeRef** �O���Q�ƂɊ֘A���������������ł���悤�ɂ��Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-186">In general, **xlAutoFree** and **xlAutoFree12** should be implemented so that they free memory associated with XLL-created **xltypeMulti** arrays and **xltypeRef** external references.</span></span> 
  
<span data-ttu-id="48b7f-p118">���ׂĂ̏ꍇ�ɓ��I�Ɋ��蓖�Ă�ꂽ **XLOPER** �� **XLOPER12** ��Ԃ��悤�� XLL �֐���������邱�Ƃ�ł��܂��B���̏ꍇ�A **xlbitDLLFree** ��A�T�u�^�C�v�Ɋ֌W�Ȃ��A�����������ׂĂ� **XLOPER** �� **XLOPER12** �Őݒ肷��K�v������܂��B�܂��A���̃������� **XLOPER********XLOPER12** ��Ń|�C���g����郁�������������悤�ɁA /  �� **xlAutoFree12** ���������K�v����邩�����܂���B����́A�߂�l��X���b�h �Z�[�t�ɂ��� 1 �̕��@�ł��B���Ƃ��΁A�O�q�̊֐�����̂悤�ɏ��������邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p118">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s. In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type. You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**. This approach is one way to make the return value thread safe. For example, the previous function could be rewritten as follows.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

<span data-ttu-id="48b7f-192">**xlAutoFree** �� **xlAutoFree12** �ɂ��ďڂ����́A�u [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md)�v��������������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-192">For more information about **xlAutoFree** and **xlAutoFree12**, see [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span></span>
  
## <a name="returning-modify-in-place-arguments"></a><span data-ttu-id="48b7f-193">�ύX�C���v���[�X������Ԃ�</span><span class="sxs-lookup"><span data-stu-id="48b7f-193">Returning Modify-in-Place Arguments</span></span>

<span data-ttu-id="48b7f-p119">Excel �ł́AXLL �֐��̓C���v���[�X�ň�����ύX���Ēl��Ԃ����Ƃ��ł��܂��B���̑���́A�|�C���^�[�Ƃ��ēn���ꂽ�����ł̂ݍs�����Ƃ��ł��܂��B���̂悤�ȏ�����s���ɂ́A�֐���o�^����Ƃ��ɁA�ύX�Ώۂ̈����� Excel �ɒʒm���Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p119">Excel allows an XLL function to return a value by modifying an argument in place. You can only do this with an argument passed in as a pointer. To work like this, the function must be registered in a way that tells Excel which argument will be modified.</span></span> 
  
<span data-ttu-id="48b7f-197">���̕��@�Œl��Ԃ����Ƃ́A�|�C���^�[�œn�����Ƃ��ł��邷�ׂẴf�[�^�^�ŃT�|�[�g����Ă��܂����A���Ɉȉ��̌^�ŕ֗��ł��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-197">This method of returning a value is supported for all data types that can be passed by pointer but is especially useful for the following types:</span></span>
  
- <span data-ttu-id="48b7f-198">�������J�E���g����Anull �ŏI������ ASCII �o�C�g������</span><span class="sxs-lookup"><span data-stu-id="48b7f-198">Length-counted and null-terminated ASCII byte strings</span></span>
    
- <span data-ttu-id="48b7f-199">�������J�E���g����Anull �ŏI������ Unicode ���C�h���������� (Excel 2007 �ȍ~)</span><span class="sxs-lookup"><span data-stu-id="48b7f-199">Length-counted and null-terminated Unicode wide character strings (starting in Excel 2007)</span></span>
    
- <span data-ttu-id="48b7f-200">**FP** ���������_�z��</span><span class="sxs-lookup"><span data-stu-id="48b7f-200">**FP** floating-point arrays</span></span> 
    
- <span data-ttu-id="48b7f-201">**FP12** ���������_�z�� (Excel 2007 �ȍ~)</span><span class="sxs-lookup"><span data-stu-id="48b7f-201">**FP12** floating-point arrays (starting in Excel 2007)</span></span> 
    
> [!NOTE]
> <span data-ttu-id="48b7f-p120">[!����] ���̕��@�ŁA **XLOPER** �� **XLOPER12** ��Ԃ��Ȃ��ł��������B�ڂ����́A�u [Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p120">You should not try to return **XLOPER**s or **XLOPER12**s in this manner. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
<span data-ttu-id="48b7f-p121">return ステートメントの代わりにこの手法を使用する利点は、Excel が戻り値のメモリを割り当てるという点です。返されたデータの処理を Excel が完了すれば、メモリを解放します。これにより、XLL 関数はメモリ管理タスクを行わなくて済みます。この手法は、スレッド セーフです。別々のスレッドで同時に Excel によって呼び出された場合、各スレッドの各関数呼び出しは独自のバッファーを持ちます。</span><span class="sxs-lookup"><span data-stu-id="48b7f-p121">The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values. Once Excel has finished reading the returned data, it releases the memory. This takes the memory management tasks away from the XLL function. This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.</span></span>
  
<span data-ttu-id="48b7f-p122">����́A���ɑO�ɂ������f�[�^�^�Ŗ𗧂����܂��B **XLOPER**/ **XLOPER12** �ɑ΂��đ��݂���Ԃ��ꂽ���ƂɃ������������邽�߂� DLL �ւ̃R�[���o�b�N ���J�j�Y���́A�P���ȕ������ **FP**/ **FP12** �z��ɂ͂Ȃ����߂ł��B���̂��߁ADLL �쐬�̕�����܂��͕��������_�z���Ԃ��ꍇ�A���̑I���������܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p122">It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for **XLOPER**/ **XLOPER12**s does not exist for simple strings and **FP**/ **FP12** arrays. Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> 
  
- <span data-ttu-id="48b7f-p123">���I�Ɋ��蓖�Ă�ꂽ�o�b�t�@�[�ɌŒ�|�C���^�[��ݒ肵�A���̃|�C���^�[��Ԃ��܂��B�֐�����ɌĂяo���Ƃ��ɁA(1) �|�C���^�[�� null �ł͂Ȃ����Ƃ�\`�F�b�N���A(2) �ȑO�̌Ăяo���Ŋ��蓖�Ă�ꂽ���\�[�X�������A�|�C���^�[�� null �Ƀ��Z�b�g���܂��B(3) �V���Ɋ��蓖�Ă�ꂽ������ �u���b�N�ɂ��̃|�C���^�[��ė��p���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p123">Set a persistent pointer to a dynamically allocated buffer, return the pointer. On the next call to the function (1) check that the pointer is not null, (2) free the resources allocated on the previous call and reset the pointer to null, (3) reuse the pointer for a newly allocated block of memory.</span></span>
    
- <span data-ttu-id="48b7f-212">������Ɣz���A�������K�v���Ȃ��ÓI�o�b�t�@�[�ɍ쐬���A���̃o�b�t�@�[�ւ̃|�C���^�[��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-212">Create your strings and arrays in a static buffer that does not need to be freed, and return a pointer to that.</span></span>
    
- <span data-ttu-id="48b7f-213">������C���v���[�X�ŕύX���܂��B���̍ہA������܂��͔z��� Excel �O�̗̈�ɒ��ڏ������݂܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-213">Modify an argument in place, writing your string or array directly into the space set aside by Excel.</span></span>
    
<span data-ttu-id="48b7f-214">����ȊO�̕��@�Ń��\�[�X������[�X����ɂ́A **XLOPER**/ **XLOPER12** ��쐬���A **xlbitDLLFree** �� **xlAutoFree**/ **xlAutoFree12** ��g�p����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-214">Otherwise, you must create an **XLOPER**/ **XLOPER12**, and use **xlbitDLLFree** and **xlAutoFree**/ **xlAutoFree12** to release the resources.</span></span> 
  
<span data-ttu-id="48b7f-215">最後のオプションは、その場合は、渡されるが同じ型の引数、戻り値として最も簡単な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="48b7f-215">The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value.</span></span> <span data-ttu-id="48b7f-216">重要なポイントは、バッファー サイズの制限は、オーバーランが発生しないことは十分に注意する必要がありますです。</span><span class="sxs-lookup"><span data-stu-id="48b7f-216">The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them.</span></span> <span data-ttu-id="48b7f-217">この間違ったを取得すると、Excel がクラッシュする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="48b7f-217">Getting this wrong could crash Excel.</span></span> <span data-ttu-id="48b7f-218">バッファー サイズの文字列と**FP**/ **FP12**の配列は次に説明します。</span><span class="sxs-lookup"><span data-stu-id="48b7f-218">Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next.</span></span> 
  
## <a name="strings"></a><span data-ttu-id="48b7f-219">������</span><span class="sxs-lookup"><span data-stu-id="48b7f-219">Strings</span></span>

<span data-ttu-id="48b7f-220">������̃������Ǘ��Ɋւ����肪�A�A�v���P�[�V�����ƃA�h�C�����s����ɂȂ�ł��ʓI�Ȍ����ł��B����������������@ (null �I���܂��͒����J�E���g (���邢�͂��̗���)�A�ÓI�o�b�t�@�[�܂��͓��I�o�b�t�@�[�A�Œ蒷�܂��͂قږ������̒����A�I�y���[�e�B���O �V�X�e���Ǘ������� (���Ƃ��΁AOLE Bstr �Ȃ�)�A�A���}�l�[�W������Ȃ�) �����l�Ȃ��Ƃ�l������ƁA����͗���ł��Ȃ����Ƃł͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-220">Problems with the management of string memory are arguably the most common cause of instability in applications and add-ins. It is understandable perhaps, given the variety of ways in which strings are handled: null-terminated or length-counted (or both); static or dynamic buffers; fixed length or almost unlimited length; operating-system managed memory (for example, OLE Bstr) or unmanaged strings; and so on.</span></span>
  
<span data-ttu-id="48b7f-p125">C/C++ �v���O���}�́Anull �I���̕�����ɂ悭���ʂ��Ă��܂��B�W�� C ���C�u�����́A���̂悤�ȕ������������邽�߂ɐ݌v����Ă��܂��B�R�[�h��̐ÓI�����񃊃e�����́Anull �I��������ɃR���p�C������܂��B�܂��AExcel �ł́A�ʏ�� null �I���ł͂Ȃ������J�E���g�̕������������܂��B��������������g�ݍ��킳��Ă���󋵂ł́A������ƕ����񃁃��������������@�Ɋւ��āADLL/XLL ��Ŗ��m����ѐ��̂�����@���K�v�ƂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p125">C/C++ programmers are most familiar with null-terminated strings. The standard C library is designed to work with such strings. Static string literals in code are compiled into null-terminated strings. Alternatively, Excel works with length-counted strings that are not in general null-terminated. The combination of these facts requires a clear and consistent approach within your DLL/XLL regarding how you handle strings and string memory.</span></span>
  
<span data-ttu-id="48b7f-226">�ł��ʓI�Ȗ���ȉ��Ɏ����܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-226">The most common problems are as follows:</span></span>
  
- <span data-ttu-id="48b7f-227">�L���ȃ|�C���^�[��K�v�Ƃ����̂̃|�C���^�[�̗L�������̂�\`�F�b�N���Ȃ��܂��͂ł��Ȃ��֐��ɁAnull �܂��͖����ȃ|�C���^�[���n�����B</span><span class="sxs-lookup"><span data-stu-id="48b7f-227">The passing of a null or invalid pointer to a function that expects a valid pointer and does not or cannot check the pointer's validity itself.</span></span>
    
- <span data-ttu-id="48b7f-228">�������܂�镶����̒����ɑ΂��ăo�b�t�@�[�̒�����\`�F�b�N���Ȃ��܂��͂ł��Ȃ��֐����A������o�b�t�@�[�̋��E��I�[�o�[��������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-228">The overrunning of the bounds of a string buffer by a function that does not or cannot check the length of the buffer against the length of the string being written.</span></span>
    
- <span data-ttu-id="48b7f-229">�ÓI������o�b�t�@�[ �������A�܂��͊��ɉ�����ꂽ������o�b�t�@�[ �������A���������@�ƈ�т��Ȃ����@�Ŋ��蓖�Ă�ꂽ������o�b�t�@�[ �������������悤�Ƃ��Ă���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-229">Trying to free string buffer memory that is either static, or has been freed already, or was not allocated in a way that is consistent with how it is being freed.</span></span>
    
- <span data-ttu-id="48b7f-230">���蓖�Ă�ꂽ��̂̉�����ꂢ�Ȃ������񂩂琶���郁���� ���[�N�B�ʏ�A�p�ɂɌĂяo�����֐��Ő����܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-230">Memory leaks that result from strings being allocated and then not freed, usually in a frequently called function.</span></span>
    
### <a name="rules-for-strings"></a><span data-ttu-id="48b7f-231">������̋K��</span><span class="sxs-lookup"><span data-stu-id="48b7f-231">Rules for Strings</span></span>

<span data-ttu-id="48b7f-p126">**XLOPER**/ **XLOPER** ��g�p����ꍇ�A�]���ׂ��������̋K���ƃK�C�h���C��������܂��B�K�C�h���C���́A�O�̃Z�N�V�����Ɠ����ł��B������p�ɓ��ʂɊg�����ꂽ�K��������ɋL���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p126">As with **XLOPER**/ **XLOPER**s, there are rules and guidelines you should follow. The guidelines are the same as given in the previous section. The rules here are an extension of the rules specifically for strings.</span></span>
  
 <span data-ttu-id="48b7f-235">**�K��:**</span><span class="sxs-lookup"><span data-stu-id="48b7f-235">**Rules:**</span></span>
  
- <span data-ttu-id="48b7f-p127">XLL �֐��Ɉ����Ƃ��ēn����郁�����������Ȃ��ł��������B�܂��AXLL �֐��Ɉ����Ƃ��ēn����镶���� **XLOPER**/ **XLOPER12** �܂��͒P���Ȓ����J�E���g�����񂠂邢�� null �I���������㏑�����Ȃ��ł��������B�������������͓ǂݎ���p�ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p127">Do not try to free memory or overwrite string **XLOPER**/ **XLOPER12**s or simple length-counted or null-terminated strings passed as arguments to your XLL function. You should treat such arguments as read-only.</span></span>
    
- <span data-ttu-id="48b7f-238">C API �R�[���o�b�N�֐��̖߂�l�̕����� **XLOPER**/ **XLOPER12** �� Excel ������������蓖�Ă�ꍇ�A **xlFree** ��g�p���ĉ�����邩�AXLL �֐����� Excel �ɕԂ��ꍇ�ɂ� **xlbitXLFree** ��ݒ肵�Ă��������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-238">Where Excel allocates memory for a string **XLOPER**/ **XLOPER12** for the return value of a C API callback function, use **xlFree** to free it, or set **xlbitXLFree** if returning it to Excel from an XLL function.</span></span> 
    
- <span data-ttu-id="48b7f-239">DLL �� **XLOPER**/ **XLOPER12** �̕�����o�b�t�@�[�𓮓I�Ɋ��蓖�Ă�ꍇ�A���蓖�Ď��ƈ�т������@�ŉ�����邩�AXLL �֐����� Excel �ɕԂ����ꍇ�ɂ� **xlbitDLLFree** ��ݒ肵�Ă��� **xlAutoFree**/ **xlAutoFree12** �ŉ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-239">Where your DLL dynamically allocates a string buffer for an **XLOPER**/ **XLOPER12**, free it in a way consistent with how you allocated it when done, or set **xlbitDLLFree** if returning it to Excel from an XLL function and then free it in **xlAutoFree**/ **xlAutoFree12**.</span></span>
    
- <span data-ttu-id="48b7f-p128">C API �ւ̌Ăяo���� DLL �ɕԂ���� **xltypeMulti** �z��� Excel ������������蓖�Ă��ꍇ�A�z���̂ǂ̕����� **XLOPER**/ **XLOPER12** ��㏑�����Ȃ��ł��������B���������z��� **xlFree** �ɂ���Ă̂݉�����Ă��������B�܂��� XLL �֐��ɂ���ĕԂ����ꍇ�ɂ́A **xlbitXLFree** ��ݒ肵�ĉ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p128">If Excel has allocated memory for an **xltypeMulti** array returned to your DLL in a call to the C API, do not overwrite any string **XLOPER**/ **XLOPER12**s within the array. Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.</span></span>
    
### <a name="string-types-supported"></a><span data-ttu-id="48b7f-242">�T�|�[�g����镶����^</span><span class="sxs-lookup"><span data-stu-id="48b7f-242">String Types Supported</span></span>

<span data-ttu-id="48b7f-243">**C API xltypeStr XLOPER/XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="48b7f-243">**C API xltypeStr XLOPER/XLOPER12s**</span></span>

|<span data-ttu-id="48b7f-244">**�o�C�g������: **XLOPER****</span><span class="sxs-lookup"><span data-stu-id="48b7f-244">**Byte strings: **XLOPER****</span></span>|<span data-ttu-id="48b7f-245">**���C�h����������: **XLOPER12****</span><span class="sxs-lookup"><span data-stu-id="48b7f-245">**Wide character strings: **XLOPER12****</span></span>|
|:-----|:-----|
|<span data-ttu-id="48b7f-246">���ׂẴo�[�W������ Excel</span><span class="sxs-lookup"><span data-stu-id="48b7f-246">All versions of Excel</span></span>  <br/> |<span data-ttu-id="48b7f-247">Excel 2007 �ȍ~</span><span class="sxs-lookup"><span data-stu-id="48b7f-247">Starting in Excel 2007</span></span>  <br/> |
|<span data-ttu-id="48b7f-248">�ő咷:255 �g�� ASCII �o�C�g</span><span class="sxs-lookup"><span data-stu-id="48b7f-248">Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="48b7f-249">�ő咷: 32,767 Unicode ����</span><span class="sxs-lookup"><span data-stu-id="48b7f-249">Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="48b7f-250">�ŏ��� (�����Ȃ�) �o�C�g = ����</span><span class="sxs-lookup"><span data-stu-id="48b7f-250">First (unsigned) byte = length</span></span>  <br/> |<span data-ttu-id="48b7f-251">�ŏ��� Unicode ���� = ����</span><span class="sxs-lookup"><span data-stu-id="48b7f-251">First Unicode character = length</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="48b7f-252">[!�D�V] **XLOPER** ������܂��� **XLOPER12** ������ null �ŏI������Ƃ͑z�肵�Ȃ��ł��������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-252">Do not assume null termination of **XLOPER** or **XLOPER12** strings.</span></span> 
  
<span data-ttu-id="48b7f-253">**C/C++ ������**</span><span class="sxs-lookup"><span data-stu-id="48b7f-253">**C/C++ strings**</span></span>

|<span data-ttu-id="48b7f-254">**�o�C�g������**</span><span class="sxs-lookup"><span data-stu-id="48b7f-254">**Byte strings**</span></span>|<span data-ttu-id="48b7f-255">**���C�h����������**</span><span class="sxs-lookup"><span data-stu-id="48b7f-255">**Wide character strings**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48b7f-256">Null で終わる (**char** \*)"C"の最大長: 255 に拡張 ASCII バイト</span><span class="sxs-lookup"><span data-stu-id="48b7f-256">Null-terminated (**char** \*) "C" Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="48b7f-257">Null で終わる (**wchar_t** \*) Unicode 文字の最大長の「C %」32,767</span><span class="sxs-lookup"><span data-stu-id="48b7f-257">Null-terminated (**wchar_t** \*) "C%" Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="48b7f-258">長さカウント (**符号なし char** \*)「D」</span><span class="sxs-lookup"><span data-stu-id="48b7f-258">Length-counted (**unsigned char** \*) "D"</span></span>  <br/> |<span data-ttu-id="48b7f-259">長さカウント (**wchar_t** \*)「D %」</span><span class="sxs-lookup"><span data-stu-id="48b7f-259">Length-counted (**wchar_t** \*) "D%"</span></span>  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a><span data-ttu-id="48b7f-260">xltypeMulti XLOPER/XLOPER12 �z���̕�����</span><span class="sxs-lookup"><span data-stu-id="48b7f-260">Strings in xltypeMulti XLOPER/XLOPER12 Arrays</span></span>

<span data-ttu-id="48b7f-p129">�ꍇ�ɂ���ẮAExcel ���ADLL/XLL �Ŏg�p���� **xltypeMulti** �z���쐬���܂��BXLM ���@�\�̒��ɂ́A���������z���Ԃ���̂����܂��B���Ƃ��΁AC API �֐� **xlfGetWorkspace** �́A����  *44*  ���n�����ƁA���ݓo�^����Ă��邷�ׂĂ� DLL �v���V�[�W����L�q���镶�����܂ޔz���Ԃ��܂��BC API �֐� **xlfDialogBox** �́A�z��̈����̕ύX�ς݃R�s�[ (������̏ڍ׃R�s�[��܂݂܂�) ��Ԃ��܂��BXLL �� **xltypeMulti** �z��ɑ�������ł��ʓI�ȏ�ʂ́AXLL �֐��Ɉ����Ƃ��ēn���ꍇ��A�͈͎Q�Ƃ��炱�̌^�ɋ����I�ɂ͂ߍ��ޏꍇ�ł��B��҂̏ꍇ�AExcel �̓\�[�X �Z���̕�����̏ڍ׃R�s�[��쐬���A�z���ł�����|�C���g���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p129">In several cases, Excel creates an **xltypeMulti** array for use in your DLL/XLL. Several of the XLM information functions return such arrays. For example, the C API function **xlfGetWorkspace**, when passed the argument  *44*  , returns an array containing strings that describe all the currently registered DLL procedures. The C API function **xlfDialogBox** returns a modified copy of its array argument, containing deep copies of the strings. Perhaps the most common way an XLL encounters an **xltypeMulti** array is where it has been passed as an argument to an XLL function, or it has been coerced to this type from a range reference. In these latter cases, Excel creates deep copies of the strings in the source cells and points to these within the array.</span></span> 
  
<span data-ttu-id="48b7f-p130">DLL �ł��������������ύX����ꍇ�ɂ́A�Ǝ��̏ڍ׃R�s�[��ݒ肷��K�v�����肊�܂��B�Ǝ��� **xltypeMulti** �z���쐬����ꍇ�ɂ́A�z���� Excel �ɂ���Ċ��蓖�Ă�ꂽ������ **XLOPER**/ **XLOPER12** ��z�u���Ȃ��ł��������B�z�u����ƁA��قǐ���������ł��Ȃ�������A�܂���������ł��Ȃ��Ȃ����肷�鋰�ꂪ����܂��B�����x�A������̏ڍ׃R�s�[��쐬���A�z���ɂ��̃R�s�[�ւ̃|�C���^�[��i�[���Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p130">Where you want to modify these strings in your DLL, you should make your own deep copies. When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12**s within them. This risks you not freeing them correctly later, or not freeing them at all. Again, you should make deep copies of the strings and store pointers to the copies in the array.</span></span>
  
 <span data-ttu-id="48b7f-271">**例**</span><span class="sxs-lookup"><span data-stu-id="48b7f-271">**Examples**</span></span>
  
<span data-ttu-id="48b7f-p131">���̊֐���́A�����J�E���g�� Unicode ������̓��I�Ɋ��蓖�Ă�ꂽ�R�s�[��쐬���܂��B���̗�ł́A�Ăяo�����́A **delete**[] ��g�p���Ċ��蓖�Ă�ꂽ��������ŏI�I�ɉ������K�v�����邱�ƁA����у\�[�X������� null �I���Ƃ͑z�肳��Ă��Ȃ����Ƃɒ��ӂ��Ă��������B�R�s�[������́A���S�̂��߂ɕK�v�ł���ΐ؂�l�߂��Anull �ŏI�����܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p131">The following example function creates a dynamically allocated copy of a length-counted Unicode string. Note that the caller must ultimately free the memory allocated in this example using **delete**[], and that the source string is not assumed to be null terminated. The copy string is truncated if necessary for safety, and is not null terminated.</span></span>
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

<span data-ttu-id="48b7f-275">この関数できますし、安全に使用**XLOPER12**の場合をコピーするのには文字列である場合、引数のコピーを返す次のエクスポート可能な XLL 関数のようにします。</span><span class="sxs-lookup"><span data-stu-id="48b7f-275">This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string.</span></span> <span data-ttu-id="48b7f-276">その他のすべての種類は、長さ 0 の文字列として返されます。</span><span class="sxs-lookup"><span data-stu-id="48b7f-276">All other types are returned as a zero-length string.</span></span> <span data-ttu-id="48b7f-277">範囲が処理されないことに注意してください-を返します **#VALUE!** です。</span><span class="sxs-lookup"><span data-stu-id="48b7f-277">Note that ranges are not handled—the function returns **#VALUE!**.</span></span> <span data-ttu-id="48b7f-278">関数は、参照は値で渡されるように U の型引数を受け取るように登録してください。</span><span class="sxs-lookup"><span data-stu-id="48b7f-278">The function must be registered as taking a type U argument so that references are passed in as values.</span></span> <span data-ttu-id="48b7f-279">これは、機能は、**文字列**が長さ 0 の文字列にもエラーを変換する点を除いて、組み込みのワークシート関数の**上**と同じです。</span><span class="sxs-lookup"><span data-stu-id="48b7f-279">This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings.</span></span> <span data-ttu-id="48b7f-280">このコード例で、その**xlAutoFree12**は、渡されたポインター、および**削除**を使用して、その内容を解放します。</span><span class="sxs-lookup"><span data-stu-id="48b7f-280">This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.</span></span>
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a><span data-ttu-id="48b7f-281">�ύX�C���v���[�X�����������Ԃ�</span><span class="sxs-lookup"><span data-stu-id="48b7f-281">Returning Modify-in-Place String Arguments</span></span>

<span data-ttu-id="48b7f-p133">**F**�A **G**�A **F%** �A **G%** �^�Ƃ��ēo�^���ꂽ�����́A�C���v���[�X�ŕύX�ł��܂��BExcel �͂����̌^�̕�����������������Ƃ��ɁA�ő咷�̃o�b�t�@�[��쐬���܂��B���ɁA�Ώە����񂪂��Ȃ�Z���ꍇ�ł����Ă�A�����������o�b�t�@�[�ɃR�s�[���܂��B���̂��߁AXLL �֐��͓�����������ɖ߂�l�𒼐ڏ������ނ��Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p133">Arguments registered as types **F**, **G**, **F%**, and **G%** can be modified in place. When Excel is preparing string arguments for these types, it creates a maximum length buffer. Then it copies the argument string into that, even if this string is very much shorter. This enables the XLL function to write its return value directly into the same memory.</span></span> 
  
<span data-ttu-id="48b7f-286">���������^�̂��߂Ɏ�蕪������o�b�t�@�[ �T�C�Y�͎��̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-286">Buffer sizes set apart for these types are as follows:</span></span>
  
- <span data-ttu-id="48b7f-287">**�o�C�g������:** 256 �o�C�g (�����J�E���^�[ (G �^) �܂��� null �I�[ (F �^) ��܂݂܂�)�B</span><span class="sxs-lookup"><span data-stu-id="48b7f-287">**Byte strings:** 256 bytes including the length counter (type G) or null-termination (type F).</span></span> 
    
- <span data-ttu-id="48b7f-288">**Unicode ������:** 32,768 ���C�h���� (65,536 �o�C�g)(�����J�E���^�[ (G% �^) �܂��� null �I�[ (F% �^) ��܂݂܂�)�B</span><span class="sxs-lookup"><span data-stu-id="48b7f-288">**Unicode strings:** 32,768 wide characters (65,536 bytes) including the length counter (type G%) or null-termination (type F%).</span></span> 
    
> [!NOTE]
> <span data-ttu-id="48b7f-p134">[!����] Visual Basic for Applications (VBA) ���炱�������֐��𒼐ڌĂяo�����Ƃ͂ł��܂���B�\���ȑ傫���̃o�b�t�@�[�����蓖�Ă��Ă��邱�Ƃ�m�F�ł��Ȃ����߂ł��B���������֐��́A�\���ȑ傫���̃o�b�t�@�[�𖾎��I�ɓn���ʂ� DLL ����݈̂��S�ɌĂяo�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p134">You cannot call such a function directly from Visual Basic for Applications (VBA) because you cannot ensure that a sufficiently large buffer has been allocated. You can only call such a function from another DLL safely if you have explicitly passed a big enough buffer.</span></span> 
  
<span data-ttu-id="48b7f-p135">�W�����C�u�����֐� **wcsrev** ��g�p���āA�n���ꂽ null �I���̃��C�h�����𔽓]������ XLL �֐��̗����Ɏ����܂��B���̏ꍇ�̈����́A�^ **F%** �Ƃ��ēo�^����܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p135">Here is an example of an XLL function that reverses a passed-in null-terminated wide character string using the standard library function **wcsrev**. The argument in this case would be registered as type **F%**.</span></span>
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a><span data-ttu-id="48b7f-293">�i���L�� (�o�C�i����)</span><span class="sxs-lookup"><span data-stu-id="48b7f-293">Persistent Storage (Binary Names)</span></span>

<span data-ttu-id="48b7f-294">バイナリの名前を定義して、ブックと共に保存されている非構造化データは、バイナリのブロックに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="48b7f-294">Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook.</span></span> <span data-ttu-id="48b7f-295">関数[xlDefineBinaryName](xldefinebinaryname.md)を使用して作成されると、関数[xlGetBinaryName](xlgetbinaryname.md)を使用してデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="48b7f-295">They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md).</span></span> <span data-ttu-id="48b7f-296">どちらの関数が関数のリファレンスで詳しく説明されている (を参照してください[C API 関数をことができますされると呼ばれるだけ DLL や XLL から](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md))、 **xltypeBigData** **XLOPER**の両方を使用して/ **XLOPER12**。</span><span class="sxs-lookup"><span data-stu-id="48b7f-296">Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> 
  
<span data-ttu-id="48b7f-297">�o�C�i�����̎��ۂ̓K�p�𐧌�������m�̖��ɂ��ẮA�u[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B</span><span class="sxs-lookup"><span data-stu-id="48b7f-297">For information about known issues that limit the practical applications of binary names, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="excel-stack"></a><span data-ttu-id="48b7f-298">Excel �̃X�^�b�N</span><span class="sxs-lookup"><span data-stu-id="48b7f-298">Excel Stack</span></span>

<span data-ttu-id="48b7f-p137">Excel �́A�ǂݍ��񂾂��ׂĂ� DLL �ƃX�^�b�N�̈����L���܂��B�ʏ�A�X�^�b�N�̈�͕��i�̎g�p�ʂ�������A���Ɏ��グ�邢�����̃K�C�h���C���ɏ]������͖��ƂȂ邱�Ƃ͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p137">Excel shares its stack space with all the DLLs it has loaded. Stack space is usually more than adequate for ordinary use, and you do not need to be concerned about it as long as you follow a few guidelines:</span></span> 
  
- <span data-ttu-id="48b7f-p138">�X�^�b�N��ŁA�֐��ɑ΂�������Ƃ��ĂƂĂ�傫�ȍ\���̂�l�Ƃ��ēn���Ȃ��ł��������B����ɁA�|�C���^�[��Q�Ƃ�n���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p138">Do not pass very large structures as arguments to functions by value on the stack. Pass pointers or references instead.</span></span>
    
- <span data-ttu-id="48b7f-p139">�X�^�b�N�ɑ傫�ȍ\���̂�Ԃ��Ȃ��ł��������B�ÓI�܂��͓��I�Ɋ��蓖�Ă�ꂽ�������ւ̃|�C���^�[��Ԃ����A�Q�Ƃɂ���ēn����������g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p139">Do not return large structures on the stack. Return pointers to static or dynamically allocated memory, or use arguments passed by reference.</span></span>
    
- <span data-ttu-id="48b7f-p140">�֐��R�[�h�ŁA���ɑ�K�͂Ȏ����ϐ��\���̂�錾���Ȃ��ł��������B�K�v�ȏꍇ�́A�X�^�e�B�b�N (Static) �Ƃ��Đ錾���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p140">Do not declare very large automatic variable structures in the function code. If you need them, declare them as static.</span></span>
    
- <span data-ttu-id="48b7f-p141">�ċA�̐[�����󂢂ƕ������Ă���ȊO�́A�֐���ċA�I�ɌĂяo���Ȃ��ł��������B����ɁA���[�v��g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p141">Do not call functions recursively unless you are sure the depth of recursion will always be shallow. Try using a loop instead.</span></span>
    
<span data-ttu-id="48b7f-p142">C API ��g�p���� DLL �� Excel �ɃR�[���o�b�N����Ƃ��́AExcel �͍ŏ��ɁA�ň��̎g�p�P�[�X�ɔ����ăX�^�b�N��ɏ\���ȗ̈悪�m�ۂ���Ă��邩�ǂ�����\`�F�b�N���܂��B�\���ȗ̈悪�Ȃ��Ɣ��f����ƁA���S�ȌĂяo���Ɏ��s���܂��B����̌Ăяo���ŁA���ۂɂ͏\���ȗ̈悪����ꍇ�ł���s���܂��B���̏ꍇ�ɂ́A�R�[���o�b�N�̓R�[�h **xlretFailed** ��Ԃ��܂��BC API �ƃX�^�b�N�̒ʏ�̎g�p�ł́A���ꂪ C API �Ăяo���̎��s�̌����ƂȂ邱�Ƃ͂قƂ�ǂ���܂���B</span><span class="sxs-lookup"><span data-stu-id="48b7f-p142">When a DLL calls back into Excel using the C API, Excel first checks whether there is enough space on the stack for the worst-case usage call that could be made. If it thinks there might be insufficient room, it will fail the call to be safe, even though there might actually have been enough space for that particular call. In this case, the callbacks return the code **xlretFailed**. For ordinary use of the C API and the stack, this is an unlikely cause of the failure of a C API call.</span></span>
  
<span data-ttu-id="48b7f-313">���̃G���[����������ꍇ�A�܂��͌��O����ꍇ�A���邢�͌����s���̃G���[���������Ƃ��ẴX�^�b�N�̈�̕s����������ꍇ�A[xlStack](xlstack.md) �֐��ւ̌Ăяo���ŃX�^�b�N�̈悪�ǂ�قǂ��邩�𒲂ׂ邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="48b7f-313">If you are concerned, or just curious, or you want to eliminate lack of stack space as a reason for an unexplained failure, you can find out how much stack space there is with a call to the [xlStack](xlstack.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48b7f-314">�֘A����</span><span class="sxs-lookup"><span data-stu-id="48b7f-314">See also</span></span>



[<span data-ttu-id="48b7f-315">Excel �ł̃}���\`�X���b�h�Čv�Z</span><span class="sxs-lookup"><span data-stu-id="48b7f-315">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="48b7f-316">Excel 2007 �ɂ�����}���\`�X���b�h�����ƃ���������</span><span class="sxs-lookup"><span data-stu-id="48b7f-316">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
  
[<span data-ttu-id="48b7f-317">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="48b7f-317">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

