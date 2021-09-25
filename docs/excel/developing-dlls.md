---
title: DLL の開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dlls [excel 2007], creating,creating DLLs [Excel 2007]
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.localizationpriority: high
ms.openlocfilehash: 365095dfaf1528663a358f69ad632b990f9ea1ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605611"
---
# <a name="developing-dlls"></a>DLL の開発

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
���C�u�����Ƃ́A���s�\�A�v���P�[�V�����ɂ������̋@�\��f�[�^��񋟂���R���p�C���ς݃R�[�h�̏W���ł��B���C�u�����͐ÓI�܂��͓��I�Ƀ����N�����邱�Ƃ��\�ŁA�]���A�t�@�C�����̊g���q�͂��ꂼ�� .lib ����� .dll �ƂȂ��Ă��܂��B�ÓI���C�u���� (C �����^�C�� ���C�u�����Ȃ�) �̓R���p�C�����ɃA�v���P�[�V�����Ƀ����N����A���ʓI�Ɏ��s�\�v���O�����̈ꕔ�ƂȂ�܂��B�A�v���P�[�V�����́A�K�v�ȂƂ� (�ʏ�́A�A�v���P�[�V�����̋N����) �� DLL ��ǂݍ��݂܂��BDLL �́A�ʂ� DLL ��ǂݍ��ݓ��I�Ƀ����N�ł��܂��B
  
## <a name="benefits-of-using-dlls"></a>DLL を使用する利点

DLL の主な利点は次のとおりです。
  
- すべてのアプリケーションが、ディスク上の単一コピーを共有できます。
    
- �A�v���P�[�V�����̎��s�\�t�@�C������K�͂Ȃ�̂ɂł��܂��B
    
- ��K�͂ȊJ���v���W�F�N�g��ו����ł��܂��B�A�v���P�[�V������ DLL �̊J���҂����ӂ���K�v������̂́A���ꂼ��̕����Ԃ̃C���^�[�t�F�C�X�݂̂ɂȂ�܂��B���̃C���^�[�t�F�C�X�́ADLL �ɂ���ăG�N�X�|�[�g����܂��B
    
- DLL の開発者は DLL を更新できます。多くの場合、その目的は効率性を向上させたり、バグを修正したりすることにあります。DLL のエクスポートされたインターフェイスを変更しない場合には、DLL を使用しているすべてのアプリケーションを更新する必要はありません。
    
DLL を使用すると、Microsoft Excel にワークシート関数とコマンドを追加できます。
  
## <a name="resources-for-creating-dlls"></a>DLL を作成するためのリソース

DLL を作成するには次のものが必要です。
  
- ソース コード エディター。
    
- ソース コードを、使用しているハードウェアと互換性のあるオブジェクト コードに変換するコンパイラ。
    
- 使用している場合に静的ライブラリからコードを追加したり、実行可能 DLL ファイルを作成したりするためのリンカー。
    
Microsoft Visual Studio �Ȃǂ̍ŐV�̓����J���� (IDE) �ɂ́A����炷�ׂĂ�������Ă��܂��B�܂��A����ɑ����̂�́A�܂�X�}�[�g �G�f�B�^�[�A�R�[�h��f�o�b�O���邽�߂̃c�[���A�����̃v���W�F�N�g��Ǘ����邽�߂̃c�[���A�V�����v���W�F�N�g �E�B�U�[�h�A����ё��̏d�v�ȑ����̃c�[�������܂��B
  
DLL �́AC/C++�APascal�AVisual Basic �Ȃǂ������̌���ō쐬�ł��܂��BExcel �ɗp�ӂ���Ă��� API �̃\�[�X �R�[�h�� C ����� C++ �ł��邱�Ƃ���A���̎����ł͂���� 2 �̌���ɂ��Ă̂ݎ��グ�܂��B
  
## <a name="exporting-functions-and-commands"></a>関数とコマンドのエクスポート

DLL �v���W�F�N�g��R���p�C������Ƃ��A�R���p�C���ƃ����J�[�́A�G�N�X�|�[�g�Ώۂ̊���c�����ăA�v���P�[�V�������g�p�ł���悤�ɂ���K�v������܂��B���̃Z�N�V�����ł́A���̂��߂̕��@�ɂ��Đ�����܂��B
  
�R���p�C�����\�[�X �R�[�h��R���p�C������Ƃ��A�ʏ�A�R���p�C���͊��̖��O��A�\�[�X �R�[�h�Ŏ�����Ă��閼�O����ύX���܂��B�����̏ꍇ�A���̂��߂ɂ͖��O�̐擪�܂��͖����ɒǉ�����܂��B���̃v���Z�X�́A���O�f�R���[�g�ƌĂ�܂��B�����ADLL ��ǂݍ��ރA�v���P�[�V�����ŔF���\�Ȗ��O�ŃG�N�X�|�[�g����邱�Ƃ�m�F����K�v������܂��B�܂�A�f�R���[�g���ꂽ���O�ƊȒP�ȃG�N�X�|�[�g����֘A�t����悤�Ƀ����J�[�Ɏw�����܂��B�G�N�X�|�[�g���́A�\�[�X �R�[�h�Ɏ�����Ă��錳�̖��O�ɂ��邱�Ƃ�A���̖��O�ɂ��邱�Ƃ�ł��܂��B
  
���O��f�R���[�g������@�́A����A����уR���p�C���Ɏw������Ă������g�p�ł���悤�ɂ�����@�A�܂��Ăяo���K���ɂ���ĈقȂ�܂��BDLL ���g�p���� Windows �W���̃v���Z�X�ԌĂяo���K��́AWinAPI �K��ƌĂ�Ă��܂��B����́AWindows �w�b�_�[ �t�@�C���� **WINAPI** �Ƃ��Ē�����܂��B
  
A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention. It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.
  
リンカーに対して、関数がエクスポートされること、名前が次の方法のいずれかによって外部で認識されることを通知できます。
  
- �Ώۂ̊���ADEF �t�@�C���� **EXPORTS** �L�[���[�h�̌�ɔz�u���A�����N���ɂ��̃t�@�C����Q�Ƃ���悤 DLL �v���W�F�N�g�ݒ��s���܂��B 
    
- ���̒�`�� **__declspec(dllexport)** �錾�q��g�p���܂��B 
    
- **#pragma** �v���v���Z�b�T �f�B���N�e�B�u��g�p���āA�����J�[�Ƀ��b�Z�[�W�𑗐M���܂��B 
    
プロジェクトでは 3 つの方法すべてを使用できます。また、コンパイラとリンカーも 3 つの方法をサポートしていますが、これらの方法を複数使用して 1 つの関数をエクスポートしてはいけません。 たとえば、ある DLL に 2 つのソース コード モジュール、1 つの C および 1 つの C++ が含まれていて、エクスポートされる **my\_C\_export** と **my\_Cpp\_export** という 2 つの関数がそれぞれに含まれているとします。 わかりやすくするため、各関数は 1 つの倍精度数値引数を取り、同じデータ型を返すことにします。 次のセクションでは、これらの各メソッドを使用してそれぞれの関数をエクスポートする方法の、代替方法について説明します。 
  
### <a name="using-a-def-file"></a>DEF ファイルの使用

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

DEF ファイルには、次の行を含める必要があります。
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

**EXPORTS** �X�e�[�g�����g�̌�̍s�̈�ʓI�ȍ\���́A���̂悤�ɂȂ�܂��B 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

C ���̓f�R���[�g����܂����ADEF �t�@�C���̓����J�[�ɑ��āA(���̗�̏ꍇ) ���̃\�[�X �R�[�h����g�p���Ċ�����J���邱�Ƃ𖾎��I�ɋ�������_�ɒ��ڂ��Ă��������B�����J�[�͌��̃R�[�h����g�p���� C++ ����ÖٓI�ɃG�N�X�|�[�g����̂ŁADEF �t�@�C���Ƀf�R���[�g���ꂽ���O��܂߂�K�v�͂���܂���B
  
32 �r�b�g�� Windows API ���Ăяo���̏ꍇ�AC �R���p�C�����̃f�R���[�g�̋K��͎��̂悤�ɂȂ�܂��B **function_name** �� _ **function_name@** _n_ �ɂȂ�܂��B�����ŁA  _n_ �́A���ׂĂ̈����Ŏ���� 10 �i�̃o�C�g���ł��B�e�o�C�g���́A�ł�߂� 4 �̔{���ɐ؂�グ���܂��B 
  
> [!NOTE]
> [!����] Win32 �ł́A���ׂẴ|�C���^�[�� 4 �o�C�g�P�ʂł��B�߂�l�̌^�́A���O�f�R���[�g�ɉe����^���܂���B 
  
C++ �R���p�C���ɑ��āAC++ ���̃f�R���[�g����Ă��Ȃ����O����J����悤�ɋ������邱�Ƃ��ł��܂��B���̏ꍇ�ɂ́A���̗�Ɏ�����Ă���悤�ɁAextern"C"{...} �u���b�N��Ɋ�����ъ��v���g�^�C�v�����܂��B(�����ł͒������� **{}** �͏ȗ�����Ă��܂��B�錾���Q�Ƃ���̂́A����̊��R�[�h �u���b�N�݂̂�����ł�)�B 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

C または C++ ソース ファイルに含めることができるヘッダー ファイルに C 関数プロトタイプを配置する場合、次のプリプロセッサ ディレクティブを含める必要があります。
  
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

### <a name="using-the-__declspecdllexport-declarator"></a>__declspec(dllexport) 宣言子の使用

次に示すように、**__declspec(dllexport)** キーワードを関数の宣言で使用できます。 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

**__declspec(dllexport)** キーワードは、宣言の左端に追加する必要があります。このアプローチの利点は、関数を DEF ファイルにリストする必要がないこと、エクスポートの状態が定義どおりになることです。 
  
C++ 関数が C++ 名前デコレートによって使用可能になるのを回避する場合には、次のように関数を宣言しなければなりません。
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

リンカーはこの関数を my_undecorated_Cpp_export として使用できるようにします。つまり、デコレートなしで、ソース コードで示されているままの名前になります。
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a>#pragma プリプロセッサ リンカー ディレクティブの使用

Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code. The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively. 
  
たとえば、Microsoft Visual Studio を使用している場合、これらの行を次のように共通ヘッダー ファイルに組み込むことができます。
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

このヘッダーがソース ファイルに含まれていると、2 つの関数例を次のようにエクスポートできます。
  
C コード:
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

C++ コード:
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

���̃f�B���N�e�B�u�́A���̖{�̓�ɔz�u����K�v������A�R���p�C�� �I�v�V���� **/EP** �܂��� **/P** ���ݒ肳��Ă��Ȃ��ꍇ�ɂ̂݊g������܂��B���̎�@��g�p����ƁADEF �t�@�C���܂��� **__declspec(dllexport)** �錾���K�v�Ȃ��Ȃ�A���R�[�h�ŃG�N�X�|�[�g��Ԃ̎d�l��ێ��ł��܂��B 
  
## <a name="see-also"></a>関連項目

- [Excel で DLL にアクセスする](how-to-access-dlls-in-excel.md)
- [DLL または XLL から Excel に呼び出す](calling-into-excel-from-the-dll-or-xll.md)
- [Excel プログラミングの概念](excel-programming-concepts.md)
- [Excel XLL の開発](developing-excel-xlls.md)

