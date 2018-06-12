---
title: 下位互換性
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- version compatibility [excel 2007],XLL compatibility [Excel 2007],backward compatibility [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 095961fa909a67b354ed43a7e093b79a9ebb4f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798771"
---
# <a name="backward-compatibility"></a><span data-ttu-id="be71b-104">下位互換性</span><span class="sxs-lookup"><span data-stu-id="be71b-104">Backward compatibility</span></span>

<span data-ttu-id="be71b-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="be71b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="be71b-106">���̃g�s�b�N�ł́AMicrosoft Excel �̊e�o�[�W�����ɂ����� XLL �݊����̖��ɂ��Đ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="be71b-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="be71b-107">便利な定数の定義</span><span class="sxs-lookup"><span data-stu-id="be71b-107">Useful constant definitions</span></span>

<span data-ttu-id="be71b-p101">XLL プロジェクト コードに、次に示すような定義を組み込んで、このコンテキストで使用されるすべてのリテラルによる数値のインスタンスを置き換えることを検討してください。これにより、バージョン固有のコードが明確になり、バージョンに関連する一見無害な形の数値によるバグが発生する可能性を抑えられるようになります。</span><span class="sxs-lookup"><span data-stu-id="be71b-p101">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context. This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a><span data-ttu-id="be71b-110">実行中のバージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="be71b-110">Getting the running version</span></span>

<span data-ttu-id="be71b-111">バージョンを使用して実行しているを検出する必要があります`Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`、 `arg` **XLOPER**が 2 に設定する数値は、バージョンは、 **XLOPER**を整数値に強制的に変換する文字列です。</span><span class="sxs-lookup"><span data-stu-id="be71b-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="be71b-112">Microsoft Excel 2013 では、これは 15.0 です。</span><span class="sxs-lookup"><span data-stu-id="be71b-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="be71b-113">または、 [xlAutoOpen](xlautoopen.md)関数でこれを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="be71b-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="be71b-114">すべての Excel のバージョンを実行して、プロジェクト内のモジュールに通知するためのグローバル変数を設定できます。</span><span class="sxs-lookup"><span data-stu-id="be71b-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="be71b-115">**Excel12**および**XLOPER12**の s を使用して、 **Excel4** **XLOPER**の s を使用してを使用してまたは C の API を呼び出すか、コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="be71b-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="be71b-116">C API �̃o�[�W��������o���邽�߂� **XLCallVer** ��Ăяo�����Ƃ��ł��܂����A���̕��@�ł́AExcel 2007 ���O�̂ǂ̃o�[�W��������s���Ă��邩�ɂ��Ă͎�����܂���B</span><span class="sxs-lookup"><span data-stu-id="be71b-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="be71b-117">デュアル インターフェイスをエクスポートするアドインを作成します。</span><span class="sxs-lookup"><span data-stu-id="be71b-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="be71b-p103">1 �̕������󂯎��A���[�N�V�[�g�̃f�[�^�^�̂����ꂩ�ɂȂ� 1 �̒l��Ԃ� XLL �֐��ɂ��čl���Ă݂܂��傤�B"PD" �^�Ƃ��ēo�^����A���Ɏ����悤�Ƀv���g�^�C�v���ꂽ�֐���G�N�X�|�[�g�ł��܂��B������́A�����J�E���g�t���o�C�g������Ƃ��ēn����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="be71b-p103">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types. You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="be71b-120">����͊����ɓ��삵�܂����A�������̗��R����AExcel 2007 �ȍ~�̃R�[�h�ɑ΂��闝�z�I�ȃC���^�[�t�F�C�X�ɂ͂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="be71b-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="be71b-121">C API �̃o�C�g������Ɋւ��鐧�����������AExcel 2007 �ȍ~�ŃT�|�[�g����钷�� Unicode ������ɃA�N�Z�X�ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="be71b-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="be71b-122">Excel 2007 �ȍ~�� Excel �́A **XLOPER** �̎󂯓n�����\�ł��B�������A����͓���I�� **XLOPER12** �ɕϊ�����邽�߁AExcel 2007 �ȍ~�ł́A�ȑO�� Excel �̃o�[�W�����̃R�[�h�Ŏ��s����ꍇ�ɂ͑��݂��Ȃ��ÖٓI�ȕϊ��̃I�[�o�[�w�b�h���������܂��B</span><span class="sxs-lookup"><span data-stu-id="be71b-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="be71b-123">���̊֐��̓X���b�h �Z�[�t�ɂ���Ă���\��������܂����A�^������  `PD$` �ɕύX�����ƁAExcel 2007 �ȍ~�ł͓o�^�Ɏ��s���܂��B</span><span class="sxs-lookup"><span data-stu-id="be71b-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="be71b-124">�����̗��R����AExcel 2007 �ȍ~�ł�  `QD%$` �Ƃ��ēo�^����Ă������[�U�[�ɑ΂��āA�R�[�h���X���b�h �Z�[�t�ł���Ƒz�肵�āA���̂悤�Ƀv���g�^�C�v���ꂽ�֐���G�N�X�|�[�g����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="be71b-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="be71b-125">Excel 2007 �ȍ~�ł͕ʂ̊֐���o�^���邱�Ƃ��]�܂������ 1 �̗��R�́AXLL �֐����ő� 255 �̈�����󂯓���� (�ȑO�̃o�[�W�����ł� 30 �ɐ�������Ă��܂���)�B</span><span class="sxs-lookup"><span data-stu-id="be71b-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="be71b-p104">�D�s���Ȃ��ƂɁA�v���W�F�N�g���痼���̃o�[�W������G�N�X�|�[�g����ƁA�����̃����b�g�������܂��B���̌�A���s���� Excel �o�[�W��������o���āA�œK�Ȋ֐������ɂ���ēo�^���܂��B�ڍׂƎ�����ɂ��ẮA�u[Excel 2007 �̃A�h�C�� (XLLs) �̊J��](http://msdn.microsoft.com/en-us/library/aa730920.aspx)�v��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="be71b-p104">Fortunately, you can have the benefits of both by exporting both versions from your project. You can then detect the running Excel version and conditionally register the most appropriate function. For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](http://msdn.microsoft.com/en-us/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="be71b-p105">���̃A�v���[�\`�ł́A�������[�N�V�[�g�� Excel 2003 �Ŏ��s�����ꍇ�ƁAExcel 2007 �ȍ~�Ŏ��s�����ꍇ�ł́A�قȂ錋�ʂ��\�������\��������܂��B���Ƃ��΁AExcel 2003 �ł� Excel 2003 ���[�N�V�[�g �Z����� Unicode ������� ASCII �o�C�g������Ƀ}�b�s���O���A���̕������؂�l�߂Ă��� XLL �֐��ɓn���܂��BExcel 2007 �ȍ~�� Excel �ł́A�K�؂ȕ��@�œo�^���ꂽ XLL �֐��ɁA�ϊ�����Ă��Ȃ� Unicode �������n���܂��B���ꂪ�A�قȂ錋�ʂ̌����ɂȂ�܂��B���̂悤�ȉ\���ƃ��[�U�[�ւ̉e���ɑ΂��钍�ӂ́A�A�b�v�O���[�h���ȊO�ɂ�K�v�ɂȂ�܂��B���Ƃ��΁A�������̑g�ݍ��݂̐��l�֐��́AExcel 2000 �� Excel 2003 �Ƃ̊Ԃŉ��P����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="be71b-p105">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007. For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function. Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way. This could lead to a different result. You should be aware of this possibility and the consequences to your users, not just in the upgrade. For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="be71b-135">新しいワークシート関数と分析ツール関数</span><span class="sxs-lookup"><span data-stu-id="be71b-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="be71b-136">分析ツール (ATP) 関数は、Excel 2007 で Excel の一部です。</span><span class="sxs-lookup"><span data-stu-id="be71b-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="be71b-137">以前は、XLL は ATP 関数を呼び出す[xlUDF](xludf.md)を使用して、可能性がありますだけです。</span><span class="sxs-lookup"><span data-stu-id="be71b-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="be71b-138">Excel 2007 以降では、分析ツール関数が呼び出される xlcall.h で定義されている関数の列挙体を使用します。</span><span class="sxs-lookup"><span data-stu-id="be71b-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="be71b-139">Dll から関数を呼び出すユーザー定義の例は、2 つの方法を示します。</span><span class="sxs-lookup"><span data-stu-id="be71b-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be71b-140">�֘A����</span><span class="sxs-lookup"><span data-stu-id="be71b-140">See also</span></span>

- <span data-ttu-id="be71b-141">[C API �R�[���o�b�N�֐� Excel4�AExcel12](c-api-callback-functions-excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="be71b-141">[C API Callback Functions Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)</span></span> 
- [<span data-ttu-id="be71b-142">Excel �ł� C API ��g�p�����v���O���~���O</span><span class="sxs-lookup"><span data-stu-id="be71b-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- <span data-ttu-id="be71b-143">[Excel �p C API �̐V�@�[](what-s-new-in-the-c-api-for-excel.md)(what-s-new-in-the-c-api-for-excel.md)</span><span class="sxs-lookup"><span data-stu-id="be71b-143">[What's New in the C API for Excel](what-s-new-in-the-c-api-for-excel.md)</span></span>

