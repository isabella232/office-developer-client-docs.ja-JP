---
title: DLL ��J������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dlls [excel 2007], creating,creating DLLs [Excel 2007]
localization_priority: Normal
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 030cdd4358d9a71841eca6acfcef6e71839e02a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798792"
---
# <a name="developing-dlls"></a>DLL ��J������

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���C�u�����Ƃ́A���s�\�A�v���P�[�V�����ɂ������̋@�\��f�[�^��񋟂���R���p�C���ς݃R�[�h�̏W���ł��B���C�u�����͐ÓI�܂��͓��I�Ƀ����N�����邱�Ƃ��\�ŁA�]���A�t�@�C�����̊g���q�͂��ꂼ�� .lib ����� .dll �ƂȂ��Ă��܂��B�ÓI���C�u���� (C �����^�C�� ���C�u�����Ȃ�) �̓R���p�C�����ɃA�v���P�[�V�����Ƀ����N����A���ʓI�Ɏ��s�\�v���O�����̈ꕔ�ƂȂ�܂��B�A�v���P�[�V�����́A�K�v�ȂƂ� (�ʏ�́A�A�v���P�[�V�����̋N����) �� DLL ��ǂݍ��݂܂��BDLL �́A�ʂ� DLL ��ǂݍ��ݓ��I�Ƀ����N�ł��܂��B
  
## <a name="benefits-of-using-dlls"></a>Dll を使用する利点

DLL �̎�ȗ��_�͎��̂Ƃ���ł��B
  
- ���ׂẴA�v���P�[�V�������A�f�B�X�N��̒P��R�s�[����L�ł��܂��B
    
- �A�v���P�[�V�����̎��s�\�t�@�C������K�͂Ȃ�̂ɂł��܂��B
    
- ��K�͂ȊJ���v���W�F�N�g��ו����ł��܂��B�A�v���P�[�V������ DLL �̊J���҂����ӂ���K�v������̂́A���ꂼ��̕����Ԃ̃C���^�[�t�F�C�X�݂̂ɂȂ�܂��B���̃C���^�[�t�F�C�X�́ADLL �ɂ���ăG�N�X�|�[�g����܂��B
    
- DLL �̊J���҂� DLL ��X�V�ł��܂��B�����̏ꍇ�A���̖ړI�͌���������コ������A�o�O��C�������肷�邱�Ƃɂ���܂��BDLL �̃G�N�X�|�[�g���ꂽ�C���^�[�t�F�C�X��ύX���Ȃ��ꍇ�ɂ́ADLL ��g�p���Ă��邷�ׂẴA�v���P�[�V������X�V����K�v�͂���܂���B
    
DLL ��g�p����ƁAMicrosoft Excel �Ƀ��[�N�V�[�g�֐��ƃR�}���h��ǉ��ł��܂��B
  
## <a name="resources-for-creating-dlls"></a>Dll を作成するためのリソース

DLL ��쐬����ɂ́A�ȉ����K�v�ƂȂ�܂��B
  
- �\�[�X �R�[�h �G�f�B�^�[�B
    
- �\�[�X �R�[�h��A�g�p���Ă���n�[�h�E�F�A�ƌ݊����̂���I�u�W�F�N�g �R�[�h�ɕϊ�����R���p�C���B
    
- �g�p���Ă���ꍇ�ɐÓI���C�u��������R�[�h��ǉ�������A���s�\ DLL �t�@�C����쐬�����肷�邽�߂̃����J�[�B
    
Microsoft Visual Studio �Ȃǂ̍ŐV�̓����J���� (IDE) �ɂ́A����炷�ׂĂ�������Ă��܂��B�܂��A����ɑ����̂�́A�܂�X�}�[�g �G�f�B�^�[�A�R�[�h��f�o�b�O���邽�߂̃c�[���A�����̃v���W�F�N�g��Ǘ����邽�߂̃c�[���A�V�����v���W�F�N�g �E�B�U�[�h�A����ё��̏d�v�ȑ����̃c�[�������܂��B
  
DLL �́AC/C++�APascal�AVisual Basic �Ȃǂ������̌���ō쐬�ł��܂��BExcel �ɗp�ӂ���Ă��� API �̃\�[�X �R�[�h�� C ����� C++ �ł��邱�Ƃ���A���̎����ł͂���� 2 �̌���ɂ��Ă̂ݎ��グ�܂��B
  
## <a name="exporting-functions-and-commands"></a>関数とコマンドをエクスポートします。

DLL �v���W�F�N�g��R���p�C������Ƃ��A�R���p�C���ƃ����J�[�́A�G�N�X�|�[�g�Ώۂ̊֐���c�����ăA�v���P�[�V�������g�p�ł���悤�ɂ���K�v������܂��B���̃Z�N�V�����ł́A���̂��߂̕��@�ɂ��Đ�����܂��B
  
�R���p�C�����\�[�X �R�[�h��R���p�C������Ƃ��A�ʏ�A�R���p�C���͊֐��̖��O��A�\�[�X �R�[�h�Ŏ�����Ă��閼�O����ύX���܂��B�����̏ꍇ�A���̂��߂ɂ͖��O�̐擪�܂��͖����ɒǉ�����܂��B���̃v���Z�X�́A���O�f�R���[�g�ƌĂ΂�܂��B�֐����ADLL ��ǂݍ��ރA�v���P�[�V�����ŔF���\�Ȗ��O�ŃG�N�X�|�[�g����邱�Ƃ�m�F����K�v������܂��B�܂�A�f�R���[�g���ꂽ���O�ƊȒP�ȃG�N�X�|�[�g����֘A�t����悤�Ƀ����J�[�Ɏw�����܂��B�G�N�X�|�[�g���́A�\�[�X �R�[�h�Ɏ�����Ă��錳�̖��O�ɂ��邱�Ƃ�A���̖��O�ɂ��邱�Ƃ�ł��܂��B
  
���O��f�R���[�g������@�́A����A����уR���p�C���Ɏw������Ă���֐���g�p�ł���悤�ɂ�����@�A�܂��Ăяo���K���ɂ���ĈقȂ�܂��BDLL ���g�p���� Windows �W���̃v���Z�X�ԌĂяo���K��́AWinAPI �K��ƌĂ΂�Ă��܂��B����́AWindows �w�b�_�[ �t�@�C���� **WINAPI** �Ƃ��Ē�**** ����܂��B
  
(かどうかは、ワークシート関数、マクロ シートと同じ関数、またはユーザー定義のコマンド) を Excel で使用する DLL のエクスポート関数は、**はい**常に使用する必要があります / **_ _stdcall**呼び出し規約です。 Win32 コンパイラの既定の設定は、呼び出し規約が指定されていない場合に**WINAPIV**、としても定義されて、 **_ _cdecl**を使用すると関数の定義で明示的に**はい**指定子を含める必要があります。
  
�����J�[�ɑ΂��āA�֐����G�N�X�|�[�g����邱�ƁA���O�����̕��@�̂����ꂩ�ɂ���ĊO���ŔF������邱�Ƃ�ʒm�ł��܂��B
  
- �Ώۂ̊֐���ADEF �t�@�C���� **EXPORTS** �L�[���[�h�̌�ɔz�u���A�����N���ɂ��̃t�@�C����Q�Ƃ���悤 DLL �v���W�F�N�g�ݒ��s���܂��B 
    
- �֐��̒�`�� **__declspec(dllexport)** �錾�q��g�p���܂��B 
    
- **#pragma** �v���v���Z�b�T �f�B���N�e�B�u��g�p���āA�����J�[�Ƀ��b�Z�[�W�𑗐M���܂��B 
    
プロジェクトで使用できるすべての 3 つの方法であり、コンパイラとリンカーをサポートして、ください 1 つの方法は、次のいずれかの複数の関数をエクスポートするのには。 たとえば、2 つのソース コード モジュール、1 つ C および C++ では、エクスポートする 2 つの関数を含む、DLL が含まれている **、\_C\_エクスポート**と **、\_Cpp\_エクスポート**それぞれ。 わかりやすくするため、各関数は 1 つの倍精度数値の引数を受け取るし、同じデータ型を返すとします。 次のセクションでは、これらの各メソッドを使用して各関数をエクスポートするための選択肢が記載されています。 
  
### <a name="using-a-def-file"></a>DEF ファイルを使用します。

```C
double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

```cpp
double WINAPI my_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<br/>

DEF �t�@�C���ɂ́A���̍s��܂߂�K�v������܂��B
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

**EXPORTS** �X�e�[�g�����g�̌�̍s�̈�ʓI�ȍ\���́A���̂悤�ɂȂ�܂��B 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

C �֐��̓f�R���[�g����܂����ADEF �t�@�C���̓����J�[�ɑ΂��āA(���̗�̏ꍇ) ���̃\�[�X �R�[�h����g�p���Ċ֐�����J���邱�Ƃ𖾎��I�ɋ�������_�ɒ��ڂ��Ă��������B�����J�[�͌��̃R�[�h����g�p���� C++ �֐���ÖٓI�ɃG�N�X�|�[�g����̂ŁADEF �t�@�C���Ƀf�R���[�g���ꂽ���O��܂߂�K�v�͂���܂���B
  
32 �r�b�g�� Windows API �֐��Ăяo���̏ꍇ�AC �R���p�C���֐��̃f�R���[�g�̋K��͎��̂悤�ɂȂ�܂��B **function_name** �� _ **function_name@** _n_ �ɂȂ�܂��B�����ŁA  _n_ �́A���ׂĂ̈����Ŏ���� 10 �i�̃o�C�g���ł��B�e�o�C�g���́A�ł�߂� 4 �̔{���ɐ؂�グ���܂��B 
  
> [!NOTE]
> [!����] Win32 �ł́A���ׂẴ|�C���^�[�� 4 �o�C�g�P�ʂł��B�߂�l�̌^�́A���O�f�R���[�g�ɉe����^���܂���B 
  
C++ �R���p�C���ɑ΂��āAC++ �֐��̃f�R���[�g����Ă��Ȃ����O����J����悤�ɋ������邱�Ƃ��ł��܂��B���̏ꍇ�ɂ́A���̗�Ɏ�����Ă���悤�ɁAextern"C"{...} �u���b�N��Ɋ֐�����ъ֐��v���g�^�C�v�����܂��B(�����ł͒������� **{}** �͏ȗ�����Ă��܂��B�錾���Q�Ƃ���̂́A����̊֐��R�[�h �u���b�N�݂̂�����ł�)�B 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

C �܂��� C++ �\�[�X �t�@�C���Ɋ܂߂邱�Ƃ��ł���w�b�_�[ �t�@�C���� C �֐��v���g�^�C�v��z�u����ꍇ�A���̃v���v���Z�b�T �f�B���N�e�B�u��܂߂�K�v������܂��B
  
```cpp
#ifdef __cplusplus
extern "C" {
#endif
double WINAPI my_C_export(double x);
double WINAPI my_Cdecorated_Cpp_export(double x);
#ifdef __cplusplus
}
#endif
```

### <a name="using-the-declspecdllexport-declarator"></a>関数宣言子を使用します。

**__declspec(dllexport)** �L�[���[�h��A���̂悤�Ɋ֐��̐錾�Ŏg�p�ł��܂��B 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

宣言の極端な左の**方式**を追加する必要があります。 このアプローチの利点は、関数が定義ファイルに登録する必要がないことは、エクスポートの状態の定義を使用して右です。 
  
C++ �֐��� C++ ���O�f�R���[�g�ɂ���Ďg�p�\�ɂȂ�̂������ꍇ�ɂ́A���̂悤�Ɋ֐���錾���Ȃ���΂Ȃ�܂���B
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

�����J�[�͂��̊֐��� my_undecorated_Cpp_export �Ƃ��Ďg�p�ł���悤�ɂ��܂��B�܂�A�f�R���[�g�Ȃ��ŁA�\�[�X �R�[�h�Ŏ�����Ă���܂܂̖��O�ɂȂ�܂��B
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a>リンカーのプリプロセッサ ディレクティブ #pragma を使用してください。

最近のバージョンの Microsoft Visual Studio は、2 つの定義済みマクロをサポートするには、 **#pragma**ディレクティブと組み合わせて使用する場合を使用すると、関数のコード内から直接関数をエクスポートするようにリンカーに指示します。 マクロは、__関数__および__FUNCDNAME__ (二重下線の各端点に注意してください) は、装飾されていないと、装飾された関数名をそれぞれ展開。 
  
���Ƃ��΁AMicrosoft Visual Studio ��g�p���Ă���ꍇ�A�����̍s����̂悤�ɋ��ʃw�b�_�[ �t�@�C���ɑg�ݍ��ނ��Ƃ��ł��܂��B
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

���̃w�b�_�[���\�[�X �t�@�C���Ɋ܂܂�Ă���ƁA2 �̊֐������̂悤�ɃG�N�X�|�[�g�ł��܂��B
  
C �R�[�h:
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

C++ �R�[�h:
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

���̃f�B���N�e�B�u�́A�֐��̖{�̓�ɔz�u����K�v������A�R���p�C�� �I�v�V���� **/EP** �܂��� **/P** ���ݒ肳��Ă��Ȃ��ꍇ�ɂ̂݊g������܂��B���̎�@��g�p����ƁADEF �t�@�C���܂��� **__declspec(dllexport)** �錾���K�v�Ȃ��Ȃ�A�֐��R�[�h�ŃG�N�X�|�[�g��Ԃ̎d�l��ێ��ł��܂��B 
  
## <a name="see-also"></a>�֘A����

- [Excel での Dll のアクセス](how-to-access-dlls-in-excel.md)
- [DLL �܂��� XLL ���� Excel �ɌĂяo��](calling-into-excel-from-the-dll-or-xll.md)
- [Excel �v���O���~���O�̊T�O](excel-programming-concepts.md)
- [Excel XLL �̊J��](developing-excel-xlls.md)

