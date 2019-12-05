---
title: Office の 32 ビット バージョンと 64 ビット バージョン間の互換性
ms.date: 12/03/2019
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: 32 ビット バージョンの Office と 64 ビット バージョンの Office の互換性についてご確認ください。
localization_priority: Priority
ms.openlocfilehash: a0accc9c4b0198ab18b999353762a016d52f6b39
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819254"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="e08fb-103">Office の 32 ビット バージョンと 64 ビット バージョン間の互換性</span><span class="sxs-lookup"><span data-stu-id="e08fb-103">Compatibility between the 32-bit and 64-bit versions of Office</span></span>

<span data-ttu-id="e08fb-104">32 ビット バージョンの Office と 64 ビット バージョンの Office の互換性についてご確認ください。</span><span class="sxs-lookup"><span data-stu-id="e08fb-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="e08fb-105">Office アプリケーションは、32 ビット バージョンと 64 ビット バージョンでご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="e08fb-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="e08fb-p101">64 ビット バージョンの Office により、Microsoft Excel 2010 で大量のデータを扱う場合など、機能の強化に伴ってより多くのデータを移動させることができるようになりました。32 ビット コードを記述する場合は、変更なしで 64 ビット バージョンの Office を使うことができます。しかし、64 ビット コードを記述する場合は、そのコードに特定のキーワードと条件付きコンパイル定数を含めることで、以前のバーションの Office との下位互換性が確保されるようにし、32 ビット コードと 64 ビット コードを組み合わせて使う場合に正しいコードが実行されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p101">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010. When writing 32-bit code, you can use the 64-bit version of Office without any changes. However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of Office, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="e08fb-p102">Visual Basic for Applications 7.0 (VBA 7) は 64 ビット バージョンの Office でリリースされ、32 ビット バージョンと 64 ビット バージョンのどちらのアプリケーションでも動作します。この記事で説明されている変更は、64 ビット バージョンの Office にのみ適用されます。32 ビット バージョンの Microsoft Office を使うと、追加の変更を加えることなく、以前のバージョンの Office で作成したソリューションを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p102">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications. The changes described in this article apply only to the 64-bit versions of Office. Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e08fb-p103">既定で、64 ビット バージョンの Office をインストールすると、32 ビット バージョンが 64 ビット システムと共にインストールされます。Microsoft Office 64 ビット バージョンのインストール オプションを明示的に選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p103">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system. You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="e08fb-114">VBA 7 では、既存の Windows API ステートメント (**Declare** ステートメント) を更新して、64 ビット バージョンで動作するようにしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e08fb-114">In VBA 7, you must update existing Windows API statements (**Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="e08fb-115">さらに、これらのステートメントで使用されるアドレス ポインターとディスプレイ ウィンドウ ハンドルをユーザー定義型で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="e08fb-116">この点については、32 ビット バージョンと 64 ビット バージョン間の互換性に関する問題と推奨される解決案と共に、この記事で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="e08fb-117">32 ビット システムと 64 ビット システムの比較</span><span class="sxs-lookup"><span data-stu-id="e08fb-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="e08fb-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="e08fb-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span></span>

<span data-ttu-id="e08fb-p105">64 ビット バージョンの Office で作成されたアプリケーションは、32 ビットバージョンよりも大きいアドレス空間を参照することができます。つまり、以前と比べると、データに対してより多くの物理メモリを使うことができるため、物理メモリでのデータの出入りにかかるオーバーヘッドを軽減できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p105">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions. This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="e08fb-p106">物理メモリ内の特定の場所への参照 ("ポインター" と呼ばれる) に加えて、表示ウィンドウ識別子 ("ハンドル" と呼ばれる) を参照するアドレスを使うこともできます。32 ビット システムと 64 ビット システムのどちらを使うかに応じて、ポインターやハンドルのサイズ (バイト数) が決まります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p106">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles). The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="e08fb-123">既存のソリューションを 64 ビット バージョンの Office を使って実行する場合は、次の点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="e08fb-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="e08fb-p107">Office のネイティブの 64 ビット プロセスは、32 ビット バイナリを読み込むことができません。既存の Microsoft ActiveX コントロールと既存のアドインがある場合、これはよく起こる問題です。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p107">Native 64-bit processes in Office cannot load 32-bit binaries. This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins.</span></span>
    
