---
title: Excel での XLL コードへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accessing xll code [excel 2007],XLLs [Excel 2007], accessing code,commands [Excel 2007], registration,functions [Excel 2007], registration,calling XLLs from Excel,registering commands [Excel 2007],registering functions [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d1332b0dffc052404c75c4ec51d94879457c3da0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304187"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="152de-104">Excel での XLL コードへのアクセス</span><span class="sxs-lookup"><span data-stu-id="152de-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="152de-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="152de-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="152de-106">XLL に含まれる関数やコマンドに Microsoft Excel でアクセスできるようにするには、次の事柄が必要となります。</span><span class="sxs-lookup"><span data-stu-id="152de-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="152de-107">XLL によってエクスポートされなければなりません。</span><span class="sxs-lookup"><span data-stu-id="152de-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="152de-108">Excel に登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="152de-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="152de-109">関数とコマンドを Excel に登録する</span><span class="sxs-lookup"><span data-stu-id="152de-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="152de-110">登録することによって、DLL エントリ ポイントについて次のことを Excel に指示します。</span><span class="sxs-lookup"><span data-stu-id="152de-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="152de-111">非表示かどうか。また関数の場合には、関数ウィザードに表示するかどうか。</span><span class="sxs-lookup"><span data-stu-id="152de-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="152de-112">XLM マクロシートからのみ呼び出せるか、あるいはワークシートからも呼び出せるか。</span><span class="sxs-lookup"><span data-stu-id="152de-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="152de-113">コマンドの場合、ワークシート関数か、またはマクロシート同等関数かどうか。</span><span class="sxs-lookup"><span data-stu-id="152de-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="152de-114">XLL/DLL エクスポート名、および Excel で使用する名前。</span><span class="sxs-lookup"><span data-stu-id="152de-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="152de-115">関数の場合:</span><span class="sxs-lookup"><span data-stu-id="152de-115">If it is a function:</span></span>
    
  - <span data-ttu-id="152de-116">返すデータ型、および引数として取るデータ型。</span><span class="sxs-lookup"><span data-stu-id="152de-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="152de-117">引数をインプレースで変更して結果を返すかどうか。</span><span class="sxs-lookup"><span data-stu-id="152de-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="152de-118">揮発性かどうか。</span><span class="sxs-lookup"><span data-stu-id="152de-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="152de-119">スレッド セーフであるかどうか (Excel 2007 以降でサポートされています)。</span><span class="sxs-lookup"><span data-stu-id="152de-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="152de-120">関数貼り付けウィザードとオートコンプリート エディターに、関数の呼び出しを支援するために表示するテキスト。</span><span class="sxs-lookup"><span data-stu-id="152de-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="152de-121">リスト表示に使用する関数カテゴリ。</span><span class="sxs-lookup"><span data-stu-id="152de-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="152de-122">前述の点は、すべて C API 関数の [xlfRegister](xlfregister-form-1.md) を使用して行えます。この関数は XLM 関数の **REGISTER** に相当します。</span><span class="sxs-lookup"><span data-stu-id="152de-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="152de-123">Excel から直接 XLL 関数を呼び出す</span><span class="sxs-lookup"><span data-stu-id="152de-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="152de-124">XLL ワークシート関数とマクロシート関数を登録すると、組み込み関数を呼び出すことが可能な次に示すすべての場所からそれらも呼び出せます。</span><span class="sxs-lookup"><span data-stu-id="152de-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="152de-125">ワークシートの単一セルまたは配列数式。</span><span class="sxs-lookup"><span data-stu-id="152de-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="152de-126">マクロシートの単一セルまたは配列数式。</span><span class="sxs-lookup"><span data-stu-id="152de-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="152de-127">定義された名前の定義。</span><span class="sxs-lookup"><span data-stu-id="152de-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="152de-128">条件付き書式のダイアログ ボックスの、条件と制限のフィールド。</span><span class="sxs-lookup"><span data-stu-id="152de-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="152de-129">C API 関数 [xlUDF](xludf.md) を介して他のアドインから。</span><span class="sxs-lookup"><span data-stu-id="152de-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="152de-130">**Application.Run** メソッドを介して Visual Basic for Applications (VBA) から。</span><span class="sxs-lookup"><span data-stu-id="152de-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="152de-p101">C API 関数 **xlfCaller** を使用すると、関数内の呼び出し元セルへの参照またはセルの範囲を取得できます。関数がセルの条件付き書式の式から呼び出された場合、関連する 1 つまたは複数のセルへの参照が返されます。したがって、セルの数式に XLL 関数が含まれているとは限りません。関数が VBA ユーザー定義関数 (UDF) から呼び出された場合、**xlfCaller** は VBA 関数を呼び出したセルのアドレスを再び返します。詳細については、「[xlfCaller](xlfcaller.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="152de-p101">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**. If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function. If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function. For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="152de-p102">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes. You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute. To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span><span class="sxs-lookup"><span data-stu-id="152de-p102">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes. You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute. To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="152de-138">Excel から直接 XLL コマンドを呼び出す</span><span class="sxs-lookup"><span data-stu-id="152de-138">Calling XLL commands directly from Excel</span></span>

<span data-ttu-id="152de-139">XLL コマンドを登録すると、他のユーザー定義マクロを呼び出すことができる次に示すあらゆる方法で XLL コマンドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="152de-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="152de-140">ワークシートに埋め込まれているコントロール オブジェクトに関連付けることによって。</span><span class="sxs-lookup"><span data-stu-id="152de-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="152de-141">[マクロの実行] ダイアログ ボックスから。</span><span class="sxs-lookup"><span data-stu-id="152de-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="152de-142">**Application.Run** メソッドを使用して VBA ユーザー定義マクロから。</span><span class="sxs-lookup"><span data-stu-id="152de-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="152de-143">カスタマイズされたメニュー項目またはツールバーから。</span><span class="sxs-lookup"><span data-stu-id="152de-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="152de-144">コマンドを登録するときにセットアップされるショートカット キーボード操作を使用して。</span><span class="sxs-lookup"><span data-stu-id="152de-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="152de-145">指定したイベントがトラップされるときに実行するコマンドとして。</span><span class="sxs-lookup"><span data-stu-id="152de-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="152de-p103">XLL コマンドは非表示で、Excel のダイアログ ボックスで使用できるマクロの一覧に表示されません。ただし、[マクロ名] フィールドに手動で入力できます。Excel では、それらのダイアログ ボックスで、DLL エクスポート名ではなく登録されたとおりの名前であることが必要となります。</span><span class="sxs-lookup"><span data-stu-id="152de-p103">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes. But they can be entered manually into the macro name field. Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="152de-149">Excel に登録されているすべての XLL コマンドは、次の形式であることが Excel で想定されています。</span><span class="sxs-lookup"><span data-stu-id="152de-149">All XLL commands registered with Excel are assumed by Excel to be of the following form:</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="152de-p104">Excel は戻り値を無視します。ただし、XLM マクロ シートから呼び出されたものを除きます (この場合、戻り値は **TRUE** または **FALSE** に変換されます)。そのため、コマンドが正常に実行された場合は 1 を返す必要があります。また、コマンドが失敗したり、ユーザーによって取り消されたりした場合は 0 を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="152de-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="152de-p105">C API 関数の **xlfCaller** を使用すると、コマンドが呼び出された方法についての情報を取得できます。詳細については、「[xlfCaller](xlfcaller.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="152de-p105">You can obtain information about how your command was invoked using the C API function **xlfCaller**. For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
<span data-ttu-id="152de-p106">Excel 2007 以降のユーザー インターフェイスは以前のバージョンのものとは大きく異なります。ほとんどの場合、カスタム メニュー バー、メニュー、サブメニュー、メニュー項目、ユーザー設定ツールバー、ツールバー ボタンの追加と削除を行える C API 関数が引き続きサポートされています。ただし、必ずしも、ユーザーがこれまでに慣れている方法で追加項目が使用可能になるわけではありません。追加機能が引き続き利用できるかどうかを注意して確認し、利用できない場合にはバージョン固有のカスタマイズを実装してください。Excel 2007 以降、ユーザー インターフェイスはマネージ コード モジュールを使用して最適の方法でカスタマイズされていて、XLL コマンドと密に連動させることができます。</span><span class="sxs-lookup"><span data-stu-id="152de-p106">Starting in Excel 2007 user interface is very different from earlier versions. The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases. However, they may not always make the added item available in a way that your users are familiar with. You should carefully check that any added functionality is still accessible, or implement a version-specific customization. Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="152de-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="152de-159">See also</span></span>

- [<span data-ttu-id="152de-160">XLL を作成する</span><span class="sxs-lookup"><span data-stu-id="152de-160">Creating XLLs</span></span>](creating-xlls.md)
- <span data-ttu-id="152de-161">[関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span><span class="sxs-lookup"><span data-stu-id="152de-161">[Call XLL Functions from the Function Wizard or Replace Dialog Boxes](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span></span>
- [<span data-ttu-id="152de-162">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="152de-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="152de-163">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="152de-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



