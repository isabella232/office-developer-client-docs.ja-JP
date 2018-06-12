---
title: Excel での Dll のアクセス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- accessing dlls [excel 2007],DLLs [Excel 2007], accessing in Excel
localization_priority: Normal
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: bfb562b6bbe824124c6b5a691745d076720ee004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798884"
---
# <a name="access-dlls-in-excel"></a>Excel での Dll のアクセス

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel �� DLL �֐���R�}���h�ɂ́A���܂��܂ȕ��@�ŃA�N�Z�X�ł��܂��B
  
- **Declare** �X�e�[�g�����g��g�p���āA�֐��܂��̓R�}���h���g�p�\�ł���悤�ɂȂ��Ă��� Microsoft Visual Basic for Applications (VBA) �R�[�h ���W���[����ʂ��ăA�N�Z�X����B 
    
- **CALL** �֐��܂��� **REGISTER** �֐���g�p���āAXLM �}�N�� �V�[�g��ʂ��ăA�N�Z�X����B 
    
- ���ڃ��[�N�V�[�g����A�܂��̓��[�U�[ �C���^�[�t�F�C�X (UI) �̃J�X�^�}�C�Y���ꂽ���ڂ���A�N�Z�X����B
    
���̃h�L�������g�ł́AXLM �֐��ɂ��Ă͐�����܂���B����ȊO�� 2 �̕��@�̂����A�ǂ��炩��g�p���邱�Ƃ�����߂��܂��B
  
���ڃ��[�N�V�[�g����A�܂��� UI �̃J�X�^�}�C�Y���ꂽ���ڂ���A�N�Z�X����ɂ́A�ŏ��Ɋ֐��܂��̓R�}���h�� Excel �ɓo�^����K�v������܂��B�R�}���h�܂��͊֐��̓o�^�̏ڍׂɂ��ẮA�u[Excel �� XLL �R�[�h�ɃA�N�Z�X����](accessing-xll-code-in-excel.md)�v��Q�Ƃ��Ă��������B
  
## <a name="calling-dll-functions-and-commands-from-vba"></a>DLL の関数やコマンドを VBA から呼び出す

**Declare** �X�e�[�g�����g��g�p����ƁAVBA �� DLL �֐���R�}���h�ɃA�N�Z�X�ł��܂��B���̃X�e�[�g�����g�ɂ́A�R�}���h�p�̍\���Ɗ֐��p�̍\���� 1 ������܂��B 
  
- **�\�� 1 ? �R�}���h**
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- **�\�� 2 ? �֐�**
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

�ȗ��\�� **Public** �L�[���[�h�� **Private** �L�[���[�h�ł́A�C���|�[�g�����֐��̃X�R�[�v��w�肵�܂� (���ꂼ��AVisual Basic �v���W�F�N�S�́A�܂��� Visual Basic ���W���[���̂�)�Bname �� VBA �R�[�h�Ŏg�p���閼�O�ɂȂ�܂��B���̖��O�� DLL �̖��O�ƈقȂ�ꍇ�́A�ʖ��ualiasname�v�w��q��g�p����K�v������܂��B�܂��A�֐��ɂ́ADLL �ɂ���ăG�N�X�|�[�g����閼�O��t����K�v������܂��BDLL �����ԍ��ւ̎Q�Ƃ� DLL �֐��ɃA�N�Z�X����ꍇ�́A�ʖ� (�擪�� **#** ��t����������) ��w�肷��K�v������܂��B
  
�R�}���h�� **void** ��Ԃ��K�v������܂��B�֐��́AVBA �� **ByVal** ��F���ł���^��Ԃ��K�v������܂��B�܂�A�������̌^ (������A�z��A���[�U�[��`�^�A����уI�u�W�F�N�g) �͈�����C���v���[�X�ŕύX���邱�ƂŁA���ȒP�ɕԂ����Ƃ������Ƃł��B
  
> [!NOTE]
> [!����] VBA �ł́AVisual Basic ���W���[���Ŏ����ꂽ�������X�g�Ɩ߂�l�� DLL �ŃR�[�h�����ꂽ��̂Ɠ����ł��邱�Ƃ�m�F�ł��܂���B����͎����ŐT�d�Ɋm�F����K�v������܂��B�ԈႢ������� Excel ���N���b�V������\��������܂��B 
  
�֐��܂��̓R�}���h�̈������Q�Ƃ܂��̓|�C���^�[�œn����Ȃ��ꍇ�́A **arglist** �錾�ň����̑O�� **ByVal** �L�[���[�h��t����K�v������܂��BC/C++ �֐����|�C���^�[�̈�����󂯎��ꍇ��AC++ �֐����Q�Ƃ̈�����󂯎��ꍇ�́A **ByRef** �n���ɂ���K�v������܂��B **ByRef** �L�[���[�h�́AVBA �ł͊���ł��邽�߈������X�g�ŏȗ����邱�Ƃ�ł��܂��B 
  
### <a name="argument-types-in-cc-and-vba"></a>C および C++ と VBA の引数の型

C/C++ �� VBA �̈����̌^�̐錾���r����Ƃ��ɂ́A���̓_�ɒ��ӂ��K�v�ł��B
  
- VBA �� **String** �́AByVal �n���̏ꍇ�̓o�C�g������ BSTR �\���̂ւ̃|�C���^�[�Ƃ��ēn����܂��B **ByRef** �n���̏ꍇ�̓|�C���^�[�ւ̃|�C���^�[�Ƃ��ēn����܂��B
    
- �������i�[���Ă��� VBA �� **Variant** �́A **ByVal** �n���̏ꍇ�� Unicode ���C�h���������� BSTR �\���̂ւ̃|�C���^�[�Ƃ��ēn����܂��B **ByRef** �n���̏ꍇ�̓|�C���^�[�ւ̃|�C���^�[�Ƃ��ēn����܂��B
    
- VBA �� **Integer** �́AC/C++ �� signed short �Ɠ����� 16 �r�b�g�^�ł��B 
    
- VBA �� **Long** �́AC/C++ �� signed int �Ɠ����� 32 �r�b�g�^�ł��B 
    
- VBA と C または C++ の両方**の種類**と**構造体**のステートメントをそれぞれ使用して、ユーザー定義データ型の定義を許可します。 
    
- VBA �� C/C++ �́A�ǂ���� **Variant** �f�[�^�^��T�|�[�g���Ă��܂��BC/C++ �ɂ��ẮAWindows OLE/COM �w�b�_�[ �t�@�C����� VARIANT �Ƃ��Ē�`����Ă��܂��B 
    
- VBA �̔z��� OLE �� **SafeArrays** �ł��BC/C++ �ɂ��ẮAWindows OLE/COM �w�b�_�[ �t�@�C����� **SAFEARRAY** �Ƃ��Ē�`����Ă��܂��B
    
- VBA �� **Currency** �f�[�^�^�́A **ByVal** �n���̏ꍇ�� Windows �w�b�_�[ �t�@�C�� wtypes.h ��Œ�`����Ă��� **CY** �^�̍\���̂Ƃ��ēn����܂��B **ByRef** �n���̏ꍇ�� this �ւ̃|�C���^�[�Ƃ��ēn����܂��B
    
VBA では、ユーザー定義データ型のデータ要素では、Visual Studio は、既定では、圧縮されている 8 バイト境界には、4 バイト境界にパックされます。 C または C++ の構造体の定義を囲む必要がありますので、`#pragma pack(4) … #pragma pack()`がずれて要素を避けるためにブロックします。 
  
���ɁA�����̃��[�U�[ �^�C�v��`�̗������܂��B
  
```vb
Type VB_User_Type
    i As Integer
    d As Double
    s As String
End Type

```

```cpp
#pragma pack(4)
struct C_user_type
{
    short iVal;
    double dVal;
    BSTR bstr; // VBA String type is a byte string
}
#pragma pack() // restore default

```

VBA �́AExcel ���T�|�[�g�����������̒l�͈̔͂�T�|�[�g���邱�Ƃ�����܂��BVBA �� double �� IEEE �ɏ������Ă��āA�����_�̃��[�N�V�[�g�ł� 0 �ɐ؂�̂Ă��Ă���񐳋K������T�|�[�g���Ă��܂��BVBA �� **Date** �^�́A���̃V���A�������ꂽ���t��g�p���邱�Ƃ� 1-Jan-0100 (100 �N 1 �� 1 ��) ����O�̓��t��\���ł��܂��BExcel �ł́A�[���ȏ�̃V���A�������ꂽ���t�݂̂����e����܂��BVBA �� **Currency** �^ (64 �r�b�g�����ɃX�P�[�����O����܂�) �́A8 �o�C�g�� double �ł̓T�|�[�g����Ȃ����x������ł��邽�߃��[�N�V�[�g�ł͈�v���܂���B 
  
Excel �́AVBA ���[�U�[��`�֐��ɁA���Ɏ����^�̃o���A���g�݂̂�n���܂��B
  
|**VBA �f�[�^�^**|**C/C++ �o���A���g�^�̃r�b�g �t���O**|**���**|
|:-----|:-----|:-----|
|Double  <br/> |**VT_R8** <br/> ||
|Boolean  <br/> |**VT_BOOL** <br/> ||
|Date  <br/> |**VT_DATE** <br/> ||
|String  <br/> |**VT_BSTR** <br/> |OLE Bstr �o�C�g������  <br/> |
|Range  <br/> |**VT_DISPATCH** <br/> |�͈͂ƃZ���̎Q��  <br/> |
|�z���܂ރo���A���g�^  <br/> |**VT_ARRAY** | **VT_VARIANT** <br/> |���e�����z��  <br/> |
|Ccy  <br/> |**VT_CY** <br/> |64 �r�b�g������g�����āA�����_�ȉ� 4 ���Ɏl�̌ܓ��������x������܂��B  <br/> |
|�G���[��܂ރo���A���g�^  <br/> |**VT_ERROR** <br/> ||
||**制約** <br/> |��̃Z���܂��͏ȗ����ꂽ����  <br/> |
   
**VarType** ��g�p���āA�n���ꂽ VBA �o���A���g�^�̎�ނ�m�F�ł��܂��B�������A�Q�Ƃ�g�p���ČĂяo���ꂽ�Ƃ��ɔ͈͂̒l�̌^��Ԃ��֐�������܂��B **Variant** �� **Range** �Q�ƃI�u�W�F�N�g���ǂ����𔻒f����ꍇ�́A **IsObject** �֐���g�p�ł��܂��B 
  
**Value** �v���p�e�B�� **Variant** �Ɋ��蓖�Ă邱�ƂŁA **Range** ���� VBA �o���A���g�^�̔z���܂� **Variants** ��쐬�ł��܂��B���̎��_�ŗL���ł������n��ݒ�̕W���ʉ݌`����g�p���ď���������\�[�X�͈͂Ɋ܂܂��Z���́A **Currency** �^�̔z��v�f�ɕϊ�����܂��B���t�Ƃ��ď��������ꂽ�Z���́A **Date** �̔z��v�f�ɕϊ�����܂��B�������܂�ł���Z���́A���C�h���� **BSTR** �o���A���g�ɕϊ�����܂��B�G���[��܂�ł���Z���́A **VT_ERROR** �^�� **Variants** �ɕϊ�����܂��B **Boolean** **True** �܂��� **False** ��܂�ł���Z���́A **VT_BOOL** �^�� **Variants** �ɕϊ�����܂��B 
  
> [!NOTE]
> [!����] **Variant** �� **True** �� ?1�A **False** �� 0 �Ƃ��Ċi�[���܂��B���t�܂��͒ʉ݋�z�Ƃ��ď���������Ă��Ȃ����l�́A **VT_R8** �^�̃o���A���g�ɕϊ�����܂��B 
  
### <a name="variant-and-string-arguments"></a>バリアント型と文字列の引数

Excel �́A����I�Ƀ��C�h���� Unicode ������œ��삵�Ă��܂��BVBA ���[�U�[��**** �֐��� **String** �����ł͂Ȃ� **Variant** ��󂯓����悤�ɂ���K�v������܂��B����ɂ��ADLL �֐��́A���� **Variant** BSTR ���C�h����������� VBA ����󂯓���ł���悤�ɂȂ�܂��B 
  
DLL ���� VBA �� Unicode �������Ԃ��ꍇ�́A **Variant** �����������C���v���[�X�ŕύX����K�v������܂��B���ꂪ���삷��ɂ́AC/C++ �R�[�h��� DLL �֐��� **Variant** �ւ̃|�C���^�[��󂯎��悤�ɐ錾���āAVBA �R�[�h��ň�����  `ByRef varg As Variant` �Ƃ��Đ錾����K�v������܂��B�Â�������̃������͉������K�v������܂��B�܂��A�V����������l�� OLE Bstr ������֐��� DLL ��ɂ̂ݍ쐬����܂��B
  
DLL ���� VBA �Ƀo�C�g�������Ԃ��ꍇ�́A�o�C�g������ BSTR ������C���v���[�X�ŕύX����K�v������܂��B���ꂪ���삷��ɂ́AC/C++ �R�[�h��� DLL �֐��� BSTR �ւ̃|�C���^�[�̃|�C���^�[��󂯎��悤�ɐ錾���āAVBA �R�[�h��ň����� ' **ByRef varg As String**' �Ƃ��Đ錾����K�v������܂��B
  
���̂悤�ȕ��@�� VBA ����n���ꂽ������́A�������֘A�̖������邽�߂ɁAOLE BSTR ������֐���g�p���Ă̂ݏ�������K�v������܂��B���Ƃ��΁A�n���ꂽ�������㏑������O�� **SysFreeString** ��Ăяo���ă������������A **SysAllocStringByteLen** �܂��� **SysAllocStringLen** ��Ăяo���ĐV����������̗̈����蓖�Ă�K�v������܂��B 
  
Excel ���[�N�V�[�g�̃G���[�́A���̕\�Ɏ���������w�肵�� **CVerr** �֐���g�p���邱�ƂŁAVBA �� **Variants** �Ƃ��č쐬�ł��܂��B�܂��A���[�N�V�[�g�̃G���[�́A **VT_ERROR** �^�� **Variants** ��g�p���āA���Ɏ����l�� **ulVal** �t�B�[���h�ɐݒ肷�邱�ƂŁADLL ���� VBA �ɕԂ����Ƃ�ł��܂��B 
  
|**�G���[**|**�o���A���g�^�� ulVal �l**|**CVerr ����**|
|:-----|:-----|:-----|
|#NULL!  <br/> |2148141008  <br/> |2000  <br/> |
|#DIV/0!  <br/> |2148141015  <br/> |2007  <br/> |
|#VALUE!  <br/> |2148141023  <br/> |2015  <br/> |
|#REF!  <br/> |2148141031  <br/> |2023  <br/> |
|#NAME?  <br/> |2148141037  <br/> |2029  <br/> |
|#NUM!  <br/> |2148141044  <br/> |2036  <br/> |
|#N/A  <br/> |2148141050  <br/> |2042  <br/> |
   
����̃o���A���g�^�� **ulVal** �l�́A **CVerr** �����̒l�� 16 �i���� x800A0000 ���������̂Ɠ����ɂȂ�_�ɒ��ڂ��Ă��������B 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a>ワークシートから直接、DLL 関数を呼び出す

���Ƃ��΁A�C���^�[�t�F�C�X�Ƃ��� VBA �܂��� XLM ��g�p���邱�ƂȂ��A���[�N�V�[�g���� Win32 DLL �̊֐��ɃA�N�Z�X���邱�Ƃ͂ł��܂���B�܂��A���̊֐��̈����Ɩ߂�l�̌^�ɂ��Ď��O�� Excel �ɒm�点�Ă����K�v�����܂��B�����s���v���Z�X��A�o�^�ƌĂт܂��B
  
���Ɏ����悤�ȕ��@�ŁA���[�N�V�[�g���� DLL �̊֐��ɃA�N�Z�X�ł��܂��B
  
- �O�q�����悤�� VBA �Ŋ֐���錾���āA���̊֐��� VBA ���[�U�[��`�֐��ŃA�N�Z�X���܂��B
    
- XLM �}�N�� �V�[�g�� CALL ��g�p���邱�Ƃ� DLL �֐���Ăяo���āAXLM ���[�U�[��`�֐�����A�N�Z�X���܂��B
    
- XLM �R�}���h�܂��� VBA �R�}���h��g�p���� XLM �� **REGISTER** �֐���Ăяo���܂��B����ɂ��A�֐������[�N�V�[�g �Z���ɓ��͂��ꂽ�Ƃ��ɁA���̊֐���F�����邽�߂� Excel ���K�v�Ƃ������񋟂��܂��B 
    
- DLL �� XLL �ɕϊ����āAXLL ��L��������Ƃ��� C API �� **xlfRegister** �֐���g�p���Ċ֐���o�^���܂��B 
    
4 �Ԗڂ̃A�v���[�`�͎��Ȋ����^�ł���A�֐���o�^����R�[�h�Ɗ֐��̃R�[�h�́A�ǂ��������R�[�h �v���W�F�N�g�Ɋ܂܂�Ă��܂��B�A�h�C���ɕύX������Ă�AXLM �V�[�g�� VBA �R�[�h�ɕύX�������K�v�͂���܂���BC API �̋@�\��ێ������܂ܓK�؂ɊǗ����ꂽ���@�ł����s���ɂ́ADLL �� XLL �ɕϊ����āA���̌��ʂ̃A�h�C����A�h�C�� �}�l�[�W���[�œǂݍ��ޕK�v������܂��B����ɂ��A�A�h�C�����ǂݍ��܂��� (�܂��͗L����������)�ADLL �Ō��J���Ă�֐��� Excel ����Ăяo����悤�ɂȂ�AXLL �Ɋ܂܂�邷�ׂĂ̊֐���o�^���āA���̑��� DLL �̏���������s�ł��܂��B
  
## <a name="calling-dll-commands-directly-from-excel"></a>Excel から直接 DLL のコマンドを呼び出す

Win32 DLL �R�}���h�́AVBA �Ȃǂ̃C���^�[�t�F�C�X�����݂��Ȃ��ꍇ��A���O�ɃR�}���h���o�^����Ă��Ȃ��ꍇ�́AExcel �̃_�C�A���O �{�b�N�X�⃁�j���[���璼�ڃA�N�Z�X���邱�Ƃ͂ł��܂���B
  
���Ɏ����悤�ȕ��@�� DLL �̃R�}���h�ɃA�N�Z�X�ł��܂��B
  
- �O�q�����悤�� VBA �ŃR�}���h��錾���āAVBA �}�N������A�N�Z�X���܂��B
    
- XLM �}�N�� �V�[�g�� **CALL** ��g�p���邱�Ƃ� DLL �R�}���h��Ăяo���āAXLM �}�N������A�N�Z�X���܂��B 
    
- XLM �R�}���h�܂��� VBA �R�}���h��g�p���� XLM �� **REGISTER** �֐���Ăяo���܂��B����ɂ��A�}�N�� �R�}���h�̖��O����҂���_�C�A���O �{�b�N�X�ɃR�}���h�����͂��ꂽ�Ƃ��ɁA���̃R�}���h��F�����邽�߂� Excel ���K�v�Ƃ����񂪒񋟂���܂��B 
    
- DLL �� XLL �ɕϊ����āAC API �� **xlfRegister** �֐���g�p���ăR�}���h��o�^���܂��B 
    
DLL �֐��Ɋւ��đO�q�����悤�ɁA4 �Ԗڂ̃A�v���[�`���ł���Ȋ����I�ł���A�o�^�̃R�[�h��R�}���h�̃R�[�h�ɋ߂Â����܂��B�����s���ɂ́ADLL �� XLL �ɕϊ����A���̌��ʂ̃A�h�C����A�h�C�� �}�l�[�W���[�Ń��[�h����K�v������܂��B���̕��@�ŃR�}���h��o�^����ƁA�R�}���h����[�U�[ �C���^�[�t�F�C�X�̗v�f�ɉ����邱�Ƃ�ł��܂� (�J�X�^�� ���j���[�Ȃ�)�B�܂��A����̃L�[�{�[�h����Ȃǂ̃C�x���g�ŃR�}���h��Ăяo���C�x���g �g���b�v��ݒ肷�邱�Ƃ�ł��܂��B
  
Exce �ɓo�^���ꂽ���ׂĂ� XLL �R�}���h�ɂ��āAExcel �ł́A���̌`���ɂȂ��Ă���ƌ��Ȃ���܂��B
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> [!����] Excel �͖߂�l�𖳎����܂��B�������AXLM �}�N�� �V�[�g����Ăяo���ꂽ��̂�����܂� (���̏ꍇ�A�߂�l�� **TRUE** �܂��� **FALSE** �ɕϊ�����܂�)�B���̂��߁A�R�}���h������Ɏ��s���ꂽ�ꍇ�� 1 ��Ԃ��K�v������܂��B�܂��A�R�}���h�����s������A���[�U�[�ɂ���Ď������ꂽ�肵���ꍇ�� 0 ��Ԃ��K�v������܂��B 
  
## <a name="dll-memory-and-multiple-dll-instances"></a>DLL のメモリと複数の DLL インスタンス

�A�v���P�[�V������ DLL ����[�h����ƁADLL �̎��s�\�R�[�h���O���[�o�� �q�[�v�Ƀ��[�h����āA���̃R�[�h�����s�ł���悤�ɂȂ�܂��B���̂Ƃ��A���̃R�[�h�̃f�[�^�\���̗p�̗̈悪�O���[�o�� �q�[�v�Ɋ��蓖�Ă��܂��BWindows �́A������ �}�b�s���O��g�p���āA���̃������̗̈��A�v���P�[�V�����̃v���Z�X�ł��邩�̂悤�Ɋm�ۂ��邽�߁A�A�v���P�[�V�����́A���̗̈�ɃA�N�Z�X�ł���悤�ɂȂ�܂��B
  
���̌�A2 �Ԗڂ̃A�v���P�[�V������ DLL ����[�h���Ă�AWindows �� DLL �̎��s�\�R�[�h�̃R�s�[��ʂɍ쐬���邱�Ƃ͂���܂��� (���̃������͓ǂݎ���p�ɂȂ��Ă��邽��)�BWindows �́ADLL �̎��s�\�R�[�h�̃������𗼕��̃A�v���P�[�V�����̃v���Z�X�Ƀ}�b�s���O���܂��B�������ADLL �̃f�[�^�\���̂̃v���C�x�[�g �R�s�[�p�� 2 �Ԗڂ̗̈悪���蓖�Ă��A���̃R�s�[�� 2 �Ԗڂ̃v���Z�X��p�Ƀ}�b�s���O����܂��B����ɂ��A�ǂ���̃A�v���P�[�V��������݂� DLL �f�[�^�Ɋ����Ȃ��悤�ɂ��܂��B
  
���̂��߁ADLL �J���҂́A�ÓI�ϐ���O���[�o���ϐ��A�f�[�^�\���̂������̃A�v���P�[�V��������A�N�Z�X���ꂽ��A�����A�v���P�[�V�����̕����̃C���X�^���X����A�N�Z�X���ꂽ�肷�邱�Ƃɂ��ĐS�z����K�v���Ȃ��Ȃ�܂��B���ׂẴA�v���P�[�V�����̊e�C���X�^���X�́A���ꂼ��ɐ�p�� DLL �f�[�^�̃R�s�[��m�ۂ��܂��B
  
DLL �J���҂́A�A�v���P�[�V�����̓����C���X�^���X���A���̃C���X�^���X��p�� DLL ��ʂ̃X���b�h���牽���Ăяo�����Ƃɂ��Ĕz������K�v������܂��B���̏ꍇ�́A���̃C���X�^���X�̃f�[�^�ɋ�������������\��������܂��B�ڍׂɂ��ẮA�u[Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B
  
## <a name="see-also"></a>�֘A����

- [DLL ��J������](developing-dlls.md) 
- [DLL �܂��� XLL ���� Excel �ɌĂяo��](calling-into-excel-from-the-dll-or-xll.md)

