---
title: XLL を作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- dlls [excel 2007], calling into excel,xlAutoFree function [Excel 2007],xlAutoFree12 function [Excel 2007],xlcall32.lib [Excel 2007],xlAutoRegister function [Excel 2007],xlcall.cpp [Excel 2007],xlAutoRemove function [Excel 2007],xlAddInManagerInfo function [Excel 2007],xlAutoAdd function [Excel 2007],xlAutoOpen function [Excel 2007],xlAutoClose function [Excel 2007],DLLs [Excel 2007], turning into XLLs,XLLs [Excel 2007], calling into Excel,xlAutoRegister12 function [Excel 2007],xlcall.h [Excel 2007],xlAddInManagerInfo12 function [Excel 2007]
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 886b8e74f00f2e724785d43475ee0ffa3c922710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304145"
---
# <a name="creating-xlls"></a><span data-ttu-id="03b4c-104">XLL を作成する</span><span class="sxs-lookup"><span data-stu-id="03b4c-104">Creating XLLs</span></span>

<span data-ttu-id="03b4c-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="03b4c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="03b4c-106">DLL が自己完結型であるか、他のライブラリのみに依存する場合、Microsoft Excel を有効にしてその関数とコマンドにアクセスする方法について把握しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-106">If your DLL is self-contained or relies only on other libraries, you must know how to enable Microsoft Excel to access its functions and commands.</span></span> <span data-ttu-id="03b4c-107">詳細については、「[Excel で DLL にアクセスする](how-to-access-dlls-in-excel.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03b4c-107">For more information, see [Access DLLs in Excel](how-to-access-dlls-in-excel.md).</span></span> 
  
<span data-ttu-id="03b4c-108">ただし、DLL が Excel の機能にアクセスする必要がある場合 (たとえば、セルの内容を取得するときや、ワークシート関数を呼び出すとき、または Excel を照会してワークスペース情報を取得するときなど) は、コードから Excel へのコールバックが可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="03b4c-108">However, if your DLL needs to access Excel functionality (for example, to get the contents of a cell, to call a worksheet function, or to interrogate Excel to obtain workspace information), your code must be able to call back into Excel.</span></span>
  
<span data-ttu-id="03b4c-p102">Excel C API には、Dll が Excel にコールバックできるようにするいくつかの関数が用意されています。これらにアクセスするには、Excel 32 ビットライブラリ xlcall32 を使用して、コンパイル時に DLL を静的にリンクする必要があります。静的ライブラリは、このライブラリの 32 ビット版と 64 ビット版の両方を含む Microsoft Excel 2013 XLL SDK の一部として Microsoft からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p102">The Excel C API provides several functions that enable DLLs to call back into Excel. To access these, the DLL must be linked statically at compile time with the Excel 32-bit library, xlcall32.lib. The static library is downloadable from Microsoft as part of the Microsoft Excel 2013 XLL SDK, which includes both 32-bit and 64-bit versions of this library.</span></span>
  
## <a name="enabling-dlls-to-call-back-into-excel"></a><span data-ttu-id="03b4c-112">Dll から Excel へのコールバックを可能にする</span><span class="sxs-lookup"><span data-stu-id="03b4c-112">Enabling DLLs to Call Back into Excel</span></span>

<span data-ttu-id="03b4c-p103">DLL が Excel の機能にアクセスし、ワークスペース情報を取得または設定できるようにするには、まず Excel のコールバック関数 **Excel4**、**Excel4v**、**Excel12**、および **Excel12v** のアドレスを取得する必要があります。最後の 2 つは、Excel 2007 で導入され、以降のバージョンで利用可能です。これらのすべてにアクセスするには、DLL プロジェクトに、Excel 2013 XLL SDK から次のファイルへの参照が含まれている必要があります。最初の 2 つのコールバック (任意のバージョンの Excel) にのみアクセスする場合は、プロジェクトに最初の 2 つのファイルのみを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p103">For a DLL to be able to access the functionality in Excel and get or set workspace information, it must first obtain the addresses of the Excel callback functions **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**. The last two were introduced in Excel 2007 and are available in subsequent versions. To access all of these, the DLL project must include references to the following files from the Excel 2013 XLL SDK. If you want to access only the first two callbacks (in any version of Excel), your project needs to include only the first two files.</span></span>
  
