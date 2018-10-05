---
title: 下位互換機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- バージョン互換性 [excel 2007],XLL 互換性 [Excel 2007],下位互換性 [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387973"
---
# <a name="backward-compatibility"></a><span data-ttu-id="93974-104">下位互換機能</span><span class="sxs-lookup"><span data-stu-id="93974-104">Backward compatibility</span></span>

<span data-ttu-id="93974-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="93974-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="93974-106">このトピックでは、Microsoft Excel の各バージョンにおける XLL 互換性の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="93974-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="93974-107">便利な定数の定義</span><span class="sxs-lookup"><span data-stu-id="93974-107">Useful constant definitions</span></span>

<span data-ttu-id="93974-p101">XLL プロジェクト コードに、次に示すような定義を組み込んで、このコンテキストで使用されるすべてのリテラルによる数値のインスタンスを置き換えることを検討してください。これにより、バージョン固有のコードが明確になり、バージョンに関連する一見無害な形の数値によるバグが発生する可能性を抑えられるようになります。</span><span class="sxs-lookup"><span data-stu-id="93974-p101">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context. This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
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

## <a name="getting-the-running-version"></a><span data-ttu-id="93974-110">実行中のバージョンの取得</span><span class="sxs-lookup"><span data-stu-id="93974-110">Getting the running version</span></span>

<span data-ttu-id="93974-111">実行中のバージョンは、`Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)` を使用して検出します。この `arg` は 2 に設定された数値型の **XLOPER** です。また、version は文字列型の **XLOPER** であり、後から強制的に整数に変換できます。</span><span class="sxs-lookup"><span data-stu-id="93974-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="93974-112">Microsoft Excel 2013 では、これは 15.0 です。</span><span class="sxs-lookup"><span data-stu-id="93974-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="93974-113">この操作には、[xlAutoOpen](xlautoopen.md) 関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93974-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="93974-114">その後、グローバル変数を設定することで、どのバージョンの Excel を実行しているかについて、プロジェクトに含まれるすべてのモジュールに通知できます。</span><span class="sxs-lookup"><span data-stu-id="93974-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="93974-115">これにより、コード内で **Excel12** と **XLOPER12** を使用する C API を呼び出すか、**Excel4** と **XLOPER** を使用する C API を呼び出すかを決定します。</span><span class="sxs-lookup"><span data-stu-id="93974-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="93974-116">C API のバージョンを検出するために **XLCallVer** を呼び出すことができますが、この方法では、Excel 2007 より前のどのバージョンを実行しているかについては示されません。</span><span class="sxs-lookup"><span data-stu-id="93974-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="93974-117">デュアル インターフェイスをエクスポートするアドインの作成</span><span class="sxs-lookup"><span data-stu-id="93974-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="93974-p103">1 つの文字列を受け取り、ワークシートのデータ型のいずれかになる 1 つの値を返す XLL 関数について考えてみましょう。"PD" 型として登録され、次に示すようにプロトタイプされた関数をエクスポートできます。文字列は、長さカウント付きバイト文字列として渡されています。</span><span class="sxs-lookup"><span data-stu-id="93974-p103">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types. You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="93974-120">これは完璧に動作しますが、いくつかの理由から、Excel 2007 以降のコードに対する理想的なインターフェイスにはなりません。</span><span class="sxs-lookup"><span data-stu-id="93974-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="93974-121">C API のバイト文字列に関する制限が課せられ、Excel 2007 以降でサポートされる長い Unicode 文字列にアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="93974-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="93974-122">Excel 2007 以降の Excel は、**XLOPER** の受け渡しが可能です。ただし、これは内部で **XLOPER12** に変換されるため、Excel 2007 以降では、以前の Excel のバージョンのコードで実行する場合には存在しない暗黙的な変換のオーバーヘッドが発生します。</span><span class="sxs-lookup"><span data-stu-id="93974-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="93974-123">この関数はスレッド セーフにされている可能性がありますが、型文字列が `PD$` に変更されると、Excel 2007 以降では登録に失敗します。</span><span class="sxs-lookup"><span data-stu-id="93974-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="93974-124">これらの理由から、Excel 2007 以降では `QD%$` として登録されていたユーザーに対して、コードがスレッド セーフであると想定して、次のようにプロトタイプされた関数をエクスポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="93974-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="93974-125">Excel 2007 以降では別の関数を登録することが望ましいもう 1 つの理由は、XLL 関数が最大 255 個の引数を受け入れる (以前のバージョンでは 30 個に制限されていました)。</span><span class="sxs-lookup"><span data-stu-id="93974-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="93974-p104">好都合なことに、プロジェクトから両方のバージョンをエクスポートすると、両方のメリットが得られます。その後、実行中の Excel バージョンを検出して、最適な関数を条件によって登録します。詳細と実装例については、「[Excel 2007 のアドイン (XLL) の開発](https://msdn.microsoft.com/library/aa730920.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93974-p104">Fortunately, you can have the benefits of both by exporting both versions from your project. You can then detect the running Excel version and conditionally register the most appropriate function. For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="93974-p105">このアプローチでは、同じワークシートを Excel 2003 で実行した場合と、Excel 2007 以降で実行した場合では、異なる結果が表示される可能性があります。たとえば、Excel 2003 では Excel 2003 ワークシート セル内の Unicode 文字列を ASCII バイト文字列にマッピングし、その文字列を切り詰めてから XLL 関数に渡します。Excel 2007 以降の Excel では、適切な方法で登録された XLL 関数に、変換されていない Unicode 文字列を渡します。これが、異なる結果の原因になります。このような可能性とユーザーへの影響に対する注意は、アップグレード時以外にも必要になります。たとえば、いくつかの組み込みの数値関数は、Excel 2000 と Excel 2003 との間で改善されています。</span><span class="sxs-lookup"><span data-stu-id="93974-p105">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007. For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function. Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way. This could lead to a different result. You should be aware of this possibility and the consequences to your users, not just in the upgrade. For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="93974-135">新しいワークシート関数と分析ツール関数</span><span class="sxs-lookup"><span data-stu-id="93974-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="93974-136">分析ツール (ATP) 関数は、Excel 2007 以降の Excel に含まれています。</span><span class="sxs-lookup"><span data-stu-id="93974-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="93974-137">以前は、XLL では [xlUDF](xludf.md) を使用することでのみ ATP 関数を呼び出せました。</span><span class="sxs-lookup"><span data-stu-id="93974-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="93974-138">Excel 2007 以降では、xlcall.h で定義されている関数の列挙値を使用して、ATP 関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="93974-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="93974-139">「DLL からのユーザー定義関数の呼び出し」の例では、2 通りの方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="93974-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93974-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="93974-140">See also</span></span>

- [<span data-ttu-id="93974-141">C API コールバック関数 Excel4、Excel12</span><span class="sxs-lookup"><span data-stu-id="93974-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="93974-142">Excel での C API を使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="93974-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="93974-143">Excel 用 C API の新機能</span><span class="sxs-lookup"><span data-stu-id="93974-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

