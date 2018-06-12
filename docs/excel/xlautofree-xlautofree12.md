---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- xlautofree function [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: a2d2b8e60b484ba8156acc80d543493e3ec9c564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798967"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="4cbe8-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="4cbe8-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="4cbe8-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4cbe8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4cbe8-p101">XLL ���[�N�V�[�g�֐��� **XLOPER**/ **XLOPER12** ��Ԃ�������ɁAXLL �ŉ������K�v�̂��郁�������܂����邱�Ƃ�����t���O��ݒ肷�邽�߂� Excel �ɂ���ČĂяo����܂��B����ɂ��A���I�Ɋ��蓖�Ă�ꂽ�z��A�����񂨂�ъO���Q�Ƃ������ ���[�N�Ȃ��� XLL �Ń��[�N�V�[�g�ɕԂ���悤�ɂȂ�܂��B�ڍׂɂ��ẮA�u [Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-p101">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release. This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="4cbe8-109">**xlAutoFree12** �֐��� **XLOPER12** �f�[�^�^�́AExcel 2007 �ȍ~�ŃT�|�[�g����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="4cbe8-p102">Excel �ł́AXLL ������炢���ꂩ�̊֐���������ăG�N�X�|�[�g���邱�Ƃ͕s�v�ł��B�������A���I�Ƀ����������蓖�Ă��Ă���A�܂��͓��I�Ɋ��蓖�Ă�ꂽ�������ւ̃|�C���^��܂�ł��� XLOPER �܂��� XLOPER12 �� XLL �֐����Ԃ��ꍇ�́A���̕K�v������܂��B�����̃f�[�^�^�ɑI����郁�����Ǘ��̕��@�́AXLL �S�̂ł̈�ѐ���m�ۂ��A **xlAutoFree** ����� **xlAutoFree12** �̎������@�Ɩ������Ȃ��悤�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-p102">Excel does not require an XLL to implement and export either of these functions. However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory. Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="4cbe8-113">**xlAutoFree**/ **xlAutoFree12** �֐��̓���ł́AExcel �ւ̃R�[���o�b�N�͖���������Ă��܂��B����ɂ� 1 �̗�O������AExcel �ɂ���Ċ��蓖�Ă�ꂽ�������������邽�߂� **xlFree** �̌Ăяo���͉\�ł��B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="4cbe8-114">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="4cbe8-114">Parameters</span></span>

 <span data-ttu-id="4cbe8-115">_pxFree_(**XlAutoFree の場合 LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="4cbe8-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="4cbe8-116">_pxFree_(**XlAutoFree12 の場合 LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="4cbe8-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="4cbe8-117">�������K�v�̂��郁���������蓖�Ă��Ă��� **XLOPER** �܂��� **XLOPER12** �ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4cbe8-118">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="4cbe8-118">Property value/Return value</span></span>

<span data-ttu-id="4cbe8-119">���̊֐��͒l��Ԃ��܂���Bvoid ��Ԃ��悤�ɐ錾����Ă���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4cbe8-120">����</span><span class="sxs-lookup"><span data-stu-id="4cbe8-120">Remarks</span></span>

<span data-ttu-id="4cbe8-p103">Excel ���}���\`�X���b�h�̃u�b�N�̍Čv�Z��g�p����悤�ɍ\������Ă���ꍇ�A **xlAutoFree**/ **xlAutoFree12** �́A�����Ԃ����֐��̌Ăяo���Ɏg�p���ꂽ�X���b�h�Ɠ����X���b�h�ŌĂяo����܂��B **xlAutoFree**/ **xlAutoFree12** �̌Ăяo���́A��ɁA���̃X���b�h�Ō㑱�̃��[�N�V�[�g�̃Z�����]�������O�ɍs���܂��B����ɂ��AXLL �ł̃X���b�h �Z�[�t�Ȑ݌v���ȒP�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-p103">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it. The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread. This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="4cbe8-124">�J�X�^���� **xlAutoFree**/ **xlAutoFree12** �֐���  **pxFree** �� _xltype_ �t�B�[���h�𒲂ׂ�ꍇ�́A **xlbitDLLFree** �r�b�g���ݒ肳�ꂽ�܂܂ɂȂ��Ă���_�ɒ��ӂ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4cbe8-125">��</span><span class="sxs-lookup"><span data-stu-id="4cbe8-125">Example</span></span>

 <span data-ttu-id="4cbe8-126">**������ 1**</span><span class="sxs-lookup"><span data-stu-id="4cbe8-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="4cbe8-p104">`\SAMPLES\EXAMPLE\EXAMPLE.C` �̍ŏ��̃R�[�h�ł́A���ɓ���� **xlAutoFree** �̎����������Ă��܂��B����� 1 �̊֐� **fArray** �����Ɏg�p����悤�ɐ݌v����Ă��܂��B��ʂɁAXLL �ɂ͉������K�v�̂��郁������Ԃ��֐�����������܂��B���̏ꍇ�́A���܂����I�łȂ��������K�v�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-p104">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**. In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="4cbe8-129">**������ 2**</span><span class="sxs-lookup"><span data-stu-id="4cbe8-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="4cbe8-p105">2 �Ԗڂ̎�����́A�Z�N�V���� 1.6.3�Axl12_Str_example�Axl12_Ref_example�A����� xl12_Multi_example �� **XLOPER12** �̍쐬��Ŏg�p�����O�����ɓK�����܂��B���̑O�����Ƃ́u **xlbitDLLFree** �r�b�g���ݒ肳��Ă���Ƃ��ɂ́A���ׂĂ̕�����A�z��A����ъO���Q�ƃ������� **malloc** ��g�p���ē��I�Ɋ��蓖�Ă��Ă��āAfree �̌Ăяo���ŉ������K�v������v�Ƃ������Ƃł��B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-p105">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example. The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="4cbe8-132">**������ 3**</span><span class="sxs-lookup"><span data-stu-id="4cbe8-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="4cbe8-p106">3 �Ԗڂ̎�����́A **malloc** ��g�p���� **XLOPER12** �����蓖�Ă�������A�O���Q�Ƃ���єz���Ԃ��֐���G�N�X�|�[�g���� XLL�A�܂��� **XLOPER12** ���̂���I�Ɋ��蓖�Ă�ꂽ XLL �ɓK�����܂��B���I�Ɋ��蓖�Ă�ꂽ **XLOPER12** �ւ̃|�C���^�[��������ɕԂ���邱�ƂŁA�֐����X���b�h �Z�[�t�ł��邱�Ƃ�ۏ؂��܂��B</span><span class="sxs-lookup"><span data-stu-id="4cbe8-p106">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12**s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated. Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
```cs
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 1
//////////////////////////////////////////
LPXLOPER12 WINAPI fArray(void)
{
    LPXLOPER12 pxArray;
    static XLOPER12 xMulti;
    int i;
    int rwcol;
    xMulti.xltype = xltypeMulti | xlbitDLLFree;
    xMulti.val.array.columns = 1;
    xMulti.val.array.rows = 8;
    // For large values of rows and columns, this would overflow
    // use __int64 in that case and return an error if rwcol
    // contains a number that won't fit in sizeof(int) bytes
    rwcol = xMulti.val.array.columns * xMulti.val.array.rows; 
    pxArray = (LPXLOPER12)GlobalLock(hArray = GlobalAlloc(GMEM_ZEROINIT, rwcol * sizeof(XLOPER12)));
    xMulti.val.array.lparray = pxArray;
    for(i = 0; i < rwcol; i++) 
    {
        pxArray[i].xltype = xltypeInt;
        pxArray[i].val.w = i;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe, use alternate memory allocation mechanisms
    return (LPXLOPER12)&xMulti;
}
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    GlobalUnlock(hArray);
    GlobalFree(hArray);
    return;
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 2
//////////////////////////////////////////
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
/* Assume all string elements were allocated using malloc, and
** need to be freed using free.  Then free the array itself.
*/
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 3
//////////////////////////////////////////
LPXLOPER12 WINAPI example_xll_function(LPXLOPER12 pxArg)
{
// Thread-safe return value. Every invocation of this function
// gets its own piece of memory.
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
// Initialize to a safe default
    pxRtnValue->xltype = xltypeNil;
// Set the value of pxRtnValue making sure that strings, external
// references, arrays, and strings within arrays are all dynamically
// allocated using malloc.
//    (code omitted)
//    ...
// Set xlbitDLLFree regardless of the type of the return value to
// ensure xlAutoFree12 is called and pxRtnValue is freed.
    pxRtnValue->xltype |= xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
// Assume all string elements were allocated using malloc, and
// need to be freed using free. Then free the array itself.
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
// Assume pxFree was itself dynamically allocated using malloc.
    free(pxFree);
}
```

## <a name="see-also"></a><span data-ttu-id="4cbe8-135">�֘A����</span><span class="sxs-lookup"><span data-stu-id="4cbe8-135">See also</span></span>



<span data-ttu-id="4cbe8-136">[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)</span><span class="sxs-lookup"><span data-stu-id="4cbe8-136">[Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)</span></span>