### <a name="xlcallh"></a><span data-ttu-id="03b4c-117">Xlcall.h</span><span class="sxs-lookup"><span data-stu-id="03b4c-117">Xlcall.h</span></span>

<span data-ttu-id="03b4c-118">Xlcall.h ファイルには、次の項目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="03b4c-118">The Xlcall.h file contains the following items:</span></span>
  
- <span data-ttu-id="03b4c-119">すべてのコールバック関数の関数プロトタイプ。</span><span class="sxs-lookup"><span data-stu-id="03b4c-119">Function prototypes for all callback functions.</span></span>
    
- <span data-ttu-id="03b4c-120">DLL/XLL と ExcelDLL 間でのデータ交換にコールバックが使用するデータ構造の定義、データ型定数の定義。</span><span class="sxs-lookup"><span data-stu-id="03b4c-120">Definitions of the data structures that the callbacks use to exchange data between the DLL/XLL and Excel, and data-type constant definitions.</span></span>
    
- <span data-ttu-id="03b4c-121">ワークシート関数、マクロ シート関数、およびサポートされている Excel コマンドに相当する C API 関数とコマンドの定義。</span><span class="sxs-lookup"><span data-stu-id="03b4c-121">Definitions of the C API function and command equivalents of the worksheet, macro sheet functions, and supported Excel commands.</span></span>
    
- <span data-ttu-id="03b4c-122">コールバック関数の戻り値の定義。</span><span class="sxs-lookup"><span data-stu-id="03b4c-122">Definitions of callback function return values.</span></span>
    
<span data-ttu-id="03b4c-123">このファイルでは、C API にアクセスするすべてのファイル、または C API が使用するデータ型を処理するすべてのファイルにおいて、このファイルの **#include** ディレクティブを (直接、あるいは別のヘッダー ファイルを介して間接的に) 使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-123">You should use the **#include** directive for this file, directly or indirectly via another header file, in all files that access the C API or that handle data types that the C API uses.</span></span> 
  
### <a name="xlcall32lib"></a><span data-ttu-id="03b4c-124">Xlcall32.lib</span><span class="sxs-lookup"><span data-stu-id="03b4c-124">Xlcall32.lib</span></span>

<span data-ttu-id="03b4c-p104">Xlcall32 ライブラリは、最初の 2 つのコールバック、**Excel4** と **Excel4v**、および **XlCallVer** 関数もエクスポートします。プロジェクトでこのライブラリへの参照がなければ、コードでこれらのコールバックのいずれかを使用している場合は、リンカーは XLL を作成できません。(これらの関数のアドレスは、通常の Excel インストールの一部としてシステムにコピーされる同等の Xlcall32.dll に動的にリンクすることによって取得できます)</span><span class="sxs-lookup"><span data-stu-id="03b4c-p104">The Xlcall32.lib library exports the first two callbacks, **Excel4** and **Excel4v**, and also the **XlCallVer** function. Without a reference to this library in your project, the linker cannot create the XLL if you have used any of these callbacks in your code. (You can obtain the addresses of these functions by linking dynamically to the equivalent Xlcall32.dll that is copied to your system as part of a normal Excel installation.)</span></span> 
  
### <a name="xlcallcpp"></a><span data-ttu-id="03b4c-128">Xlcall.cpp</span><span class="sxs-lookup"><span data-stu-id="03b4c-128">Xlcall.cpp</span></span>

