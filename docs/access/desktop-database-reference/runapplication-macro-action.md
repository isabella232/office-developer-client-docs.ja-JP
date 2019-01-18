---
title: RunApplication マクロ アクション
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e7bf54934c6be215b2be5f32160d74fc2b4ab346
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721788"
---
# <a name="runapplication-macro-action"></a><span data-ttu-id="f7941-102">RunApplication マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="f7941-102">RunApplication macro action</span></span>

<span data-ttu-id="f7941-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f7941-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="セキュリティに関する注意" alt="Security note" /><span data-ttu-id="f7941-105"><strong>セキュリティ メモ</strong></span><span class="sxs-lookup"><span data-stu-id="f7941-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f7941-p101">実行可能ファイルまたはマクロやアプリケーションのコードを実行するときは注意が必要です。実行可能ファイルまたはコードを使用してアクションを実行すると、コンピューターおよびデータのセキュリティを損なうおそれがあります。</span><span class="sxs-lookup"><span data-stu-id="f7941-p101">Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f7941-108">**RunApplication**アクションを使用すると、Microsoft access から Microsoft Excel、Word、または Microsoft PowerPoint など、Windows ベースまたは ms-dos アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="f7941-108">You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access.</span></span> <span data-ttu-id="f7941-109">たとえば、Excel スプレッドシートのデータを Access データベースに貼り付ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f7941-109">For example, you may want to paste Excel spreadsheet data into your Access database.</span></span>

> [!NOTE]
> <span data-ttu-id="f7941-110">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="f7941-110">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="f7941-111">設定値</span><span class="sxs-lookup"><span data-stu-id="f7941-111">Setting</span></span>

<span data-ttu-id="f7941-112">**RunApplication**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="f7941-112">The **RunApplication** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7941-113">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="f7941-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f7941-114">説明</span><span class="sxs-lookup"><span data-stu-id="f7941-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7941-115"><strong>Command Line/コマンド ライン</strong></span><span class="sxs-lookup"><span data-stu-id="f7941-115"><strong>Command Line</strong></span></span></p></td>
<td><p><span data-ttu-id="f7941-p103">アプリケーションの起動に使用するコマンド ラインを指定します。パスの指定や、特定のモードでアプリケーションを実行するスイッチなどのパラメーターの指定もできます。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>コマンド ライン</strong>] ボックスにコマンド ラインを入力します。この引数は省略できません。  </span><span class="sxs-lookup"><span data-stu-id="f7941-p103">The command line used to start the application (including the path and any other necessary parameters, such as switches that run the application in a particular mode). Enter the command line in the <strong>Command Line</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f7941-119">解説</span><span class="sxs-lookup"><span data-stu-id="f7941-119">Remarks</span></span>

<span data-ttu-id="f7941-p104">このアクションで指定したアプリケーションは、画面の一番手前で起動します。このアクションが定義されているマクロは、アプリケーションの起動後も継続して実行されます。</span><span class="sxs-lookup"><span data-stu-id="f7941-p104">The application selected with this action loads and runs in the foreground. The macro containing this action continues to run after starting the application.</span></span>

<span data-ttu-id="f7941-122">他のアプリケーションと Access の間でデータを転送するには、Windows のダイナミック データ エクス (チェンジ DDE) 機能やクリップボードを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7941-122">You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard.</span></span> <span data-ttu-id="f7941-123">**"キー送信"** アクションを使用すると、(ただし、DDE は、データを転送するためのより効率的な方法です)、その他のアプリケーションにキーストロークを送信します。</span><span class="sxs-lookup"><span data-stu-id="f7941-123">You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data).</span></span> <span data-ttu-id="f7941-124">オートメーションを使用してアプリケーション間でデータを共有することもできます。</span><span class="sxs-lookup"><span data-stu-id="f7941-124">You can also share data among applications by using automation.</span></span>

<span data-ttu-id="f7941-125">MS-DOS ベースのアプリケーションは、Windows 環境の MS-DOS ウィンドウで実行します。</span><span class="sxs-lookup"><span data-stu-id="f7941-125">MS-DOS-based applications run in an MS-DOS window within the Windows environment.</span></span>

<span data-ttu-id="f7941-126">Windows オペレーティング システムでは、エクスプローラーからプログラムを起動する方法、[ **スタート**] メニューの [ **ファイル名を指定して実行**] コマンドを使用する方法、Windows のデスクトップでプログラム アイコンをダブルクリックする方法など、さまざまな方法でアプリケーションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f7941-126">In Windows operating systems, there are a number of ways to run an application, including starting the program from the Windows Explorer, using the **Run** command on the **Start** menu, and double-clicking a program icon on the Windows Desktop.</span></span>

<span data-ttu-id="f7941-127">Visual Basic for Applications (VBA) モジュールでは、 **RunApplication**アクションを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="f7941-127">You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="f7941-128">VBA **Shell**関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f7941-128">Use the VBA **Shell** function instead.</span></span>

