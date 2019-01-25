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
localization_priority: Priority
ms.openlocfilehash: 89dd7b65ad94ba2fc7e1cf3f99ee163d3003d0fe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704750"
---
# <a name="developing-dlls"></a><span data-ttu-id="61757-104">DLL の開発</span><span class="sxs-lookup"><span data-stu-id="61757-104">Developing DLLs</span></span>

<span data-ttu-id="61757-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="61757-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="61757-p101">���C�u�����Ƃ́A���s�\�A�v���P�[�V�����ɂ������̋@�\��f�[�^��񋟂���R���p�C���ς݃R�[�h�̏W���ł��B���C�u�����͐ÓI�܂��͓��I�Ƀ����N�����邱�Ƃ��\�ŁA�]���A�t�@�C�����̊g���q�͂��ꂼ�� .lib ����� .dll �ƂȂ��Ă��܂��B�ÓI���C�u���� (C �����^�C�� ���C�u�����Ȃ�) �̓R���p�C�����ɃA�v���P�[�V�����Ƀ����N����A���ʓI�Ɏ��s�\�v���O�����̈ꕔ�ƂȂ�܂��B�A�v���P�[�V�����́A�K�v�ȂƂ� (�ʏ�́A�A�v���P�[�V�����̋N����) �� DLL ��ǂݍ��݂܂��BDLL �́A�ʂ� DLL ��ǂݍ��ݓ��I�Ƀ����N�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-p101">A library is a body of compiled code that provides some functionality and data to an executable application. Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively. Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable. The application loads a DLL when it is needed, usually when the application starts up. One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="61757-111">DLL を使用する利点</span><span class="sxs-lookup"><span data-stu-id="61757-111">Benefits of Using DLLs</span></span>

<span data-ttu-id="61757-112">DLL の主な利点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="61757-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="61757-113">すべてのアプリケーションが、ディスク上の単一コピーを共有できます。</span><span class="sxs-lookup"><span data-stu-id="61757-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="61757-114">�A�v���P�[�V�����̎��s�\�t�@�C������K�͂Ȃ�̂ɂł��܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="61757-p102">��K�͂ȊJ���v���W�F�N�g��ו����ł��܂��B�A�v���P�[�V������ DLL �̊J���҂����ӂ���K�v������̂́A���ꂼ��̕����Ԃ̃C���^�[�t�F�C�X�݂̂ɂȂ�܂��B���̃C���^�[�t�F�C�X�́ADLL �ɂ���ăG�N�X�|�[�g����܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-p102">They enable large development projects to be broken down. Application and DLL developers only need agree an interface between their respective parts. This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="61757-118">DLL の開発者は DLL を更新できます。多くの場合、その目的は効率性を向上させたり、バグを修正したりすることにあります。DLL のエクスポートされたインターフェイスを変更しない場合には、DLL を使用しているすべてのアプリケーションを更新する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="61757-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="61757-119">DLL を使用すると、Microsoft Excel にワークシート関数とコマンドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="61757-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="61757-120">DLL を作成するためのリソース</span><span class="sxs-lookup"><span data-stu-id="61757-120">Resources for Creating DLLs</span></span>

<span data-ttu-id="61757-121">DLL を作成するには次のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="61757-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="61757-122">ソース コード エディター。</span><span class="sxs-lookup"><span data-stu-id="61757-122">A source code editor.</span></span>
    
- <span data-ttu-id="61757-123">ソース コードを、使用しているハードウェアと互換性のあるオブジェクト コードに変換するコンパイラ。</span><span class="sxs-lookup"><span data-stu-id="61757-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="61757-124">使用している場合に静的ライブラリからコードを追加したり、実行可能 DLL ファイルを作成したりするためのリンカー。</span><span class="sxs-lookup"><span data-stu-id="61757-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="61757-p103">Microsoft Visual Studio �Ȃǂ̍ŐV�̓����J���� (IDE) �ɂ́A����炷�ׂĂ�������Ă��܂��B�܂��A����ɑ����̂�́A�܂�X�}�[�g �G�f�B�^�[�A�R�[�h��f�o�b�O���邽�߂̃c�[���A�����̃v���W�F�N�g��Ǘ����邽�߂̃c�[���A�V�����v���W�F�N�g �E�B�U�[�h�A����ё��̏d�v�ȑ����̃c�[�������܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-p103">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things. They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="61757-p104">DLL �́AC/C++�APascal�AVisual Basic �Ȃǂ������̌���ō쐬�ł��܂��BExcel �ɗp�ӂ���Ă��� API �̃\�[�X �R�[�h�� C ����� C++ �ł��邱�Ƃ���A���̎����ł͂���� 2 �̌���ɂ��Ă̂ݎ��グ�܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-p104">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic. Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="61757-129">関数とコマンドのエクスポート</span><span class="sxs-lookup"><span data-stu-id="61757-129">Exporting Functions and Commands</span></span>

<span data-ttu-id="61757-p105">DLL �v���W�F�N�g��R���p�C������Ƃ��A�R���p�C���ƃ����J�[�́A�G�N�X�|�[�g�Ώۂ̊���c�����ăA�v���P�[�V�������g�p�ł���悤�ɂ���K�v������܂��B���̃Z�N�V�����ł́A���̂��߂̕��@�ɂ��Đ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-p105">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application. This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="61757-p106">�R���p�C�����\�[�X �R�[�h��R���p�C������Ƃ��A�ʏ�A�R���p�C���͊��̖��O��A�\�[�X �R�[�h�Ŏ�����Ă��閼�O����ύX���܂��B�����̏ꍇ�A���̂��߂ɂ͖��O�̐擪�܂��͖����ɒǉ�����܂��B���̃v���Z�X�́A���O�f�R���[�g�ƌĂ�܂��B�����ADLL ��ǂݍ��ރA�v���P�[�V�����ŔF���\�Ȗ��O�ŃG�N�X�|�[�g����邱�Ƃ�m�F����K�v������܂��B�܂�A�f�R���[�g���ꂽ���O�ƊȒP�ȃG�N�X�|�[�g����֘A�t����悤�Ƀ����J�[�Ɏw�����܂��B�G�N�X�|�[�g���́A�\�[�X �R�[�h�Ɏ�����Ă��錳�̖��O�ɂ��邱�Ƃ�A���̖��O�ɂ��邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-p106">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code. They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration. You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL. This can mean telling the linker to associate the decorated name with a simpler export name. The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="61757-p107">���O��f�R���[�g������@�́A����A����уR���p�C���Ɏw������Ă������g�p�ł���悤�ɂ�����@�A�܂��Ăяo���K���ɂ���ĈقȂ�܂��BDLL ���g�p���� Windows �W���̃v���Z�X�ԌĂяo���K��́AWinAPI �K��ƌĂ�Ă��܂��B����́AWindows �w�b�_�[ �t�@�C���� **WINAPI** �Ƃ��Ē�\*\*\*\* ����܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-p107">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention. The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention. It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="61757-140">Excel で使用する DLL エクスポート関数 (ワークシート関数、マクロシート同等関数、ユーザー定義コマンドのいずれの場合であっても) は、必ず **WINAPI** / **__stdcall** 呼び出し規則を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61757-140">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention.</span></span> <span data-ttu-id="61757-141">Win32 コンパイラの既定として **__cdecl** 呼び出し規則を使用するには、関数の定義に **WINAPI** 指定子を明示的に含める必要があります。何も指定しない場合は **WINAPIV** として定義されます。</span><span class="sxs-lookup"><span data-stu-id="61757-141">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention. It is necessary to include the **WINAPI** specifier explicitly in the function’s definition as the default in Win32 compilers is to use the __cdecl calling convention, also defined as WINAPIV, if none is specified.</span></span>
  
<span data-ttu-id="61757-142">リンカーに対して、関数がエクスポートされること、名前が次の方法のいずれかによって外部で認識されることを通知できます。</span><span class="sxs-lookup"><span data-stu-id="61757-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="61757-143">�Ώۂ̊���ADEF �t�@�C���� **EXPORTS** �L�[���[�h�̌�ɔz�u���A�����N���ɂ��̃t�@�C����Q�Ƃ���悤 DLL �v���W�F�N�g�ݒ��s���܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="61757-144">���̒�\`�� **__declspec(dllexport)** �錾�q��g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="61757-145">**#pragma** �v���v���Z�b�T �f�B���N�e�B�u��g�p���āA�����J�[�Ƀ��b�Z�[�W�𑗐M���܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="61757-146">プロジェクトでは 3 つの方法すべてを使用できます。また、コンパイラとリンカーも 3 つの方法をサポートしていますが、これらの方法を複数使用して 1 つの関数をエクスポートしてはいけません。</span><span class="sxs-lookup"><span data-stu-id="61757-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="61757-147">たとえば、ある DLL に 2 つのソース コード モジュール、1 つの C および 1 つの C++ が含まれていて、エクスポートされる **my\_C\_export** と **my\_Cpp\_export** という 2 つの関数がそれぞれに含まれているとします。</span><span class="sxs-lookup"><span data-stu-id="61757-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="61757-148">わかりやすくするため、各関数は 1 つの倍精度数値引数を取り、同じデータ型を返すことにします。</span><span class="sxs-lookup"><span data-stu-id="61757-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="61757-149">次のセクションでは、これらの各メソッドを使用してそれぞれの関数をエクスポートする方法の、代替方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="61757-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="61757-150">DEF ファイルの使用</span><span class="sxs-lookup"><span data-stu-id="61757-150">Using a DEF File</span></span>

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

<span data-ttu-id="61757-151">DEF ファイルには、次の行を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="61757-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="61757-152">**EXPORTS** �X�e�[�g�����g�̌�̍s�̈�ʓI�ȍ\���́A���̂悤�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="61757-p110">C ���̓f�R���[�g����܂����ADEF �t�@�C���̓����J�[�ɑ��āA(���̗�̏ꍇ) ���̃\�[�X �R�[�h����g�p���Ċ�����J���邱�Ƃ𖾎��I�ɋ�������_�ɒ��ڂ��Ă��������B�����J�[�͌��̃R�[�h����g�p���� C++ ����ÖٓI�ɃG�N�X�|�[�g����̂ŁADEF �t�@�C���Ƀf�R���[�g���ꂽ���O��܂߂�K�v�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="61757-p110">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example). The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="61757-155">32 �r�b�g�� Windows API ���Ăяo���̏ꍇ�AC �R���p�C�����̃f�R���[�g�̋K��͎��̂悤�ɂȂ�܂��B **function_name** �� _ **function_name@** _n_ �ɂȂ�܂��B�����ŁA  _n_ �́A���ׂĂ̈����Ŏ���� 10 �i�̃o�C�g���ł��B�e�o�C�g���́A�ł�߂� 4 �̔{���ɐ؂�グ���܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="61757-p111">[!����] Win32 �ł́A���ׂẴ|�C���^�[�� 4 �o�C�g�P�ʂł��B�߂�l�̌^�́A���O�f�R���[�g�ɉe����^���܂���B</span><span class="sxs-lookup"><span data-stu-id="61757-p111">All pointers are four bytes wide in Win32. The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="61757-p112">C++ �R���p�C���ɑ��āAC++ ���̃f�R���[�g����Ă��Ȃ����O����J����悤�ɋ������邱�Ƃ��ł��܂��B���̏ꍇ�ɂ́A���̗�Ɏ�����Ă���悤�ɁAextern"C"{...} �u���b�N��Ɋ�����ъ��v���g�^�C�v�����܂��B(�����ł͒������� **{}** �͏ȗ�����Ă��܂��B�錾���Q�Ƃ���̂́A����̊��R�[�h �u���b�N�݂̂�����ł�)�B</span><span class="sxs-lookup"><span data-stu-id="61757-p112">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…} block, as shown in this example. (The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="61757-161">C または C++ ソース ファイルに含めることができるヘッダー ファイルに C 関数プロトタイプを配置する場合、次のプリプロセッサ ディレクティブを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="61757-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
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

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="61757-162">__declspec(dllexport) 宣言子の使用</span><span class="sxs-lookup"><span data-stu-id="61757-162">Using the __declspec(dllexport) Declarator</span></span>

<span data-ttu-id="61757-163">次に示すように、**__declspec(dllexport)** キーワードを関数の宣言で使用できます。</span><span class="sxs-lookup"><span data-stu-id="61757-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="61757-p113">**__declspec(dllexport)** キーワードは、宣言の左端に追加する必要があります。このアプローチの利点は、関数を DEF ファイルにリストする必要がないこと、エクスポートの状態が定義どおりになることです。</span><span class="sxs-lookup"><span data-stu-id="61757-p113">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration. The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="61757-166">C++ 関数が C++ 名前デコレートによって使用可能になるのを回避する場合には、次のように関数を宣言しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="61757-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="61757-167">リンカーはこの関数を my_undecorated_Cpp_export として使用できるようにします。つまり、デコレートなしで、ソース コードで示されているままの名前になります。</span><span class="sxs-lookup"><span data-stu-id="61757-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="61757-168">#pragma プリプロセッサ リンカー ディレクティブの使用</span><span class="sxs-lookup"><span data-stu-id="61757-168">Using a #pragma Preprocessor Linker Directive</span></span>

<span data-ttu-id="61757-169">Microsoft Visual Studio の最近のバージョンでは、**#pragma** ディレクティブと一緒に使用する、2 つの事前定義されたマクロをサポートしています。リンカーに対して、関数コードから直接関数をエクスポートするように指示できます。</span><span class="sxs-lookup"><span data-stu-id="61757-169">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code. The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> <span data-ttu-id="61757-170">__FUNCTION__ と __FUNCDNAME__ (それぞれの末尾はアンダースコア 2 つで構成されています) というマクロは、それぞれデコレートされない関数名とデコレートされた関数名に拡張されます。</span><span class="sxs-lookup"><span data-stu-id="61757-170">The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="61757-171">たとえば、Microsoft Visual Studio を使用している場合、これらの行を次のように共通ヘッダー ファイルに組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="61757-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="61757-172">このヘッダーがソース ファイルに含まれていると、2 つの関数例を次のようにエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="61757-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="61757-173">C コード:</span><span class="sxs-lookup"><span data-stu-id="61757-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="61757-174">C++ コード:</span><span class="sxs-lookup"><span data-stu-id="61757-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="61757-p115">���̃f�B���N�e�B�u�́A���̖{�̓�ɔz�u����K�v������A�R���p�C�� �I�v�V���� **/EP** �܂��� **/P** ���ݒ肳��Ă��Ȃ��ꍇ�ɂ̂݊g������܂��B���̎�@��g�p����ƁADEF �t�@�C���܂��� **__declspec(dllexport)** �錾���K�v�Ȃ��Ȃ�A���R�[�h�ŃG�N�X�|�[�g��Ԃ̎d�l��ێ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="61757-p115">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set. This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61757-177">関連項目</span><span class="sxs-lookup"><span data-stu-id="61757-177">See also</span></span>

- [<span data-ttu-id="61757-178">Excel で DLL にアクセスする</span><span class="sxs-lookup"><span data-stu-id="61757-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="61757-179">DLL または XLL から Excel に呼び出す</span><span class="sxs-lookup"><span data-stu-id="61757-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="61757-180">Excel プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="61757-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="61757-181">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="61757-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