<span data-ttu-id="03b4c-p105">Excel のコールバック **Excel12** と **Excel12v** は Xlcall32.lib ではエクスポートされません。これにより、Excel 2007 以降で作成する XLL プロジェクトは、以前のバージョンの Excel でも機能します。Xlcall.cpp モジュールには **Excel12** および **Excel12v** 関数のコードが含まれており、Excel 2007 以降の Excel エントリ ポイントを呼び出したり、以前のバージョンの Excel を実行している場合は安全なエラー値を返したりします。Excel 2007 以降で実行する、より大きなグリッドと長い Unicode 文字列を処理する新しいデータ型を使用できる XLL を作成したい場合は、このモジュールをプロジェクトに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p105">The Excel callbacks **Excel12** and **Excel12v** are not exported in Xlcall32.lib. This ensures that XLL projects that you create starting in Excel 2007 will also work with earlier versions of Excel. The Xlcall.cpp module contains code for the **Excel12** and **Excel12v** functions, which call into an Excel entry point starting in Excel 2007, or return a safe error value if you are running an earlier version of Excel. You should include this module in your project if you want to create an XLL that runs starting in Excel 2007 and that is able to use the new data types that handle larger grids and longer Unicode strings.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03b4c-133">Excel 2010 SDK 以降では、このファイルは 32 ビットと 64 ビットの両方の XLL にコンパイルできます。</span><span class="sxs-lookup"><span data-stu-id="03b4c-133">Starting with the Excel 2010 SDK, this file can be compiled for both 32-bit and 64-bit XLLs.</span></span> 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a><span data-ttu-id="03b4c-134">DLL を XLL に変換する: アドイン マネージャー インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="03b4c-134">Turning DLLs into XLLs: Add-in Manager Interface Functions</span></span>

<span data-ttu-id="03b4c-p106">XLL は、Excel または Excel のアドイン マネージャーによって呼び出されるいくつかのプロシージャをエクスポートする DLL です。ここでは、これらのプロシージャを簡単に説明します。詳細な説明については、「[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)」を参照してください。これらの DLL コールバックはすべてプレフィックス **xlAuto** で始まります。これらのうち必須コマンドは **xlAutoOpen** のみです。これは、アドインが有効になると呼び出され、通常は Excel に XLL の関数とコマンドを登録してその他の初期化タスクを実行するために使用されます。すべての **xlAuto** 関数の関数シグネチャと実装例は、後のセクションで説明します。 </span><span class="sxs-lookup"><span data-stu-id="03b4c-p106">An XLL is a DLL that exports several procedures that are called by Excel or the Excel Add-in Manager. These procedures are described briefly here and discussed in detail in [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md). All of these DLL callbacks start with the prefix **xlAuto**. Only one of these, the command **xlAutoOpen**, is required. It is called when the add-in is activated, and it is typically used to register XLL functions and commands with Excel and to do other initialization tasks. The function signatures and example implementations of all of the **xlAuto** functions are provided in later sections.</span></span> 
  
<span data-ttu-id="03b4c-141">これらのコールバックの中で必須なのは **xlAutoOpen** だけですが、アドインの動作によっては、他のコマンドもエクスポートする必要がある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-141">Even though **xlAutoOpen** is the only required one of these callbacks, your add-in may also need to export others depending on its behavior.</span></span> 
  
<span data-ttu-id="03b4c-p107">Excel 2007 では、より大きなグリッドに対応し、長い Unicode 文字列をサポートするために、新しいデータ型 **XLOPER12** が導入されました。 **XLOPER12** については、このトピックの後半で説明します。**xlAuto** 関数は古いデータ型 **XLOPER** を取得または返すのに対し、これらの関数の新しいバージョンは **XLOPER12** データ型を使用する Excel 2007 で導入されました。**XLOPER12** のメモリリークを回避するために実装する必要がある **xlAutoFree12** を除いて、バージョン 12 の **xlAuto** 関数をすべて省略しても問題ありません (この場合、Excel 2007 以降では **XLOPER** バージョンが呼び出されます)。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p107">Excel 2007 introduced a new data type, **XLOPER12**, to accommodate larger grids and to support long Unicode strings. **XLOPER12** is described later in this topic. Whereas **xlAuto** functions take or return the old data type **XLOPER**, new versions of these functions were introduced in Excel 2007 that use **XLOPER12** data types. With the exception of **xlAutoFree12**, which you must sometimes implement to avoid **XLOPER12** memory leaks, you can safely omit all the version 12 **xlAuto** functions, in which case, starting in Excel 2007, Excel calls the **XLOPER** versions.</span></span> 
  
