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
# <a name="memory-management-in-excel"></a>Excel �̃������Ǘ�

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�����I�ň��肵�� XLL ��쐬����ꍇ�ɂ́A�������Ǘ����ł�d�v�ȉۑ�ƂȂ�܂��B��������Ǘ��ł��Ȃ��� Microsoft Excel �ŗl�X�Ȗ�肪������\��������܂��B���Ƃ��΁A���������蓖�Ă⏉�����̌����������Ȃ�����A���K�͂ȃ����� ���[�N���������肷��Ƃ�������r�I�����Ȗ�肩��AExcel ���s����ɂȂ�Ƃ������傫�Ȗ��Ȃǂ��N���錴���ƂȂ�܂��B
  
�A�h�C���֘A�̐[���Ȗ��̍ł��ʓI�Ȍ������A�������Ǘ��̎��s�ɂ���܂��B���������āA�v���W�F�N�g��r���h����ہA��ѐ�������A�\���ɍl�������������Ǘ��̐헪��g�p����K�v������܂��B 
  
Microsoft Office Excel 2007 �ł̓}���`�X���b�h�̃u�b�N�Čv�Z�̓����ɔ����A�������Ǘ�������܂ňȏ�ɕ��G�ɂȂ�܂����B�X���b�h �Z�[�t�ȃ��[�N�V�[�g�֐���쐬���ăG�N�X�|�[�g����ꍇ�́A�����̃X���b�h���A�N�Z�X�Ɋւ��ċ�������Ƃ��ɐ�����\�������鋣����Ԃ�Ǘ����Ȃ���΂Ȃ�܂���B
  
���� 3 �̃f�[�^�\���̌^�Ɋւ��郁�����̍l������������܂��B
  
- **XLOPER** �� **XLOPER12**
    
- **XLOPER** �ł� **XLOPER12** �ł�Ȃ�������
    
- **FP** �z��� **FP12** �z�� 
    
## <a name="xloperxloper12-memory"></a>XLOPER/XLOPER12 ������

**XLOPER**/ **XLOPER12**のデータ構造体には、つまり文字列 (**xltypeStr**)、配列 (**xltypeMulti**) および外部参照 (**xltypeRef**) のメモリ ブロックへのポインターが含まれているいくつかのサブタイプです。 **XLOPER**の文字列を**xltypeMulti**配列に含められることにも注意してください/ **XLOPER12s**に他のメモリ ブロックを指す。 
  
**XLOPER**/ **XLOPER12** �́A���̂悤�ɂ������̕��@�ō쐬����܂��B 
  
- Excel �ɂ���āBXLL �֐��ɓn�����������������Ƃ�
    
- Excel �ɂ���āBC API �Ăяo���� **XLOPER** �܂��� **XLOPER12** ���Ԃ����Ƃ� 
    
- DLL �ɂ���āBC API �Ăяo���ɓn����������쐬����Ƃ�
    
- DLL �ɂ���āBXLL �֐��̖߂�l��쐬����Ƃ�
    
�����ꂩ�̃����� �|�C���g�^�̃����� �u���b�N�́A���̂������̕��@�Ŋ��蓖�Ă邱�Ƃ��ł��܂��B
  
- �֐��R�[�h�O�� DLL �ŐÓI�u���b�N�Ƃ��邱�Ƃ��ł��܂��B���̏ꍇ�A����������蓖�Ă����������肷��K�v�͂���܂���B
    
- �֐��R�[�h��� DLL �ŐÓI�u���b�N�Ƃ��邱�Ƃ��ł��܂��B���̏ꍇ�A����������蓖�Ă����������肷��K�v�͂���܂���B
    
- DLL �œ��I�Ɋ��蓖�Ă�����������ł��܂��B���̂��߂ɂ́A **malloc** �� **free**�A **new** �� **delete** �Ȃǂ̕��@������܂��B
    
- Excel �œ��I�Ɋ��蓖�Ă邱�Ƃ��ł��܂��B
    
���X���݂���\�������� **XLOPER**/ **XLOPER12** �������̐��� **XLOPER**/ **XLOPER12** �Ƀ����������蓖�Ă�ꂽ�󋵂̑��l���ɂ��čl������ƁA�ƂĂ������Ɏv���Ă����������܂���B�������A���ɋL���������̋K���ƃK�C�h���C���ɏ]���ƁA���G����啝�ɍ팸�ł��܂��B 
  
### <a name="rules-for-working-with-xloperxloper12"></a>XLOPER/XLOPER12 ������Ƃ��̋K��

- ����������������AXLL �֐��Ɉ����Ƃ��ēn����� **XLOPERs**/ **XLOPER12** ��㏑�����Ȃ��ł��������B�������������͓ǂݎ���p�ɂ���K�v������܂��B�ڂ����́A�u **Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��**�v�́u�C�� �v���[�X�̈�����ύX���� **XLOPER** �܂��� [XLOPER12](known-issues-in-excel-xll-development.md) ��Ԃ��v��������������B
    
- C API �ւ̌Ăяo���ŁADLL �ɕԂ���� **XLOPER**/ **XLOPER12** �� Excel ������������蓖�Ă��ꍇ: 
    
  - **XLOPER**/ **XLOPER12** ���s�v�ɂȂ�ꍇ�A [xlFree](xlfree.md) ��Ăяo���ă������������Ȃ���΂Ȃ�܂���B���̑��̕��@ (free�Adelete �Ȃ�) ��g�p���ă������������Ȃ��ł��������B
    
  - �Ԃ����^�� **xltypeMulti** �̂Ƃ��A�z���� **XLOPER**/ **XLOPER12** ��㏑�����Ȃ��ł��������B���ɁA�����񂪊܂܂�Ă���ꍇ�A����ѕ�����ŏ㏑�����悤�Ƃ��Ă���̂ł͂Ȃ��ꍇ�ɒ��ӂ��Ă��������B
    
  - DLL �֐��̖߂�l�Ƃ��� **XLOPER**/ **XLOPER12** �� Excel �ɕԂ��ꍇ�AExcel �ɑ΂��āA�s�v�ɂȂ�����������K�v�����郁���������݂��邱�Ƃ�ʒm���Ȃ���΂Ȃ�܂���B 
    
- C API �Ăяo���ɑ΂���߂�l�Ƃ��č쐬���ꂽ **XLOPER******/  �ł� **xlFree** �݂̂�Ăяo���܂��B 
    
- DLL �֐��̖߂�l�Ƃ��� Excel �ɕԂ� **XLOPER**/ **XLOPER12** �� DLL ������������蓖�Ă��ꍇ�ɂ́ADLL ���������K�v�����郁���������݂��邱�Ƃ� Excel �ɒʒm���Ȃ���΂Ȃ�܂���B 
    
### <a name="guidelines-for-memory-management"></a>�������Ǘ��̃K�C�h���C��

- ����������蓖�Ăĉ�����邽�߂Ɏg�p���郁�\�b�h�� DLL ��ň�т����܂��B�قȂ郁�\�b�h�����݂��Ȃ��悤�ɂ��܂��B������ �N���X�܂��͍\���̂Ŏg�p���郁�\�b�h����b�v���A�Ώۃ��\�b�h���g�p����Ă��鑽���̏ꏊ�ŃR�[�h��ς��Ȃ��Ă�ύX�ł���悤�ɂ��邱�Ƃ�����߂��܂��B
    
- DLL �� **xltypeMulti** �z���쐬����ꍇ�A������Ƀ���������蓖�Ă���@���т����Ă��������B�K���������𓮓I�Ɋ��蓖�Ă邩�A�K���ÓI��������g�p���邩�̂ǂ��炩�ɂ��Ă��������B�������Ă����΁A��������������Ƃ��ɁA�������K��������邩�A������Ă͂Ȃ�Ȃ�����������܂��B 
    
- Excel ���쐬���� **XLOPER**/ **XLOPER12** ��R�s�[����Ƃ��́AExcel �����蓖�Ă���������ڍ׃R�s�[���܂��B
    
- Excel �����蓖�Ă������� **XLOPER**/ **XLOPER12** �� **xltypeMulti** �z���ɔz�u���Ȃ��ł��������B������̏ڍ׃R�s�[��쐬���A���̃R�s�[�ւ̃|�C���^�[��z���Ɋi�[���܂��B 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Excel �����蓖�Ă� XLOPER/XLOPER12 ��������������

���� XLL �R�}���h�ɂ��čl�����܂��B���̃R�}���h�́A **xlGetName** ��g�p���āADLL �̃p�X�ƃt�@�C������܂ޕ������擾���A **xlcAlert** ��g�p���Čx���_�C�A���O �{�b�N�X�ɕ\�����܂��B
  
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

���̊֐��� **xDllName** �ɂ���ă|�C���g����Ă��郁������K�v�Ƃ��Ȃ��Ȃ����Ȃ�ADLL ��p C API �֐��� 1 �ł��� [xlFree �֐�](xlfree.md)�ւ̌Ăяo����g�p���ĉ���ł��܂��B 
  
**xlFree** �֐��ɂ��Ă͊֐����t�@�����X �Z�N�V���� (�u [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)�v�������������) �ɏڍׂ��L����Ă��܂����A�ȉ��̓_�ɒ��ӂ��Ă��������B
  
- **xlFree** �ւ� 1 ��̌Ăяo���ŕ����� / ******XLOPER12** �ւ̃|�C���^�[��n�����Ƃ��ł��܂��B�������A���s����Ă��� Excel �o�[�W�����ŃT�|�[�g����Ă��鐔�̊֐������Ɍ��肳��܂� (Excel 2003 �̏ꍇ�ɂ� 30�AExcel 2007 �ȍ~�ł� 255)�B
    
- **xlFree** �͊܂܂�Ă���|�C���^�[�� **NULL** �ɐݒ肵�A���ɉ�����ꂽ **XLOPER**/ **XLOPER12** �������悤�Ƃ��Ă���S�ȏ�Ԃ�m�ۂ��܂��B **xlFree** �́A������ύX����B��� C API �֐��ł��B 
    
- �������ւ̃|�C���^�[���܂܂�邩�ǂ����Ɋ֌W�Ȃ��AC API �ւ̌Ăяo���̖߂�l�Ɏg�p�����C�ӂ� **XLOPER******/  �� **xlFree** ����S�ɌĂяo���܂��B 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Excel �ŉ������� XLOPER/XLOPER12 ��Ԃ�

�O�̃Z�N�V�����ɋL����Ă���R�}���h���A **Boolean** **true** �������n�����Ƃ��ɂ� DLL �p�X�ƃt�@�C������Ԃ��A����ȊO�̏ꍇ�ɂ� **#N/A** ��Ԃ����[�N�V�[�g�֐��ɕύX����ꍇ�ɂ��čl���܂��BExcel �ɕԂ����O�� **xlFree** ��Ăяo���ĕ����񃁃��������ł��Ȃ����Ƃ͖����ł��B�������A�����ꂩ�̎��_�ŉ������Ȃ��ƁA�A�h�C���͊֐����Ăяo����邽�тɃ����� ���[�N��N�����܂��B���̖�������邽�߁Axlcall.h �� **xlbitXLFree** �Ƃ��Ē�`����Ă���A **XLOPER**/ **XLOPER12** �� **xltype** �t�B�[���h�Ƀr�b�g��ݒ�ł��܂��B�����ݒ肷�邱�Ƃɂ���āA�l�̃R�s�[���I�������Ƃ��ɁA�Ԃ��ꂽ��������������K�v�����邱�Ƃ� Excel �ɒʒm���܂��B 
  
### <a name="example"></a>��

���̃R�[�h��́AXLL ���[�N�V�[�g�֐��ɕϊ����ꂽ�A�O�̃Z�N�V������ XLL �R�}���h������Ă��܂��B
  
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

**XLOPER**/ **XLOPER12** ��g�p���� XLL �֐��́A **XLOPER**/ **XLOPER12** �ւ̃|�C���^�[��擾���߂���̂Ƃ��Ē�`����K�v������܂��B���̊֐���Ŏg�p����Ă���T���v���̐ÓI **XLOPER12** �̓X���b�h �Z�[�t�ł͂���܂���B�s�K�؂ɂ���̊֐���X���b�h �Z�[�t�Ƃ��ēo�^���邱�Ƃ͂ł��܂����A����X���b�h�� **xRtnValue** �̏�����I������O�ɕʂ̃X���b�h���㏑�����Ă��܂��Ƃ����댯�������܂��B 
  
**xlbitXLFree** �̐ݒ�́A���蓖�Ă�s�� Excel �R�[���o�b�N�ւ̌Ăяo����ɍs���K�v������܂��B�ݒ���ɍs���ƁA�㏑������āA�K�v�ȓ��삪�����܂���B�ʂ� C API �֐��ւ̌Ăяo���Œl������Ƃ��Ďg�p���Ă��烏�[�N�V�[�g�ɖ߂��ꍇ�ɂ́A���̂悤�ȌĂяo����ɂ��̃r�b�g��ݒ肵�Ă��������B���̂悤�ɂ��Ȃ��ƁA **XLOPER**/ **XLLOPER12** �^�̃`�F�b�N����܂ŁA���̃r�b�g��}�X�N���Ȃ��֐����������Ă��܂��܂��B 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>DLL �ŉ������� XLOPER/XLOPER12 ��Ԃ�

���l�̖�肪�A **XLOPER**/ **XLOPER12** �̃������� XLL �����蓖�ĂāAExcel �ɖ߂��ꍇ�ɐ����܂��BExcel �́Axlcall.h �� **xlbitDLLFree** �Ƃ��Ē�`����Ă���A **XLOPER**/ **XLOPER12** �� **xltype** �t�B�[���h�ɐݒ�\�ȕʂ̃r�b�g��F�����܂��B 
  
Excel が **、XLOPER**を受け取ると/ この**XLOPER12**ビットが設定、( **XLOPER**s) の[xlAutoFree](xlautofree-xlautofree12.md)または**XLOPER12**秒) ( **xlAutoFree12**と呼ばれる xll ファイルをエクスポートするようにする関数を呼び出すしようとします。 この関数は、関数リファレンスで詳しく説明が ([マネージャー、XLL インターフェイスの関数](add-in-manager-and-xll-interface-functions.md)を参照)、ですが、最低限の実装例をここで指定します。 **XLOPER**を解放するための目的は、/ 最初割り当てられた方法に一貫性のある方法でメモリを**XLOPER12** 。 
  
### <a name="examples"></a>��

���̊֐���́A�O�q�̊֐��Ɠ����ł��B��O�́ADLL ���̑O�ɁuThe full pathname for this DLL is�v�Ƃ����e�L�X�g���܂܂�Ă���_�ł��B
  
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

�O�q�̊֐���G�N�X�|�[�g�����AXLL �ɂ����� **xlAutoFree12** �̍ŏ����̎�������Ɏ����܂��B 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

���̎����́AXLL �� **XLOPER12** �����񂾂���߂��A�����̕������ **malloc** �݂̂�g�p���Ċ��蓖�Ă�ꍇ�Ɍ���g�p�ł��܂��B���̃e�X�g 
  
 ` if(p_oper->xltype == xltypeStr) `
  
�͎��s���邱�Ƃɒ��ӂ��Ă��������B **xlbitDLLFree** ���ݒ肳��Ă��邽�߂ł� 
  
��ʂɁA **xlAutoFree** �� **xlAutoFree12** ��������AXLL �쐬�� **xltypeMulti** �z��� **xltypeRef** �O���Q�ƂɊ֘A���������������ł���悤�ɂ��Ȃ���΂Ȃ�܂���B 
  
���ׂĂ̏ꍇ�ɓ��I�Ɋ��蓖�Ă�ꂽ **XLOPER** �� **XLOPER12** ��Ԃ��悤�� XLL �֐���������邱�Ƃ�ł��܂��B���̏ꍇ�A **xlbitDLLFree** ��A�T�u�^�C�v�Ɋ֌W�Ȃ��A�����������ׂĂ� **XLOPER** �� **XLOPER12** �Őݒ肷��K�v������܂��B�܂��A���̃������� **XLOPER********XLOPER12** ��Ń|�C���g����郁�������������悤�ɁA /  �� **xlAutoFree12** ���������K�v����邩�����܂���B����́A�߂�l��X���b�h �Z�[�t�ɂ��� 1 �̕��@�ł��B���Ƃ��΁A�O�q�̊֐�����̂悤�ɏ��������邱�Ƃ��ł��܂��B
  
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

**xlAutoFree** �� **xlAutoFree12** �ɂ��ďڂ����́A�u [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md)�v��������������B
  
## <a name="returning-modify-in-place-arguments"></a>�ύX�C���v���[�X������Ԃ�

Excel �ł́AXLL �֐��̓C���v���[�X�ň�����ύX���Ēl��Ԃ����Ƃ��ł��܂��B���̑���́A�|�C���^�[�Ƃ��ēn���ꂽ�����ł̂ݍs�����Ƃ��ł��܂��B���̂悤�ȏ�����s���ɂ́A�֐���o�^����Ƃ��ɁA�ύX�Ώۂ̈����� Excel �ɒʒm���Ȃ���΂Ȃ�܂���B 
  
���̕��@�Œl��Ԃ����Ƃ́A�|�C���^�[�œn�����Ƃ��ł��邷�ׂẴf�[�^�^�ŃT�|�[�g����Ă��܂����A���Ɉȉ��̌^�ŕ֗��ł��B
  
- �������J�E���g����Anull �ŏI������ ASCII �o�C�g������
    
- �������J�E���g����Anull �ŏI������ Unicode ���C�h���������� (Excel 2007 �ȍ~)
    
- **FP** ���������_�z�� 
    
- **FP12** ���������_�z�� (Excel 2007 �ȍ~) 
    
> [!NOTE]
> [!����] ���̕��@�ŁA **XLOPER** �� **XLOPER12** ��Ԃ��Ȃ��ł��������B�ڂ����́A�u [Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B 
  
return ステートメントの代わりにこの手法を使用する利点は、Excel が戻り値のメモリを割り当てるという点です。返されたデータの処理を Excel が完了すれば、メモリを解放します。これにより、XLL 関数はメモリ管理タスクを行わなくて済みます。この手法は、スレッド セーフです。別々のスレッドで同時に Excel によって呼び出された場合、各スレッドの各関数呼び出しは独自のバッファーを持ちます。
  
����́A���ɑO�ɂ������f�[�^�^�Ŗ𗧂����܂��B **XLOPER**/ **XLOPER12** �ɑ΂��đ��݂���Ԃ��ꂽ���ƂɃ������������邽�߂� DLL �ւ̃R�[���o�b�N ���J�j�Y���́A�P���ȕ������ **FP**/ **FP12** �z��ɂ͂Ȃ����߂ł��B���̂��߁ADLL �쐬�̕�����܂��͕��������_�z���Ԃ��ꍇ�A���̑I���������܂��B 
  
- ���I�Ɋ��蓖�Ă�ꂽ�o�b�t�@�[�ɌŒ�|�C���^�[��ݒ肵�A���̃|�C���^�[��Ԃ��܂��B�֐�����ɌĂяo���Ƃ��ɁA(1) �|�C���^�[�� null �ł͂Ȃ����Ƃ�`�F�b�N���A(2) �ȑO�̌Ăяo���Ŋ��蓖�Ă�ꂽ���\�[�X�������A�|�C���^�[�� null �Ƀ��Z�b�g���܂��B(3) �V���Ɋ��蓖�Ă�ꂽ������ �u���b�N�ɂ��̃|�C���^�[��ė��p���܂��B
    
- ������Ɣz���A�������K�v���Ȃ��ÓI�o�b�t�@�[�ɍ쐬���A���̃o�b�t�@�[�ւ̃|�C���^�[��Ԃ��܂��B
    
- ������C���v���[�X�ŕύX���܂��B���̍ہA������܂��͔z��� Excel �O�̗̈�ɒ��ڏ������݂܂��B
    
����ȊO�̕��@�Ń��\�[�X������[�X����ɂ́A **XLOPER**/ **XLOPER12** ��쐬���A **xlbitDLLFree** �� **xlAutoFree**/ **xlAutoFree12** ��g�p����K�v������܂��B 
  
最後のオプションは、その場合は、渡されるが同じ型の引数、戻り値として最も簡単な可能性があります。 重要なポイントは、バッファー サイズの制限は、オーバーランが発生しないことは十分に注意する必要がありますです。 この間違ったを取得すると、Excel がクラッシュする可能性があります。 バッファー サイズの文字列と**FP**/ **FP12**の配列は次に説明します。 
  
## <a name="strings"></a>������

������̃������Ǘ��Ɋւ����肪�A�A�v���P�[�V�����ƃA�h�C�����s����ɂȂ�ł��ʓI�Ȍ����ł��B����������������@ (null �I���܂��͒����J�E���g (���邢�͂��̗���)�A�ÓI�o�b�t�@�[�܂��͓��I�o�b�t�@�[�A�Œ蒷�܂��͂قږ������̒����A�I�y���[�e�B���O �V�X�e���Ǘ������� (���Ƃ��΁AOLE Bstr �Ȃ�)�A�A���}�l�[�W������Ȃ�) �����l�Ȃ��Ƃ�l������ƁA����͗���ł��Ȃ����Ƃł͂���܂���B
  
C/C++ �v���O���}�́Anull �I���̕�����ɂ悭���ʂ��Ă��܂��B�W�� C ���C�u�����́A���̂悤�ȕ������������邽�߂ɐ݌v����Ă��܂��B�R�[�h��̐ÓI�����񃊃e�����́Anull �I��������ɃR���p�C������܂��B�܂��AExcel �ł́A�ʏ�� null �I���ł͂Ȃ������J�E���g�̕������������܂��B��������������g�ݍ��킳��Ă���󋵂ł́A������ƕ����񃁃��������������@�Ɋւ��āADLL/XLL ��Ŗ��m����ѐ��̂�����@���K�v�ƂȂ�܂��B
  
�ł��ʓI�Ȗ���ȉ��Ɏ����܂��B
  
- �L���ȃ|�C���^�[��K�v�Ƃ����̂̃|�C���^�[�̗L�������̂�`�F�b�N���Ȃ��܂��͂ł��Ȃ��֐��ɁAnull �܂��͖����ȃ|�C���^�[���n�����B
    
- �������܂�镶����̒����ɑ΂��ăo�b�t�@�[�̒�����`�F�b�N���Ȃ��܂��͂ł��Ȃ��֐����A������o�b�t�@�[�̋��E��I�[�o�[��������B
    
- �ÓI������o�b�t�@�[ �������A�܂��͊��ɉ�����ꂽ������o�b�t�@�[ �������A���������@�ƈ�т��Ȃ����@�Ŋ��蓖�Ă�ꂽ������o�b�t�@�[ �������������悤�Ƃ��Ă���B
    
- ���蓖�Ă�ꂽ��̂̉�����ꂢ�Ȃ������񂩂琶���郁���� ���[�N�B�ʏ�A�p�ɂɌĂяo�����֐��Ő����܂��B
    
### <a name="rules-for-strings"></a>������̋K��

**XLOPER**/ **XLOPER** ��g�p����ꍇ�A�]���ׂ��������̋K���ƃK�C�h���C��������܂��B�K�C�h���C���́A�O�̃Z�N�V�����Ɠ����ł��B������p�ɓ��ʂɊg�����ꂽ�K��������ɋL���܂��B
  
 **�K��:**
  
- XLL �֐��Ɉ����Ƃ��ēn����郁�����������Ȃ��ł��������B�܂��AXLL �֐��Ɉ����Ƃ��ēn����镶���� **XLOPER**/ **XLOPER12** �܂��͒P���Ȓ����J�E���g�����񂠂邢�� null �I���������㏑�����Ȃ��ł��������B�������������͓ǂݎ���p�ɂ���K�v������܂��B
    
- C API �R�[���o�b�N�֐��̖߂�l�̕����� **XLOPER**/ **XLOPER12** �� Excel ������������蓖�Ă�ꍇ�A **xlFree** ��g�p���ĉ�����邩�AXLL �֐����� Excel �ɕԂ��ꍇ�ɂ� **xlbitXLFree** ��ݒ肵�Ă��������B 
    
- DLL �� **XLOPER**/ **XLOPER12** �̕�����o�b�t�@�[�𓮓I�Ɋ��蓖�Ă�ꍇ�A���蓖�Ď��ƈ�т������@�ŉ�����邩�AXLL �֐����� Excel �ɕԂ����ꍇ�ɂ� **xlbitDLLFree** ��ݒ肵�Ă��� **xlAutoFree**/ **xlAutoFree12** �ŉ�����܂��B
    
- C API �ւ̌Ăяo���� DLL �ɕԂ���� **xltypeMulti** �z��� Excel ������������蓖�Ă��ꍇ�A�z���̂ǂ̕����� **XLOPER**/ **XLOPER12** ��㏑�����Ȃ��ł��������B���������z��� **xlFree** �ɂ���Ă̂݉�����Ă��������B�܂��� XLL �֐��ɂ���ĕԂ����ꍇ�ɂ́A **xlbitXLFree** ��ݒ肵�ĉ�����܂��B
    
### <a name="string-types-supported"></a>�T�|�[�g����镶����^

**C API xltypeStr XLOPER/XLOPER12**

|**�o�C�g������: **XLOPER****|**���C�h����������: **XLOPER12****|
|:-----|:-----|
|���ׂẴo�[�W������ Excel  <br/> |Excel 2007 �ȍ~  <br/> |
|�ő咷:255 �g�� ASCII �o�C�g  <br/> |�ő咷: 32,767 Unicode ����  <br/> |
|�ŏ��� (�����Ȃ�) �o�C�g = ����  <br/> |�ŏ��� Unicode ���� = ����  <br/> |
   
> [!IMPORTANT]
> [!�D�V] **XLOPER** ������܂��� **XLOPER12** ������ null �ŏI������Ƃ͑z�肵�Ȃ��ł��������B 
  
**C/C++ ������**

|**�o�C�g������**|**���C�h����������**|
|:-----|:-----|
|Null で終わる (**char** *)"C"の最大長: 255 に拡張 ASCII バイト  <br/> |Null で終わる (**wchar_t** *) Unicode 文字の最大長の「C %」32,767  <br/> |
|長さカウント (**符号なし char** *)「D」  <br/> |長さカウント (**wchar_t** *)「D %」  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>xltypeMulti XLOPER/XLOPER12 �z���̕�����

�ꍇ�ɂ���ẮAExcel ���ADLL/XLL �Ŏg�p���� **xltypeMulti** �z���쐬���܂��BXLM ���@�\�̒��ɂ́A���������z���Ԃ���̂����܂��B���Ƃ��΁AC API �֐� **xlfGetWorkspace** �́A����  *44*  ���n�����ƁA���ݓo�^����Ă��邷�ׂĂ� DLL �v���V�[�W����L�q���镶�����܂ޔz���Ԃ��܂��BC API �֐� **xlfDialogBox** �́A�z��̈����̕ύX�ς݃R�s�[ (������̏ڍ׃R�s�[��܂݂܂�) ��Ԃ��܂��BXLL �� **xltypeMulti** �z��ɑ�������ł��ʓI�ȏ�ʂ́AXLL �֐��Ɉ����Ƃ��ēn���ꍇ��A�͈͎Q�Ƃ��炱�̌^�ɋ����I�ɂ͂ߍ��ޏꍇ�ł��B��҂̏ꍇ�AExcel �̓\�[�X �Z���̕�����̏ڍ׃R�s�[��쐬���A�z���ł�����|�C���g���܂��B 
  
DLL �ł��������������ύX����ꍇ�ɂ́A�Ǝ��̏ڍ׃R�s�[��ݒ肷��K�v�����肊�܂��B�Ǝ��� **xltypeMulti** �z���쐬����ꍇ�ɂ́A�z���� Excel �ɂ���Ċ��蓖�Ă�ꂽ������ **XLOPER**/ **XLOPER12** ��z�u���Ȃ��ł��������B�z�u����ƁA��قǐ���������ł��Ȃ�������A�܂���������ł��Ȃ��Ȃ����肷�鋰�ꂪ����܂��B�����x�A������̏ڍ׃R�s�[��쐬���A�z���ɂ��̃R�s�[�ւ̃|�C���^�[��i�[���Ȃ���΂Ȃ�܂���B
  
 **例**
  
���̊֐���́A�����J�E���g�� Unicode ������̓��I�Ɋ��蓖�Ă�ꂽ�R�s�[��쐬���܂��B���̗�ł́A�Ăяo�����́A **delete**[] ��g�p���Ċ��蓖�Ă�ꂽ��������ŏI�I�ɉ������K�v�����邱�ƁA����у\�[�X������� null �I���Ƃ͑z�肳��Ă��Ȃ����Ƃɒ��ӂ��Ă��������B�R�s�[������́A���S�̂��߂ɕK�v�ł���ΐ؂�l�߂��Anull �ŏI�����܂���B
  
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

この関数できますし、安全に使用**XLOPER12**の場合をコピーするのには文字列である場合、引数のコピーを返す次のエクスポート可能な XLL 関数のようにします。 その他のすべての種類は、長さ 0 の文字列として返されます。 範囲が処理されないことに注意してください-を返します **#VALUE!** です。 関数は、参照は値で渡されるように U の型引数を受け取るように登録してください。 これは、機能は、**文字列**が長さ 0 の文字列にもエラーを変換する点を除いて、組み込みのワークシート関数の**上**と同じです。 このコード例で、その**xlAutoFree12**は、渡されたポインター、および**削除**を使用して、その内容を解放します。
  
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

### <a name="returning-modify-in-place-string-arguments"></a>�ύX�C���v���[�X�����������Ԃ�

**F**�A **G**�A **F%** �A **G%** �^�Ƃ��ēo�^���ꂽ�����́A�C���v���[�X�ŕύX�ł��܂��BExcel �͂����̌^�̕�����������������Ƃ��ɁA�ő咷�̃o�b�t�@�[��쐬���܂��B���ɁA�Ώە����񂪂��Ȃ�Z���ꍇ�ł����Ă�A�����������o�b�t�@�[�ɃR�s�[���܂��B���̂��߁AXLL �֐��͓�����������ɖ߂�l�𒼐ڏ������ނ��Ƃ��ł��܂��B 
  
���������^�̂��߂Ɏ�蕪������o�b�t�@�[ �T�C�Y�͎��̂Ƃ���ł��B
  
- **�o�C�g������:** 256 �o�C�g (�����J�E���^�[ (G �^) �܂��� null �I�[ (F �^) ��܂݂܂�)�B 
    
- **Unicode ������:** 32,768 ���C�h���� (65,536 �o�C�g)(�����J�E���^�[ (G% �^) �܂��� null �I�[ (F% �^) ��܂݂܂�)�B 
    
> [!NOTE]
> [!����] Visual Basic for Applications (VBA) ���炱�������֐��𒼐ڌĂяo�����Ƃ͂ł��܂���B�\���ȑ傫���̃o�b�t�@�[�����蓖�Ă��Ă��邱�Ƃ�m�F�ł��Ȃ����߂ł��B���������֐��́A�\���ȑ傫���̃o�b�t�@�[�𖾎��I�ɓn���ʂ� DLL ����݈̂��S�ɌĂяo�����Ƃ��ł��܂��B 
  
�W�����C�u�����֐� **wcsrev** ��g�p���āA�n���ꂽ null �I���̃��C�h�����𔽓]������ XLL �֐��̗����Ɏ����܂��B���̏ꍇ�̈����́A�^ **F%** �Ƃ��ēo�^����܂��B
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>�i���L�� (�o�C�i����)

バイナリの名前を定義して、ブックと共に保存されている非構造化データは、バイナリのブロックに関連付けられています。 関数[xlDefineBinaryName](xldefinebinaryname.md)を使用して作成されると、関数[xlGetBinaryName](xlgetbinaryname.md)を使用してデータを取得します。 どちらの関数が関数のリファレンスで詳しく説明されている (を参照してください[C API 関数をことができますされると呼ばれるだけ DLL や XLL から](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md))、 **xltypeBigData** **XLOPER**の両方を使用して/ **XLOPER12**。 
  
�o�C�i�����̎��ۂ̓K�p�𐧌�������m�̖��ɂ��ẮA�u[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B
  
## <a name="excel-stack"></a>Excel �̃X�^�b�N

Excel �́A�ǂݍ��񂾂��ׂĂ� DLL �ƃX�^�b�N�̈����L���܂��B�ʏ�A�X�^�b�N�̈�͕��i�̎g�p�ʂ�������A���Ɏ��グ�邢�����̃K�C�h���C���ɏ]������͖��ƂȂ邱�Ƃ͂���܂���B 
  
- �X�^�b�N��ŁA�֐��ɑ΂�������Ƃ��ĂƂĂ�傫�ȍ\���̂�l�Ƃ��ēn���Ȃ��ł��������B����ɁA�|�C���^�[��Q�Ƃ�n���܂��B
    
- �X�^�b�N�ɑ傫�ȍ\���̂�Ԃ��Ȃ��ł��������B�ÓI�܂��͓��I�Ɋ��蓖�Ă�ꂽ�������ւ̃|�C���^�[��Ԃ����A�Q�Ƃɂ���ēn����������g�p���܂��B
    
- �֐��R�[�h�ŁA���ɑ�K�͂Ȏ����ϐ��\���̂�錾���Ȃ��ł��������B�K�v�ȏꍇ�́A�X�^�e�B�b�N (Static) �Ƃ��Đ錾���܂��B
    
- �ċA�̐[�����󂢂ƕ������Ă���ȊO�́A�֐���ċA�I�ɌĂяo���Ȃ��ł��������B����ɁA���[�v��g�p���܂��B
    
C API ��g�p���� DLL �� Excel �ɃR�[���o�b�N����Ƃ��́AExcel �͍ŏ��ɁA�ň��̎g�p�P�[�X�ɔ����ăX�^�b�N��ɏ\���ȗ̈悪�m�ۂ���Ă��邩�ǂ�����`�F�b�N���܂��B�\���ȗ̈悪�Ȃ��Ɣ��f����ƁA���S�ȌĂяo���Ɏ��s���܂��B����̌Ăяo���ŁA���ۂɂ͏\���ȗ̈悪����ꍇ�ł���s���܂��B���̏ꍇ�ɂ́A�R�[���o�b�N�̓R�[�h **xlretFailed** ��Ԃ��܂��BC API �ƃX�^�b�N�̒ʏ�̎g�p�ł́A���ꂪ C API �Ăяo���̎��s�̌����ƂȂ邱�Ƃ͂قƂ�ǂ���܂���B
  
���̃G���[����������ꍇ�A�܂��͌��O����ꍇ�A���邢�͌����s���̃G���[���������Ƃ��ẴX�^�b�N�̈�̕s����������ꍇ�A[xlStack](xlstack.md) �֐��ւ̌Ăяo���ŃX�^�b�N�̈悪�ǂ�قǂ��邩�𒲂ׂ邱�Ƃ��ł��܂��B 
  
## <a name="see-also"></a>�֘A����



[Excel �ł̃}���`�X���b�h�Čv�Z](multithreaded-recalculation-in-excel.md)
  
[Excel 2007 �ɂ�����}���`�X���b�h�����ƃ���������](multithreading-and-memory-contention-in-excel.md)
  
[Excel XLL �̊J��](developing-excel-xlls.md)

