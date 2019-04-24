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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306840"
---
# <a name="runapplication-macro-action"></a><span data-ttu-id="8f62f-102">RunApplication マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="8f62f-102">RunApplication macro action</span></span>

<span data-ttu-id="8f62f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f62f-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="セキュリティ メモ" alt="Security note" /><span data-ttu-id="8f62f-105"><strong>セキュリティに関するメモ</strong></span><span class="sxs-lookup"><span data-stu-id="8f62f-105"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f62f-p101">実行可能ファイルまたはマクロやアプリケーションのコードを実行するときは注意が必要です。実行可能ファイルまたはコードを使用してアクションを実行すると、コンピューターおよびデータのセキュリティを損なうおそれがあります。</span><span class="sxs-lookup"><span data-stu-id="8f62f-p101">Use caution when running executable files or code in macros or applications. Executable files or code can be used to carry out actions that might compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8f62f-p102">You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access. For example, you may want to paste Excel spreadsheet data into your Access database.</span><span class="sxs-lookup"><span data-stu-id="8f62f-p102">You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access. For example, you may want to paste Excel spreadsheet data into your Access database.</span></span>

> [!NOTE]
> <span data-ttu-id="8f62f-110">このアクションは、データベースが信頼されていない場合には許可されません。</span><span class="sxs-lookup"><span data-stu-id="8f62f-110">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="8f62f-111">設定値</span><span class="sxs-lookup"><span data-stu-id="8f62f-111">Setting</span></span>

<span data-ttu-id="8f62f-112">"RunApplication/アプリケーションの実行" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8f62f-112">The **RunApplication** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f62f-113">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="8f62f-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8f62f-114">説明</span><span class="sxs-lookup"><span data-stu-id="8f62f-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f62f-115"><strong>Command Line/コマンド ライン</strong></span><span class="sxs-lookup"><span data-stu-id="8f62f-115"><strong>Command Line</strong></span></span></p></td>
<td><p><span data-ttu-id="8f62f-p103">アプリケーションの起動に使用するコマンド ラインを指定します。パスの指定や、特定のモードでアプリケーションを実行するスイッチなどのパラメーターの指定もできます。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>コマンド ライン</strong>] ボックスにコマンド ラインを入力します。この引数は省略できません。  </span><span class="sxs-lookup"><span data-stu-id="8f62f-p103">The command line used to start the application (including the path and any other necessary parameters, such as switches that run the application in a particular mode). Enter the command line in the <strong>Command Line</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8f62f-119">注釈</span><span class="sxs-lookup"><span data-stu-id="8f62f-119">Remarks</span></span>

<span data-ttu-id="8f62f-p104">このアクションで指定したアプリケーションは、画面の一番手前で起動します。このアクションが定義されているマクロは、アプリケーションの起動後も継続して実行されます。</span><span class="sxs-lookup"><span data-stu-id="8f62f-p104">The application selected with this action loads and runs in the foreground. The macro containing this action continues to run after starting the application.</span></span>

<span data-ttu-id="8f62f-p105">You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard. You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data). You can also share data among applications by using automation.</span><span class="sxs-lookup"><span data-stu-id="8f62f-p105">You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard. You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data). You can also share data among applications by using automation.</span></span>

<span data-ttu-id="8f62f-125">MS-DOS ベースのアプリケーションは、Windows 環境の MS-DOS ウィンドウで実行します。</span><span class="sxs-lookup"><span data-stu-id="8f62f-125">MS-DOS-based applications run in an MS-DOS window within the Windows environment.</span></span>

<span data-ttu-id="8f62f-126">Windows オペレーティング システムでは、エクスプローラーからプログラムを起動する方法、[ **スタート**] メニューの [ **ファイル名を指定して実行**] コマンドを使用する方法、Windows のデスクトップでプログラム アイコンをダブルクリックする方法など、さまざまな方法でアプリケーションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="8f62f-126">In Windows operating systems, there are a number of ways to run an application, including starting the program from the Windows Explorer, using the **Run** command on the **Start** menu, and double-clicking a program icon on the Windows Desktop.</span></span>

<span data-ttu-id="8f62f-p106">You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module. Use the VBA **Shell** function instead.</span><span class="sxs-lookup"><span data-stu-id="8f62f-p106">You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module. Use the VBA **Shell** function instead.</span></span>