### <a name="xlautoopen"></a><span data-ttu-id="03b4c-146">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="03b4c-146">xlAutoOpen</span></span>

<span data-ttu-id="03b4c-p108">Excel は、XLL がアクティブになるたびに [xlAutoOpen](xlautoopen.md) 関数を呼び出します。正常終了した最後の Excel セッションでアクティブだったアドインは、次の Excel セッションの開始時にアクティブ化されます。アドインは、Excel セッション中に読み込まれると、アクティブになります。アドインが Excel セッション中に非アクティブにされてから再度アクティブにされる場合の、再アクティブ化のときにこの関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p108">Excel calls the [xlAutoOpen](xlautoopen.md) function whenever the XLL is activated. The add-in will be activated at the start of an Excel session if it was active in the last Excel session that ended normally. The add-in is activated if it is loaded during an Excel session. The add-in can be deactivated and reactivated during an Excel session, and the function is called on reactivation.</span></span> 
  
<span data-ttu-id="03b4c-151">XLL の関数とコマンドの登録、データ構造の初期化、ユーザー インターフェイスのカスタマイズなどを行うには、**xlAutoOpen** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-151">You should use **xlAutoOpen** to register XLL functions and commands, initialize data structures, customize the user interface, and so on.</span></span> 
  
<span data-ttu-id="03b4c-p109">アドインが [xlAutoRegister](xlautoregister-xlautoregister12.md) 関数または [xlAutoRegister12](xlautoregister-xlautoregister12.md) 関数を実装してエクスポートする場合、Excel は最初に **xlAutoOpen** 関数を呼び出さずに関数やコマンドをアクティブ化して登録しようとすることがあります。この場合は、関数またはコマンドが正しく機能するように、アドインが十分に初期化されていることを確認する必要があります。そうなっていない場合、関数やコマンドの登録や、必要な初期化の実行が失敗します。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p109">If your add-in implements and exports the [xlAutoRegister](xlautoregister-xlautoregister12.md) function or the [xlAutoRegister12](xlautoregister-xlautoregister12.md) function, Excel might attempt to activate and register a function or command without first calling the **xlAutoOpen** function. In this case, you should ensure that your add-in is sufficiently initialized for your function or command to work properly. If it is not, you should either fail the attempt to register the function or command, or carry out the necessary initialization.</span></span> 
  
### <a name="xlautoclose"></a><span data-ttu-id="03b4c-155">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="03b4c-155">xlAutoClose</span></span>

<span data-ttu-id="03b4c-p110">XLL ファイルが非アクティブになるたびに、Excel は [xlAutoClose](xlautoclose.md) を呼び出します。Excel セッションが正常に終了すると、アドインは非アクティブになります。Excel セッション中にユーザーがアドインを非アクティブ化する場合に、この関数は呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p110">Excel calls the [xlAutoClose](xlautoclose.md) function whenever the XLL is deactivated. The add-in will be deactivated when an Excel session ends normally. If the user deactivates the add-in during an Excel session, the function is called.</span></span> 
  
