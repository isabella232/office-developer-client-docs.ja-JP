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
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419542"
---
# <a name="memory-management-in-excel"></a>Excel のメモリ管理

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
効率的で安定した XLL を作成する場合には、メモリ管理が最も重要な課題となります。メモリを管理できないと Microsoft Excel で様々な問題が生じる可能性があります。たとえば、メモリ割り当てや初期化の効率が悪くなったり、小規模なメモリ リークが生じたりするといった比較的小さな問題から、Excel が不安定になるといった大きな問題などが起こる原因となります。
  
�A�h�C���֘A�̐[���Ȗ��̍ł��ʓI�Ȍ������A�������Ǘ��̎��s�ɂ���܂��B���������āA�v���W�F�N�g��r���h����ہA��ѐ�������A�\���ɍl�������������Ǘ��̐헪��g�p����K�v������܂��B 
  
Microsoft Office Excel 2007 �ł̓}���`�X���b�h�̃u�b�N�Čv�Z�̓����ɔ����A�������Ǘ�������܂ňȏ�ɕ��G�ɂȂ�܂����B�X���b�h �Z�[�t�ȃ��[�N�V�[�g�֐���쐬���ăG�N�X�|�[�g����ꍇ�́A�����̃X���b�h���A�N�Z�X�Ɋւ��ċ�������Ƃ��ɐ�����\�������鋣����Ԃ�Ǘ����Ȃ���΂Ȃ�܂���B
  
���� 3 �̃f�[�^�\���̌^�Ɋւ��郁�����̍l������������܂��B
  
- **XLOPER** �� **XLOPER12**
    
- **XLOPER** �ł� **XLOPER12** �ł�Ȃ�������
    
- **FP** �z��� **FP12** �z�� 
    
## <a name="xloperxloper12-memory"></a>XLOPER/XLOPER12 メモリ

**XLOPER**/ **XLOPER12**データ構造体には、メモリブロック (strings (**xltypeStr**)、arrays (**xltypeMulti**)、および外部参照 (**xltyperef**) へのポインターを含むいくつかのサブタイプがあります。 また、 **xltypeMulti**配列には、他のメモリブロックをポイントすることによって、string **XLOPER**/ **xloper12**を含めることもできます。 
  
**XLOPER**/ **XLOPER12** �́A���̂悤�ɂ������̕��@�ō쐬����܂��B 
  
- Excel �ɂ���āBXLL �֐��ɓn�����������������Ƃ�
    
- Excel �ɂ���āBC API �Ăяo���� **XLOPER** �܂��� **XLOPER12** ���Ԃ����Ƃ� 
    
- DLL �ɂ���āBC API �Ăяo���ɓn����������쐬����Ƃ�
    
- DLL によって。XLL 関数の戻り値を作成するとき
    
いずれかのメモリ ポイント型のメモリ ブロックは、次のいくつかの方法で割り当てることができます。
  
- 関数コード外の DLL で静的ブロックとすることができます。この場合、メモリを割り当てたり解放したりする必要はありません。
    
- �֐��R�[�h��� DLL �ŐÓI�u���b�N�Ƃ��邱�Ƃ��ł��܂��B���̏ꍇ�A����������蓖�Ă����������肷��K�v�͂���܂���B
    
- DLL �œ��I�Ɋ��蓖�Ă�����������ł��܂��B���̂��߂ɂ́A **malloc** �� **free**�A **new** �� **delete** �Ȃǂ̕��@������܂��B
    
- Excel �œ��I�Ɋ��蓖�Ă邱�Ƃ��ł��܂��B
    
���X���݂���\�������� **XLOPER**/ **XLOPER12** �������̐��� **XLOPER**/ **XLOPER12** �Ƀ����������蓖�Ă�ꂽ�󋵂̑��l���ɂ��čl������ƁA�ƂĂ������Ɏv���Ă����������܂���B�������A���ɋL���������̋K���ƃK�C�h���C���ɏ]���ƁA���G����啝�ɍ팸�ł��܂��B 
  
### <a name="rules-for-working-with-xloperxloper12"></a>XLOPER/XLOPER12 を扱うときの規則

- ����������������AXLL �֐��Ɉ����Ƃ��ēn����� **XLOPERs**/ **XLOPER12** ��㏑�����Ȃ��ł��������B�������������͓ǂݎ���p�ɂ���K�v������܂��B�ڂ����́A�u **Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��**�v�́u�C�� �v���[�X�̈�����ύX���� **XLOPER** �܂��� [XLOPER12](known-issues-in-excel-xll-development.md) ��Ԃ��v��������������B
    
- C API �ւ̌Ăяo���ŁADLL �ɕԂ���� **XLOPER**/ **XLOPER12** �� Excel ������������蓖�Ă��ꍇ: 
    
  - **XLOPER**/ **XLOPER12** ���s�v�ɂȂ�ꍇ�A [xlFree](xlfree.md) ��Ăяo���ă������������Ȃ���΂Ȃ�܂���B���̑��̕��@ (free�Adelete �Ȃ�) ��g�p���ă������������Ȃ��ł��������B
    
  - �Ԃ����^�� **xltypeMulti** �̂Ƃ��A�z���� **XLOPER**/ **XLOPER12** ��㏑�����Ȃ��ł��������B���ɁA�����񂪊܂܂�Ă���ꍇ�A����ѕ�����ŏ㏑�����悤�Ƃ��Ă���̂ł͂Ȃ��ꍇ�ɒ��ӂ��Ă��������B
    
  - DLL �֐��̖߂�l�Ƃ��� **XLOPER**/ **XLOPER12** �� Excel �ɕԂ��ꍇ�AExcel �ɑ΂��āA�s�v�ɂȂ�����������K�v�����郁���������݂��邱�Ƃ�ʒm���Ȃ���΂Ȃ�܂���B 
    
- **** XLOPER/ **XLOPER12**では、C API 呼び出しへの戻り値として作成された**xlfree**のみを呼び出す必要があります。 
    
- DLL �֐��̖߂�l�Ƃ��� Excel �ɕԂ� **XLOPER**/ **XLOPER12** �� DLL ������������蓖�Ă��ꍇ�ɂ́ADLL ���������K�v�����郁���������݂��邱�Ƃ� Excel �ɒʒm���Ȃ���΂Ȃ�܂���B 
    
### <a name="guidelines-for-memory-management"></a>メモリ管理のガイドライン

- メモリを割り当てて解放するために使用するメソッドを DLL 内で一貫させます。異なるメソッドが混在しないようにします。メモリ クラスまたは構造体で使用するメソッドをラップし、対象メソッドが使用されている多くの場所でコードを変えなくても変更できるようにすることをお勧めします。
    
- DLL �� **xltypeMulti** �z���쐬����ꍇ�A������Ƀ���������蓖�Ă���@���т����Ă��������B�K���������𓮓I�Ɋ��蓖�Ă邩�A�K���ÓI��������g�p���邩�̂ǂ��炩�ɂ��Ă��������B�������Ă����΁A��������������Ƃ��ɁA�������K��������邩�A������Ă͂Ȃ�Ȃ�����������܂��B 
    
- Excel ���쐬���� **XLOPER**/ **XLOPER12** ��R�s�[����Ƃ��́AExcel �����蓖�Ă���������ڍ׃R�s�[���܂��B
    
- Excel �����蓖�Ă������� **XLOPER**/ **XLOPER12** �� **xltypeMulti** �z���ɔz�u���Ȃ��ł��������B������̏ڍ׃R�s�[��쐬���A���̃R�s�[�ւ̃|�C���^�[��z���Ɋi�[���܂��B 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Excel が割り当てた XLOPER/XLOPER12 メモリを解放する

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
  
- 1回の呼び出しで複数の**XLOPER**/ **XLOPER12**s にポインターを渡すことが**** できます。これは、excel の実行中のバージョンでサポートされている関数の引数の数によってのみ制限されます (excel 2003 では、excel 2007 以降では 30)。
    
- **xlFree** �͊܂܂�Ă���|�C���^�[�� **NULL** �ɐݒ肵�A���ɉ�����ꂽ **XLOPER**/ **XLOPER12** �������悤�Ƃ��Ă���S�ȏ�Ԃ�m�ۂ��܂��B **xlFree** �́A������ύX����B��� C API �֐��ł��B 
    
- C API への呼び出しの戻り値には、メモリへのポインターが含まれているかどうかに関係なく、 **XLOPER**/ **XLOPER12**で**xlfree**を安全に呼び出すことができます。 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Excel で解放される XLOPER/XLOPER12 を返す

�O�̃Z�N�V�����ɋL����Ă���R�}���h���A **Boolean** **true** �������n�����Ƃ��ɂ� DLL �p�X�ƃt�@�C������Ԃ��A����ȊO�̏ꍇ�ɂ� **#N/A** ��Ԃ����[�N�V�[�g�֐��ɕύX����ꍇ�ɂ��čl���܂��BExcel �ɕԂ����O�� **xlFree** ��Ăяo���ĕ����񃁃��������ł��Ȃ����Ƃ͖����ł��B�������A�����ꂩ�̎��_�ŉ������Ȃ��ƁA�A�h�C���͊֐����Ăяo����邽�тɃ����� ���[�N��N�����܂��B���̖�������邽�߁Axlcall.h �� **xlbitXLFree** �Ƃ��Ē�`����Ă���A **XLOPER**/ **XLOPER12** �� **xltype** �t�B�[���h�Ƀr�b�g��ݒ�ł��܂��B�����ݒ肷�邱�Ƃɂ���āA�l�̃R�s�[���I�������Ƃ��ɁA�Ԃ��ꂽ��������������K�v�����邱�Ƃ� Excel �ɒʒm���܂��B 
  
### <a name="example"></a>例

次のコード例は、XLL ワークシート関数に変換された、前のセクションの XLL コマンドを示しています。
  
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
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>DLL で解放される XLOPER/XLOPER12 を返す

���l�̖�肪�A **XLOPER**/ **XLOPER12** �̃������� XLL �����蓖�ĂāAExcel �ɖ߂��ꍇ�ɐ����܂��BExcel �́Axlcall.h �� **xlbitDLLFree** �Ƃ��Ē�`����Ă���A **XLOPER**/ **XLOPER12** �� **xltype** �t�B�[���h�ɐݒ�\�ȕʂ̃r�b�g��F�����܂��B 
  
When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s). This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here. Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated. 
  
### <a name="examples"></a>例

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
  
すべての場合に動的に割り当てられた **XLOPER** と **XLOPER12** を返すように XLL 関数を実装することもできます。 その場合、**xlbitDLLFree** を、サブタイプに関係なく、そうしたすべての **XLOPER** と **XLOPER12** で設定する必要があります。 また、 **xlAutoFree**と**xlAutoFree12**を実装して、このメモリが解放され、 **XLOPER**/ **XLOPER12**内でポイントするメモリがあるようにする必要もあります。 これは、戻り値をスレッド セーフにする 1 つの方法です。 たとえば、前述の関数を次のように書き換えることができます。
  
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
  
## <a name="returning-modify-in-place-arguments"></a>変更インプレース引数を返す

Excel では、XLL 関数はインプレースで引数を変更して値を返すことができます。この操作は、ポインターとして渡された引数でのみ行うことができます。このような処理を行うには、関数を登録するときに、変更対象の引数を Excel に通知しなければなりません。  
  
���̕��@�Œl��Ԃ����Ƃ́A�|�C���^�[�œn�����Ƃ��ł��邷�ׂẴf�[�^�^�ŃT�|�[�g����Ă��܂����A���Ɉȉ��̌^�ŕ֗��ł��B
  
- �������J�E���g����Anull �ŏI������ ASCII �o�C�g������
    
- �������J�E���g����Anull �ŏI������ Unicode ���C�h���������� (Excel 2007 �ȍ~)
    
- **FP** ���������_�z�� 
    
- **FP12** ���������_�z�� (Excel 2007 �ȍ~) 
    
> [!NOTE]
> [!����] ���̕��@�ŁA **XLOPER** �� **XLOPER12** ��Ԃ��Ȃ��ł��������B�ڂ����́A�u [Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B 
  
The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values. Once Excel has finished reading the returned data, it releases the memory. This takes the memory management tasks away from the XLL function. This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.
  
����́A���ɑO�ɂ������f�[�^�^�Ŗ𗧂����܂��B **XLOPER**/ **XLOPER12** �ɑ΂��đ��݂���Ԃ��ꂽ���ƂɃ������������邽�߂� DLL �ւ̃R�[���o�b�N ���J�j�Y���́A�P���ȕ������ **FP**/ **FP12** �z��ɂ͂Ȃ����߂ł��B���̂��߁ADLL �쐬�̕�����܂��͕��������_�z���Ԃ��ꍇ�A���̑I���������܂��B 
  
- ���I�Ɋ��蓖�Ă�ꂽ�o�b�t�@�[�ɌŒ�|�C���^�[��ݒ肵�A���̃|�C���^�[��Ԃ��܂��B�֐�����ɌĂяo���Ƃ��ɁA(1) �|�C���^�[�� null �ł͂Ȃ����Ƃ�`�F�b�N���A(2) �ȑO�̌Ăяo���Ŋ��蓖�Ă�ꂽ���\�[�X�������A�|�C���^�[�� null �Ƀ��Z�b�g���܂��B(3) �V���Ɋ��蓖�Ă�ꂽ������ �u���b�N�ɂ��̃|�C���^�[��ė��p���܂��B
    
- 文字列と配列を、解放する必要がない静的バッファーに作成し、そのバッファーへのポインターを返します。
    
- ������C���v���[�X�ŕύX���܂��B���̍ہA������܂��͔z��� Excel �O�̗̈�ɒ��ڏ������݂܂��B
    
����ȊO�̕��@�Ń��\�[�X������[�X����ɂ́A **XLOPER**/ **XLOPER12** ��쐬���A **xlbitDLLFree** �� **xlAutoFree**/ **xlAutoFree12** ��g�p����K�v������܂��B 
  
The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value. The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them. Getting this wrong could crash Excel. Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next. 
  
## <a name="strings"></a>文字列

文字列のメモリ管理に関する問題が、アプリケーションとアドインが不安定になる最も一般的な原因です。文字列を処理する方法 (null 終了または長さカウント (あるいはその両方)、静的バッファーまたは動的バッファー、固定長またはほぼ無制限の長さ、オペレーティング システム管理メモリ (たとえば、OLE Bstr など)、アンマネージ文字列など) が多様なことを考慮すると、これは理解できないことではありません。
  
C/C++ �v���O���}�́Anull �I���̕�����ɂ悭���ʂ��Ă��܂��B�W�� C ���C�u�����́A���̂悤�ȕ������������邽�߂ɐ݌v����Ă��܂��B�R�[�h��̐ÓI�����񃊃e�����́Anull �I��������ɃR���p�C������܂��B�܂��AExcel �ł́A�ʏ�� null �I���ł͂Ȃ������J�E���g�̕������������܂��B��������������g�ݍ��킳��Ă���󋵂ł́A������ƕ����񃁃��������������@�Ɋւ��āADLL/XLL ��Ŗ��m����ѐ��̂�����@���K�v�ƂȂ�܂��B
  
�ł��ʓI�Ȗ���ȉ��Ɏ����܂��B
  
- �L���ȃ|�C���^�[��K�v�Ƃ����̂̃|�C���^�[�̗L�������̂�`�F�b�N���Ȃ��܂��͂ł��Ȃ��֐��ɁAnull �܂��͖����ȃ|�C���^�[���n�����B
    
- �������܂�镶����̒����ɑ΂��ăo�b�t�@�[�̒�����`�F�b�N���Ȃ��܂��͂ł��Ȃ��֐����A������o�b�t�@�[�̋��E��I�[�o�[��������B
    
- 静的文字列バッファー メモリ、または既に解放された文字列バッファー メモリ、解放する方法と一貫しない方法で割り当てられた文字列バッファー メモリを解放しようとしている。
    
- 割り当てられたものの解放されいない文字列から生じるメモリ リーク。通常、頻繁に呼び出される関数で生じます。
    
### <a name="rules-for-strings"></a>文字列の規則

**XLOPER**/ **XLOPER** ��g�p����ꍇ�A�]���ׂ��������̋K���ƃK�C�h���C��������܂��B�K�C�h���C���́A�O�̃Z�N�V�����Ɠ����ł��B������p�ɓ��ʂɊg�����ꂽ�K��������ɋL���܂��B
  
 **�K��:**
  
- XLL �֐��Ɉ����Ƃ��ēn����郁�����������Ȃ��ł��������B�܂��AXLL �֐��Ɉ����Ƃ��ēn����镶���� **XLOPER**/ **XLOPER12** �܂��͒P���Ȓ����J�E���g�����񂠂邢�� null �I���������㏑�����Ȃ��ł��������B�������������͓ǂݎ���p�ɂ���K�v������܂��B
    
- C API �R�[���o�b�N�֐��̖߂�l�̕����� **XLOPER**/ **XLOPER12** �� Excel ������������蓖�Ă�ꍇ�A **xlFree** ��g�p���ĉ�����邩�AXLL �֐����� Excel �ɕԂ��ꍇ�ɂ� **xlbitXLFree** ��ݒ肵�Ă��������B 
    
- DLL �� **XLOPER**/ **XLOPER12** �̕�����o�b�t�@�[�𓮓I�Ɋ��蓖�Ă�ꍇ�A���蓖�Ď��ƈ�т������@�ŉ�����邩�AXLL �֐����� Excel �ɕԂ����ꍇ�ɂ� **xlbitDLLFree** ��ݒ肵�Ă��� **xlAutoFree**/ **xlAutoFree12** �ŉ�����܂��B
    
- C API �ւ̌Ăяo���� DLL �ɕԂ���� **xltypeMulti** �z��� Excel ������������蓖�Ă��ꍇ�A�z���̂ǂ̕����� **XLOPER**/ **XLOPER12** ��㏑�����Ȃ��ł��������B���������z��� **xlFree** �ɂ���Ă̂݉�����Ă��������B�܂��� XLL �֐��ɂ���ĕԂ����ꍇ�ɂ́A **xlbitXLFree** ��ݒ肵�ĉ�����܂��B
    
### <a name="string-types-supported"></a>サポートされる文字列型

**C API xltypeStr XLOPER/XLOPER12**

|**�o�C�g������: **XLOPER****|**���C�h����������: **XLOPER12****|
|:-----|:-----|
|���ׂẴo�[�W������ Excel  <br/> |Excel 2007 �ȍ~  <br/> |
|�ő咷:255 �g�� ASCII �o�C�g  <br/> |最大長: 32,767 Unicode 文字  <br/> |
|最初の (符号なし) バイト = 長さ  <br/> |�ŏ��� Unicode ���� = ����  <br/> |
   
> [!IMPORTANT]
> [!�D�V] **XLOPER** ������܂��� **XLOPER12** ������ null �ŏI������Ƃ͑z�肵�Ȃ��ł��������B 
  
**C/C++ ������**

|**�o�C�g������**|**���C�h����������**|
|:-----|:-----|
|Null 終了 (**char** *)"C" の最大長:255 拡張 ASCII バイト  <br/> |Null 終了 (**wchar_t** *) "C%" 最大長: 32,767 Unicode 文字  <br/> |
|長さカウント (**unsigned char** *) "D"  <br/> |長さカウント (**wchar_t** *) "D%"  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>xltypeMulti XLOPER/XLOPER12 配列内の文字列

�ꍇ�ɂ���ẮAExcel ���ADLL/XLL �Ŏg�p���� **xltypeMulti** �z���쐬���܂��BXLM ���@�\�̒��ɂ́A���������z���Ԃ���̂����܂��B���Ƃ��΁AC API �֐� **xlfGetWorkspace** �́A����  *44*  ���n�����ƁA���ݓo�^����Ă��邷�ׂĂ� DLL �v���V�[�W����L�q���镶�����܂ޔz���Ԃ��܂��BC API �֐� **xlfDialogBox** �́A�z��̈����̕ύX�ς݃R�s�[ (������̏ڍ׃R�s�[��܂݂܂�) ��Ԃ��܂��BXLL �� **xltypeMulti** �z��ɑ�������ł��ʓI�ȏ�ʂ́AXLL �֐��Ɉ����Ƃ��ēn���ꍇ��A�͈͎Q�Ƃ��炱�̌^�ɋ����I�ɂ͂ߍ��ޏꍇ�ł��B��҂̏ꍇ�AExcel �̓\�[�X �Z���̕�����̏ڍ׃R�s�[��쐬���A�z���ł�����|�C���g���܂��B 
  
DLL �ł��������������ύX����ꍇ�ɂ́A�Ǝ��̏ڍ׃R�s�[��ݒ肷��K�v�����肊�܂��B�Ǝ��� **xltypeMulti** �z���쐬����ꍇ�ɂ́A�z���� Excel �ɂ���Ċ��蓖�Ă�ꂽ������ **XLOPER**/ **XLOPER12** ��z�u���Ȃ��ł��������B�z�u����ƁA��قǐ���������ł��Ȃ�������A�܂���������ł��Ȃ��Ȃ����肷�鋰�ꂪ����܂��B�����x�A������̏ڍ׃R�s�[��쐬���A�z���ɂ��̃R�s�[�ւ̃|�C���^�[��i�[���Ȃ���΂Ȃ�܂���B
  
 **Examples**
  
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

This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string. All other types are returned as a zero-length string. Note that ranges are not handled—the function returns **#VALUE!**. The function must be registered as taking a type U argument so that references are passed in as values. This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings. This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.
  
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

### <a name="returning-modify-in-place-string-arguments"></a>変更インプレース文字列引数を返す

**F**�A **G**�A **F%** �A **G%** �^�Ƃ��ēo�^���ꂽ�����́A�C���v���[�X�ŕύX�ł��܂��BExcel �͂����̌^�̕�����������������Ƃ��ɁA�ő咷�̃o�b�t�@�[��쐬���܂��B���ɁA�Ώە����񂪂��Ȃ�Z���ꍇ�ł����Ă�A�����������o�b�t�@�[�ɃR�s�[���܂��B���̂��߁AXLL �֐��͓�����������ɖ߂�l�𒼐ڏ������ނ��Ƃ��ł��܂��B 
  
���������^�̂��߂Ɏ�蕪������o�b�t�@�[ �T�C�Y�͎��̂Ƃ���ł��B
  
- **バイト文字列:** 256 バイト (長さカウンター (G 型) または null 終端 (F 型) を含みます)。 
    
- **Unicode 文字列:** 32,768 ワイド文字 (65,536 バイト)(長さカウンター (G% 型) または null 終端 (F% 型) を含みます)。 
    
> [!NOTE]
> [!����] Visual Basic for Applications (VBA) ���炱�������֐��𒼐ڌĂяo�����Ƃ͂ł��܂���B�\���ȑ傫���̃o�b�t�@�[�����蓖�Ă��Ă��邱�Ƃ�m�F�ł��Ȃ����߂ł��B���������֐��́A�\���ȑ傫���̃o�b�t�@�[�𖾎��I�ɓn���ʂ� DLL ����݈̂��S�ɌĂяo�����Ƃ��ł��܂��B 
  
�W�����C�u�����֐� **wcsrev** ��g�p���āA�n���ꂽ null �I���̃��C�h�����𔽓]������ XLL �֐��̗����Ɏ����܂��B���̏ꍇ�̈����́A�^ **F%** �Ƃ��ēo�^����܂��B
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>永続記憶 (バイナリ名)

Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook. They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md). Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**. 
  
�o�C�i�����̎��ۂ̓K�p�𐧌�������m�̖��ɂ��ẮA�u[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B
  
## <a name="excel-stack"></a>Excel のスタック

Excel は、読み込んだすべての DLL とスタック領域を共有します。通常、スタック領域は普段の使用量よりも多く、次に取り上げるいくつかのガイドラインに従う限りは問題となることはありません。  
  
- �X�^�b�N��ŁA�֐��ɑ΂�������Ƃ��ĂƂĂ�傫�ȍ\���̂�l�Ƃ��ēn���Ȃ��ł��������B����ɁA�|�C���^�[��Q�Ƃ�n���܂��B
    
- �X�^�b�N�ɑ傫�ȍ\���̂�Ԃ��Ȃ��ł��������B�ÓI�܂��͓��I�Ɋ��蓖�Ă�ꂽ�������ւ̃|�C���^�[��Ԃ����A�Q�Ƃɂ���ēn����������g�p���܂��B
    
- �֐��R�[�h�ŁA���ɑ�K�͂Ȏ����ϐ��\���̂�錾���Ȃ��ł��������B�K�v�ȏꍇ�́A�X�^�e�B�b�N (Static) �Ƃ��Đ錾���܂��B
    
- �ċA�̐[�����󂢂ƕ������Ă���ȊO�́A�֐���ċA�I�ɌĂяo���Ȃ��ł��������B����ɁA���[�v��g�p���܂��B
    
C API ��g�p���� DLL �� Excel �ɃR�[���o�b�N����Ƃ��́AExcel �͍ŏ��ɁA�ň��̎g�p�P�[�X�ɔ����ăX�^�b�N��ɏ\���ȗ̈悪�m�ۂ���Ă��邩�ǂ�����`�F�b�N���܂��B�\���ȗ̈悪�Ȃ��Ɣ��f����ƁA���S�ȌĂяo���Ɏ��s���܂��B����̌Ăяo���ŁA���ۂɂ͏\���ȗ̈悪����ꍇ�ł���s���܂��B���̏ꍇ�ɂ́A�R�[���o�b�N�̓R�[�h **xlretFailed** ��Ԃ��܂��BC API �ƃX�^�b�N�̒ʏ�̎g�p�ł́A���ꂪ C API �Ăяo���̎��s�̌����ƂȂ邱�Ƃ͂قƂ�ǂ���܂���B
  
���̃G���[����������ꍇ�A�܂��͌��O����ꍇ�A���邢�͌����s���̃G���[���������Ƃ��ẴX�^�b�N�̈�̕s����������ꍇ�A[xlStack](xlstack.md) �֐��ւ̌Ăяo���ŃX�^�b�N�̈悪�ǂ�قǂ��邩�𒲂ׂ邱�Ƃ��ł��܂��B 
  
## <a name="see-also"></a>関連項目



[Excel でのマルチスレッド再計算](multithreaded-recalculation-in-excel.md)
  
[Excel 2007 �ɂ�����}���`�X���b�h�����ƃ���������](multithreading-and-memory-contention-in-excel.md)
  
[Excel XLL の開発](developing-excel-xlls.md)

