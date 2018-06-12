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
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
XLL ���[�N�V�[�g�֐��� **XLOPER**/ **XLOPER12** ��Ԃ�������ɁAXLL �ŉ������K�v�̂��郁�������܂����邱�Ƃ�����t���O��ݒ肷�邽�߂� Excel �ɂ���ČĂяo����܂��B����ɂ��A���I�Ɋ��蓖�Ă�ꂽ�z��A�����񂨂�ъO���Q�Ƃ������ ���[�N�Ȃ��� XLL �Ń��[�N�V�[�g�ɕԂ���悤�ɂȂ�܂��B�ڍׂɂ��ẮA�u [Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B
  
**xlAutoFree12** �֐��� **XLOPER12** �f�[�^�^�́AExcel 2007 �ȍ~�ŃT�|�[�g����Ă��܂��B 
  
Excel �ł́AXLL ������炢���ꂩ�̊֐���������ăG�N�X�|�[�g���邱�Ƃ͕s�v�ł��B�������A���I�Ƀ����������蓖�Ă��Ă���A�܂��͓��I�Ɋ��蓖�Ă�ꂽ�������ւ̃|�C���^��܂�ł��� XLOPER �܂��� XLOPER12 �� XLL �֐����Ԃ��ꍇ�́A���̕K�v������܂��B�����̃f�[�^�^�ɑI����郁�����Ǘ��̕��@�́AXLL �S�̂ł̈�ѐ���m�ۂ��A **xlAutoFree** ����� **xlAutoFree12** �̎������@�Ɩ������Ȃ��悤�ɂ��܂��B
  
**xlAutoFree**/ **xlAutoFree12** �֐��̓���ł́AExcel �ւ̃R�[���o�b�N�͖���������Ă��܂��B����ɂ� 1 �̗�O������AExcel �ɂ���Ċ��蓖�Ă�ꂽ�������������邽�߂� **xlFree** �̌Ăяo���͉\�ł��B 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxFree_(**XlAutoFree の場合 LPXLOPER**)
  
 _pxFree_(**XlAutoFree12 の場合 LPXLOPER12**)
  
�������K�v�̂��郁���������蓖�Ă��Ă��� **XLOPER** �܂��� **XLOPER12** �ւ̃|�C���^�[�B 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

���̊֐��͒l��Ԃ��܂���Bvoid ��Ԃ��悤�ɐ錾����Ă���K�v������܂��B
  
## <a name="remarks"></a>����

Excel ���}���`�X���b�h�̃u�b�N�̍Čv�Z��g�p����悤�ɍ\������Ă���ꍇ�A **xlAutoFree**/ **xlAutoFree12** �́A�����Ԃ����֐��̌Ăяo���Ɏg�p���ꂽ�X���b�h�Ɠ����X���b�h�ŌĂяo����܂��B **xlAutoFree**/ **xlAutoFree12** �̌Ăяo���́A��ɁA���̃X���b�h�Ō㑱�̃��[�N�V�[�g�̃Z�����]�������O�ɍs���܂��B����ɂ��AXLL �ł̃X���b�h �Z�[�t�Ȑ݌v���ȒP�ɂȂ�܂��B 
  
�J�X�^���� **xlAutoFree**/ **xlAutoFree12** �֐���  **pxFree** �� _xltype_ �t�B�[���h�𒲂ׂ�ꍇ�́A **xlbitDLLFree** �r�b�g���ݒ肳�ꂽ�܂܂ɂȂ��Ă���_�ɒ��ӂ��Ă��������B 
  
## <a name="example"></a>��

 **������ 1**
  
`\SAMPLES\EXAMPLE\EXAMPLE.C` �̍ŏ��̃R�[�h�ł́A���ɓ���� **xlAutoFree** �̎����������Ă��܂��B����� 1 �̊֐� **fArray** �����Ɏg�p����悤�ɐ݌v����Ă��܂��B��ʂɁAXLL �ɂ͉������K�v�̂��郁������Ԃ��֐�����������܂��B���̏ꍇ�́A���܂����I�łȂ��������K�v�ɂȂ�܂��B 
  
 **������ 2**
  
2 �Ԗڂ̎�����́A�Z�N�V���� 1.6.3�Axl12_Str_example�Axl12_Ref_example�A����� xl12_Multi_example �� **XLOPER12** �̍쐬��Ŏg�p�����O�����ɓK�����܂��B���̑O�����Ƃ́u **xlbitDLLFree** �r�b�g���ݒ肳��Ă���Ƃ��ɂ́A���ׂĂ̕�����A�z��A����ъO���Q�ƃ������� **malloc** ��g�p���ē��I�Ɋ��蓖�Ă��Ă��āAfree �̌Ăяo���ŉ������K�v������v�Ƃ������Ƃł��B
  
 **������ 3**
  
3 �Ԗڂ̎�����́A **malloc** ��g�p���� **XLOPER12** �����蓖�Ă�������A�O���Q�Ƃ���єz���Ԃ��֐���G�N�X�|�[�g���� XLL�A�܂��� **XLOPER12** ���̂���I�Ɋ��蓖�Ă�ꂽ XLL �ɓK�����܂��B���I�Ɋ��蓖�Ă�ꂽ **XLOPER12** �ւ̃|�C���^�[��������ɕԂ���邱�ƂŁA�֐����X���b�h �Z�[�t�ł��邱�Ƃ�ۏ؂��܂��B 
  
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

## <a name="see-also"></a>�֘A����



[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)