<span data-ttu-id="03b4c-159">関数とコマンドの登録解除、リソースの解放、カスタマイズの解除などを行うには、**xlAutoClose** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-159">You should use **xlAutoClose** to unregister functions and commands, release resources, undo customizations, and so on.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03b4c-p111">関数とコマンドの登録解除に関しては、既知の問題があります。詳しくは、「[Excel XLL 開発での既知の問題](known-issues-in-excel-xll-development.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p111">There is a known issue with the unregistration of functions and commands. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
### <a name="xlautoadd"></a><span data-ttu-id="03b4c-162">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="03b4c-162">xlAutoAdd</span></span>

<span data-ttu-id="03b4c-p112">ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL をアクティブ化すると、Excel は [xlAutoAdd 関数](xlautoadd.md)を呼び出します。Excel が起動して、あらかじめインストールされたアドインを読み込む際には、この関数は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p112">Excel calls the [xlAutoAdd function](xlautoadd.md) whenever the user activates the XLL during an Excel session by using the Add-In Manager. This function is not called when Excel starts and loads a preinstalled add-in.</span></span> 
  
<span data-ttu-id="03b4c-165">この関数を使用して、アドインがアクティブになっていることをユーザーに通知するカスタム ダイアログ ボックスの表示、レジストリに対する読み書き、またはライセンス情報の確認を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="03b4c-165">You can use this function to display a custom dialog box that tells the user that the add-in has been activated, to read from or write to the registry, or to check licensing information.</span></span>
  
### <a name="xlautoremove"></a><span data-ttu-id="03b4c-166">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="03b4c-166">xlAutoRemove</span></span>

<span data-ttu-id="03b4c-p113">ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL を非アクティブ化すると、Excel は [xlAutoRemove](xlautoremove.md) 関数を呼び出します。アドインがインストールされている状態で Excel セッションが終了するときには、正常終了でも異常終了でも、この関数は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p113">Excel calls the [xlAutoRemove](xlautoremove.md) function whenever the user deactivates the XLL during an Excel session by using the Add-In Manager. This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span> 
  
<span data-ttu-id="03b4c-169">この関数を使用して、アドインが非アクティブになっていることをユーザーに通知するカスタム ダイアログ ボックスを表示したり、レジストリへの読み書きを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="03b4c-169">You can use this function to display a custom dialog box that tells the user that the add-in has been deactivated, or to read from or write to the registry.</span></span>
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="03b4c-170">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="03b4c-170">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

<span data-ttu-id="03b4c-p114">アドイン マネージャーが Excel セッションで初めて呼び出されるとき、Excel は [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) 関数を呼び出します。Excel が 1 と等しい引数を渡す場合、この関数は文字列 (通常は、アドインの名前) を返す必要があります。それ以外の場合は、**#VALUE!** を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p114">Excel calls the [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) function when the Add-in Manager is invoked for the first time in an Excel session. If Excel passes an argument equal to 1, this function should return a string (typically, the name of the add-in); otherwise, it should return **#VALUE!**.</span></span>
  
<span data-ttu-id="03b4c-p115">Excel 2007 以降のバージョンでは、XLL によってエクスポートされる場合には **xlAddInManagerInfo** 関数ではなく **xlAddInManagerInfo12** 関数が呼び出されます。**xlAddInManagerInfo12** 関数は、**xlAddInManagerInfo** と同じように機能して、XLL の動作におけるバージョン固有の相違点を回避する必要があります。**xlAddInManagerInfo12** 関数は **XLOPER12** データ型を返し、**xlAddInManagerInfo** は **XLOPER** データ型を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p115">Starting in Excel 2007, Excel calls the **xlAddInManagerInfo12** function in preference to the **xlAddInManagerInfo** function if it is exported by the XLL. The **xlAddInManagerInfo12** function should work in the same way as the **xlAddInManagerInfo** function to avoid version-specific differences in the behavior of the XLL. The **xlAddInManagerInfo12** function should return an **XLOPER12** data type, whereas the **xlAddInManagerInfo** function should return an **XLOPER** data type.</span></span> 
  
### <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="03b4c-176">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="03b4c-176">xlAutoRegister/xlAutoRegister12</span></span>

<span data-ttu-id="03b4c-p116">Excel は登録対象の関数の戻り値の型と引数の型がない状態で、XLM 関数 **REGISTER**、または C API の同等の [xlfRegister](xlfregister-form-1.md) 関数に対する呼び出しが実行されると、常に [xlAutoRegister 関数](xlautoregister-xlautoregister12.md)を呼び出します。**xlAutoRegister**関数により、XLL はその内部にあるエクスポートされた関数とコマンドのリストを検索してその関数を引数とともに登録し、指定された型を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p116">Excel calls the [xlAutoRegister](xlautoregister-xlautoregister12.md) function whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister](xlfregister-form-1.md) function, with the return and argument types missing for the function being registered. The **xlAutoRegister** function allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return the specified types.</span></span> 
  
<span data-ttu-id="03b4c-179">Excel 2007 以降では、**xlAddInRegister12** 関数が XLL によってエクスポートされている場合、Excel はこの関数を **xlAddInRegister** 関数よりも優先して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="03b4c-179">Starting in Excel 2007, Excel calls the **xlAddInRegister12** function in preference to the **xlAddInRegister** function if it is exported by the XLL.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03b4c-180">引数と戻り値の型の指定がないままで **xlAddInRegister**/ **xlAddInRegister12** が関数を登録しようとすれば、再帰的な呼び出しのループが発生し、最終的にはコール スタックがオーバーフローして Excel が終了するか、応答しなくなります。</span><span class="sxs-lookup"><span data-stu-id="03b4c-180">If **xlAddInRegister**/ **xlAddInRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs that eventually overflows the call stack and causes Excel to close or stop responding.</span></span> 
  
### <a name="xlautofreexlautofree12"></a><span data-ttu-id="03b4c-181">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="03b4c-181">xlAutoFree/xlAutoFree12</span></span>

<span data-ttu-id="03b4c-p117">Excel calls the [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) function just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** data type with a flag set that tells Excel there is memory that the XLL still needs to release. This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks. Starting in Excel 2007, the **XLOPER12** data type is supported. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="03b4c-p117">Excel calls the [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) function just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** data type with a flag set that tells Excel there is memory that the XLL still needs to release. This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks. Starting in Excel 2007, the **XLOPER12** data type is supported. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="03b4c-p118">Starting in Excel 2007, when Excel is configured to use multithreaded worksheet recalculation, the **xlAutoFree**/ **xlAutoFree12** function is called on the same thread that was just used to call the function that returned it. The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread. This simplifies thread-safe design in your XLL. For more information, see [Multithreaded Recalculation in Excel](multithreaded-recalculation-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="03b4c-p118">Starting in Excel 2007, when Excel is configured to use multithreaded worksheet recalculation, the **xlAutoFree**/ **xlAutoFree12** function is called on the same thread that was just used to call the function that returned it. The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread. This simplifies thread-safe design in your XLL. For more information, see [Multithreaded Recalculation in Excel](multithreaded-recalculation-in-excel.md).</span></span> 
  
### <a name="creating-64-bit-xlls"></a><span data-ttu-id="03b4c-190">64 ビット XLL の作成</span><span class="sxs-lookup"><span data-stu-id="03b4c-190">Creating 64-bit XLLs</span></span>

<span data-ttu-id="03b4c-p119">Excel およびユーザー定義関数は、32 ビット オペレーティング システムよりも優れたパフォーマンスを期待できる 64 ビット オペレーティング システムで実行可能です。Excel は、データの型に関する情報を含む **XLOPER12** 構造の値を渡します。**XLOPER12** 構造とネイティブ型 (**int** またはより大きい型に値を保持するポインターなど) の間で値を変換する場合はご注意ください。</span><span class="sxs-lookup"><span data-stu-id="03b4c-p119">Excel and user-defined functions can run on 64-bit operating systems to take advantage of performance benefits over 32-bit operating systems. Excel passes values in **XLOPER12** structures that include information about the types for the data. Be careful when you convert between values in the **XLOPER12** structure and native types like **int** or pointers to preserve the values in the larger type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03b4c-194">関連項目</span><span class="sxs-lookup"><span data-stu-id="03b4c-194">See also</span></span>



<span data-ttu-id="03b4c-195">[関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span><span class="sxs-lookup"><span data-stu-id="03b4c-195">[Call XLL Functions from the Function Wizard or Replace Dialog Boxes](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span></span>
  
[<span data-ttu-id="03b4c-196">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="03b4c-196">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
[<span data-ttu-id="03b4c-197">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="03b4c-197">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