- <span data-ttu-id="e08fb-p108">これまで VBA にはポインター データ型がなかったため、ポインターとハンドルを格納する 32 ビットの変数を使う必要がありました。 **Declare** ステートメントを使う場合、API 呼び出しで返される 64 ビット値は、これらの変数で切り詰められるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p108">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles. These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="e08fb-128">VBA 7 コード ベース</span><span class="sxs-lookup"><span data-stu-id="e08fb-128">VBA 7 code base</span></span>
<span data-ttu-id="e08fb-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="e08fb-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span></span>

<span data-ttu-id="e08fb-p109">VBA 7 は、Office 2007 以前のバージョンでの VBA コード ベースを置き換えます。VBA 7 は、Office の 32 ビットと 64 ビットのどちらのバージョンでもご利用いただけます。次の 2 つの条件付きコンパイル定数があります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p109">VBA 7 replaces the VBA code base in Office 2007 and earlier versions. VBA 7 is available in both the 32-bit and 64-bit versions of Office. It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="e08fb-133">**VBA7** - アプリケーションが VBA 7 を使っているか、以前のバージョンの VBA を使っているかをテストすることによって、コードの下位互換性が確保されます。</span><span class="sxs-lookup"><span data-stu-id="e08fb-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="e08fb-134">**Win64** 32 ビットと 64 ビットのどちらでコードが実行されているかをテストします。</span><span class="sxs-lookup"><span data-stu-id="e08fb-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="e08fb-135">特定の例外を除き、32 ビット バージョンのアプリケーションで機能しているドキュメント内のマクロは 64 ビット バージョンでも機能します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="e08fb-136">ActiveX コントロールと COM アドインの互換性</span><span class="sxs-lookup"><span data-stu-id="e08fb-136">ActiveX control and COM add-in compatibility</span></span>
<span data-ttu-id="e08fb-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="e08fb-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span></span>

<span data-ttu-id="e08fb-p110">既存の 32 ビット ActiveX コントロールは Office の 64 ビット バージョンと互換性がありません。ActiveX コントロールと COM オブジェクトについては、次のようにしてください。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p110">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office. For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="e08fb-140">ソース コードがあれば、64 ビット バージョンを自分で生成します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-140">If you have the source code, generate a 64-bit version yourself.</span></span>
- <span data-ttu-id="e08fb-141">ソース コードがなければ、販売元に更新されたバージョンを請求してください。</span><span class="sxs-lookup"><span data-stu-id="e08fb-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="e08fb-p111">Office のネイティブの 64 ビット プロセスでは 32 ビットのバイナリを読み込むことができません。これには、 **MSComCtl** の一般的なコントロール (TabStrip、Toolbar、StatusBar、ProgressBar、TreeView、ListViews、ImageList、Slider、ImageComboBox) と、 **MSComCt2** のコントロール (Animation、UpDown、MonthView、DateTimePicker、FlatScrollBar) が含まれます。これらのコントロールは、Office 2010 より前の 32 ビット バージョンの Office でインストールされました。64 ビット バージョンの Office にコードを移行するときにこれらのコントロールを使う既存の VBA ソリューションの代替策を見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p111">Native 64-bit processes in Office cannot load 32-bit binaries. This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar). These controls were installed by 32-bit versions of Office earlier than Office 2010. You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="e08fb-146">API の互換性</span><span class="sxs-lookup"><span data-stu-id="e08fb-146">API compatibility</span></span>
<span data-ttu-id="e08fb-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="e08fb-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span></span>

<span data-ttu-id="e08fb-p112">VBA ライブラリとタイプ ライブラリを組み合わせれば、Office アプリケーションの作成にさまざまな機能を使えるようになります。ただし、コンピューターのオペレーティング システムや他のコンポーネントとの直接のやりとりが必要になることもあります。たとえば、メモリやプロセスの管理、ウィンドウやコントロールなどの UI 要素の操作、Windows レジストリの変更を行うときです。このような状況では、DLL ファイルに組み込まれた外部関数を使うのが最善策です。VBA でこれを行うには、 **Declare** を使って API 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p112">The combination of VBA and type libraries gives you lots of functionality to create Office applications. However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry. In these scenarios, your best option is to use one of the external functions that are embedded in DLL files. You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e08fb-152">Microsoft は、1,500 個の Declare ステートメントが含まれている Win32API.txt ファイルと、コードに含める **Declare** ステートメントをコピーするツールを提供しています。</span><span class="sxs-lookup"><span data-stu-id="e08fb-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="e08fb-153">ただし、これらのステートメントは 32 ビット システム用であるため、この記事で後ほど説明する情報に従って 64 ビットに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="e08fb-154">既存の **Declare** ステートメントは、**PtrSafe** 属性を使って 64 ビットに対して安全なステートメントとしてマークするまでは、64 ビットの VBA にコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="e08fb-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="e08fb-155">この種類の変換の例については、Excel MVP Jan Karel Pieterse の Web サイト ([https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp)) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e08fb-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="e08fb-156">[Office Code Compatibility Inspector ユーザーズ ガイド](https://docs.microsoft.com/previous-versions/office/office-2010/ee833946(v=office.14))は、**PtrSafe** 属性と適切な戻り値の型 (必要に応じて) の API **Declare** ステートメントの構文を検査するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e08fb-156">The [Office Code Compatibility Inspector user's guide](https://docs.microsoft.com/previous-versions/office/office-2010/ee833946(v=office.14)) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="e08fb-157">**Declare** ステートメントの形式は、サブルーチン (戻り値がない) と関数 (戻り値がある) のどちらを呼び出すのかに応じて、次のどちらかになります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-157">**Declare** statements resemble one of the following, depending on whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="e08fb-p114">**SubName** 関数または **FunctionName** 関数は、プロシージャを VBA コードから呼び出すときに使用する名前を表しており、DLL ファイル内のプロシージャの実際の名前に置き換えます。プロシージャの名前として **AliasName** 引数を指定することもできます。 **Lib** キーワードの後ろには、呼び出すプロシージャが含まれている DLL ファイルの名前を指定します。引数リストには、プロシージャに渡す必要のあるパラメーターとデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p114">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code. You can also specify an **AliasName** argument for the name of the procedure. The name of the DLL file that contains the procedure being called follows the **Lib** keyword. And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="e08fb-162">次の **Declare** ステートメントは、Windows レジストリ内の*サブキー*を開き、その値を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e08fb-162">The following **Declare** statement opens a  *subkey*  in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="e08fb-163">**RegOpenKeyA** 関数の Windows.h (ウィンドウ ハンドル) エントリは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="e08fb-p115">Visual C と Microsoft Visual C++ では、上記の例は 32 ビットと 64 ビットのどちらについても正しくコンパイルされます。なぜなら、HKEY がポインターとして定義されており、そのサイズはコードをコンパイルするプラットフォームのメモリ サイズを反映するからです。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p115">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit. This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="e08fb-p116">以前のバージョンの VBA では、特定のポインター データ型がなかったので、 **Long** データ型が使われていました。 **Long** データ型は常に 32 ビットなので、64 ビット メモリのシステムで使用すると問題が起きます。なぜなら、上位の 32 ビットが切り捨てられるか、他のメモリ アドレスに上書きされることがあるからです。どちらの場合も、予測できない動作やシステム クラッシュを引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p116">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used. And because the **Long** data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits might be truncated or might overwrite other memory addresses. Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="e08fb-p117">この問題を解決するため、VBA には *LongPtr* という真の  **ポインター**  データ型があります。この新しいデータ型を使用すれば、次のように本来の **Declare** ステートメントを正しく書くことができます。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p117">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**. This new data type enables you to write the original **Declare** statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="e08fb-p118">このデータ型と新しい **PtrSafe** 属性を使うと、この **Declare** ステートメントを 32 ビット システムでも 64 ビット システムでも使うことができます。 **PtrSafe** 属性は、 **Declare** ステートメントの対象を 64 ビット バージョンの Office とすることを VBA コンパイラに指示するものです。この属性を指定せずに **Declare** ステートメントを 64 ビット システムで使うと、コンパイル時エラーが発生します。 **PtrSafe** 属性は、32 ビット バージョンの Office ではオプションです。これにより、既存の **Declare** ステートメントは従来どおりに動作します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p118">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems. The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office. Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error. The **PtrSafe** attribute is optional on the 32-bit version of Office. This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="e08fb-176">次の表では、新しい修飾子とデータ型に加え、1 つのデータ型、2 つの変換演算子、3 つの関数についても説明します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-176">The following table provides more information about the new qualifier and data typeas well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="e08fb-177">種類</span><span class="sxs-lookup"><span data-stu-id="e08fb-177">Type</span></span>|<span data-ttu-id="e08fb-178">アイテム</span><span class="sxs-lookup"><span data-stu-id="e08fb-178">Item</span></span>|<span data-ttu-id="e08fb-179">説明</span><span class="sxs-lookup"><span data-stu-id="e08fb-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e08fb-180">修飾子</span><span class="sxs-lookup"><span data-stu-id="e08fb-180">Qualifier</span></span>  <br/> |<span data-ttu-id="e08fb-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="e08fb-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="e08fb-p119">**Declare** ステートメントが 64 ビットと互換性があることを示します。この属性は 64 ビット システムでは必須です。  </span><span class="sxs-lookup"><span data-stu-id="e08fb-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="e08fb-184">データ型</span><span class="sxs-lookup"><span data-stu-id="e08fb-184">Data Type</span></span>  <br/> |<span data-ttu-id="e08fb-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="e08fb-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="e08fb-p120">変数のデータ型であり、Microsoft Office の 32 ビット バージョンでは 4 バイトのデータ型で、64 ビット バージョンでは 8 バイトのデータ型です。これは新しいコードでポインターやハンドルを宣言するときの推奨方法です。ただし、レガシー コードでも、64 ビット バージョンの Office で実行する場合は、やはりこれが推奨される方法です。これは 32 ビットおよび 64 ビットで VBA 7 ランタイムでのみサポートされます。そこに数値を代入することはできますが、数値型を代入することはできません。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p120">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office. This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office. It is only supported in the VBA 7 runtime on 32-bit and 64-bit. Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="e08fb-190">データ型</span><span class="sxs-lookup"><span data-stu-id="e08fb-190">Data Type</span></span>  <br/> |<span data-ttu-id="e08fb-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="e08fb-191">**LongLong**</span></span> <br/> |<span data-ttu-id="e08fb-p121">これは 64 ビット バージョンの Microsoft Office でのみ使用できる 8 バイトのデータ型です。数値を代入することはできますが、数値型を代入することはできません (切り詰められるのを避けるためです)。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p121">This is an 8-byte data type which is available only in 64-bit versions of Microsoft Office. You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="e08fb-194">変換演算子</span><span class="sxs-lookup"><span data-stu-id="e08fb-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="e08fb-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="e08fb-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="e08fb-196">単純な式を **LongPtr** データ型に変換します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="e08fb-197">変換演算子</span><span class="sxs-lookup"><span data-stu-id="e08fb-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="e08fb-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="e08fb-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="e08fb-199">単純な式を **LongLong** データ型に変換します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="e08fb-200">職務</span><span class="sxs-lookup"><span data-stu-id="e08fb-200">Function</span></span>  <br/> |<span data-ttu-id="e08fb-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="e08fb-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="e08fb-p122">バリアント コンバーター。64 ビット バージョンでは **LongPtr** を返し、32 ビット バージョンでは **Long** を返します (4 バイト)。  </span><span class="sxs-lookup"><span data-stu-id="e08fb-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="e08fb-204">職務</span><span class="sxs-lookup"><span data-stu-id="e08fb-204">Function</span></span>  <br/> |<span data-ttu-id="e08fb-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="e08fb-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="e08fb-p123">オブジェクト コンバーター。64 ビット バージョンでは **LongPtr** を返し、32 ビット バージョンでは **Long** を返します (4 バイト)。  </span><span class="sxs-lookup"><span data-stu-id="e08fb-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="e08fb-208">職務</span><span class="sxs-lookup"><span data-stu-id="e08fb-208">Function</span></span>  <br/> |<span data-ttu-id="e08fb-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="e08fb-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="e08fb-p124">文字列コンバーター。64 ビット バージョンでは **LongPtr** を返し、32 ビット バージョンでは **Long** を返します (4 バイト)。  </span><span class="sxs-lookup"><span data-stu-id="e08fb-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="e08fb-212">次の例は、これらのアイテムのいくつかについて、 **Declare** ステートメントでの使用方法を示したものです。</span><span class="sxs-lookup"><span data-stu-id="e08fb-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="e08fb-213">**Declare** ステートメントで **PtrSafe** を指定しないと、64 ビット バージョンの Office と互換性がないものと見なされます。</span><span class="sxs-lookup"><span data-stu-id="e08fb-213">Note that **Declare** statements without the **PtrSafe** attribute are assumed not to be compatible with the 64-bit version of Office.</span></span> 
  
<span data-ttu-id="e08fb-p125">**VBA7** と **Win64** という 2 つの条件付きコンパイル定数があります。以前のバージョンの Microsoft Office との下位互換性を確保するには、 **VBA7** 定数を使って (これがより一般的なやり方です)、以前のバージョンの Office で 64 ビット コードが実行されないようにします。32 ビット バージョンと 64 ビット バージョンとでコードが異なる場合は (たとえば、64 ビット バージョンについては **LongLong** を使い、32 ビット バージョンについては **Long** を使う数値演算 API を呼び出す場合など)、 **Win64** 定数を使います。次のコードで、この 2 つの定数の使用例を示します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p125">There are two conditional compilation constants: **VBA7** and **Win64**. To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office. For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant. The following code shows the use of these two constants.</span></span> 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

<span data-ttu-id="e08fb-p126">要約すると次のようになります。64 ビットのコードを書き、それを以前のバージョンの Office で使用する場合は、 **VBA7** 条件付きコンパイル定数を使用する必要があります。しかし、32 ビットのコードを書き、それを Office で使用する場合は、このコンパイル定数を使用しなくても、そのコードは以前のバージョンの Office での動作と同じになります。32 ビット バージョンには間違いなく 32 ビットのステートメントが使われ、64 ビット バージョンには間違いなく 64 ビットのステートメントが使われるようにするには、 **Win64** 条件付きコンパイル定数を使用するのが最善策です。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p126">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant. However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant. If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="e08fb-221">条件付きコンパイル属性の使用</span><span class="sxs-lookup"><span data-stu-id="e08fb-221">Using conditional compilation attributes</span></span>
<span data-ttu-id="e08fb-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="e08fb-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span></span>

<span data-ttu-id="e08fb-p127">次に、更新する必要がある 32 ビット用に記述された VBA コードの例を示します。このレガシー コードのデータ型は、ハンドルやポインターを参照しているため、 **LongPtr** を使うように更新されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p127">The following example shows VBA code written for 32-bit that needs to be updated. Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers.</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="e08fb-225">32 ビット バージョン用に記述された VBA コード</span><span class="sxs-lookup"><span data-stu-id="e08fb-225">VBA code written for 32-bit versions</span></span>
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="e08fb-226">64 ビット バージョン用に記述された VBA コード</span><span class="sxs-lookup"><span data-stu-id="e08fb-226">VBA code rewritten for 64-bit versions</span></span>
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<span data-ttu-id="e08fb-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="e08fb-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="e08fb-228">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="e08fb-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="e08fb-229">どのような場合に 64 ビット バージョンの Office を使うべきですか。</span><span class="sxs-lookup"><span data-stu-id="e08fb-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="e08fb-p128">使っているホスト アプリケーション (Excel、Word など) によって異なります。たとえば、Excel を 64 ビット バージョンの Microsoft Office で使うと、より大きなワークシートを処理できます。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p128">This is more a matter of which host application (Excel, Word, and so forth) you are using. For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="e08fb-232">64 ビット バージョンと 32 ビット バージョンの Office を同時にインストールできますか。</span><span class="sxs-lookup"><span data-stu-id="e08fb-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="e08fb-233">いいえ。</span><span class="sxs-lookup"><span data-stu-id="e08fb-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="e08fb-234">どのような場合に Long パラメーターを LongPtr に変換する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="e08fb-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="e08fb-p129">呼び出す関数については、Microsoft Developers Network の Windows API ドキュメントを確認する必要があります。ハンドルとポインターは **LongPtr** に変換する必要があります。たとえば、 [RegOpenKeyA](https://docs.microsoft.com/windows/win32/api/winreg/nf-winreg-regopenkeyexa) のドキュメントは、次のシグネチャを提供します。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p129">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call. Handles and pointers need to be converted to **LongPtr**. As an example, the documentation for [RegOpenKeyA](https://docs.microsoft.com/windows/win32/api/winreg/nf-winreg-regopenkeyexa) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="e08fb-238">パラメーターは次のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="e08fb-238">The parameters are defined as:</span></span>
  
|<span data-ttu-id="e08fb-239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e08fb-239">Parameter</span></span>|<span data-ttu-id="e08fb-240">説明</span><span class="sxs-lookup"><span data-stu-id="e08fb-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="e08fb-241">hKey [in]</span><span class="sxs-lookup"><span data-stu-id="e08fb-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="e08fb-242">レジストリ キーを開く *ハンドル*  。</span><span class="sxs-lookup"><span data-stu-id="e08fb-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="e08fb-243">lpSubKey [in, optional]</span><span class="sxs-lookup"><span data-stu-id="e08fb-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="e08fb-244">開くレジストリ サブキーの名前。</span><span class="sxs-lookup"><span data-stu-id="e08fb-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="e08fb-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="e08fb-245">ulOptions</span></span>  <br/> |<span data-ttu-id="e08fb-246">このパラメーターは予約済みで、0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08fb-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="e08fb-247">samDesired [in]</span><span class="sxs-lookup"><span data-stu-id="e08fb-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="e08fb-248">キーに対する必要なアクセス権を指定するマスク。</span><span class="sxs-lookup"><span data-stu-id="e08fb-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="e08fb-249">phkResult [out]</span><span class="sxs-lookup"><span data-stu-id="e08fb-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="e08fb-250">キーを開くハンドルを受け取る変数への *ポインター*  。</span><span class="sxs-lookup"><span data-stu-id="e08fb-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="e08fb-251">[Win32API_PtrSafe.txt](https://docs.microsoft.com/office/troubleshoot/office/win32api_ptrsafe-with-64-bit-support) では、**Declare** ステートメントが次のように定義されています。</span><span class="sxs-lookup"><span data-stu-id="e08fb-251">In [Win32API_PtrSafe.txt](https://docs.microsoft.com/office/troubleshoot/office/win32api_ptrsafe-with-64-bit-support), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="e08fb-252">構造体のポインターとハンドルを変換する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="e08fb-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="e08fb-p130">はい。Win32API_PtrSafe.txt の **MSG** 型をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p130">Yes. See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="e08fb-255">strptr、varpt、objptr は、どのような場合に使用すべきですか。</span><span class="sxs-lookup"><span data-stu-id="e08fb-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="e08fb-p131">これらの関数は、文字列、変数、オブジェクトへのポインターを取得するために使う必要があります。64 ビット バージョンの Office では、これらの関数は 64 ビットの **LongPtr** を返します。これは **Declare** ステートメントに渡すことができます。これらの関数の使い方は、以前のバージョンの VBA と変わっていません。唯一の違いは、 **LongPtr** を返すことです。</span><span class="sxs-lookup"><span data-stu-id="e08fb-p131">You should use these functions to retrieve pointers to strings, variables and objects, respectively. On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements. The use of these functions has not changed from previous versions of VBA. The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e08fb-260">関連項目</span><span class="sxs-lookup"><span data-stu-id="e08fb-260">See also</span></span>
<span data-ttu-id="e08fb-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="e08fb-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span></span>

- <span data-ttu-id="e08fb-262">[Anatomy of a Declare Statement](https://docs.microsoft.com/previous-versions/aa671659(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="e08fb-262">[Anatomy of a Declare Statement](https://docs.microsoft.com/previous-versions/aa671659(v=vs.71))</span></span>
