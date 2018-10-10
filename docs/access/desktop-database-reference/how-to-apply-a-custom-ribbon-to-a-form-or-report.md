---
title: フォームまたはレポートにカスタム リボンを適用します。
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478796"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="015a9-102">フォームまたはレポートにカスタム リボンを適用します。</span><span class="sxs-lookup"><span data-stu-id="015a9-102">Apply a custom ribbon to a form or report</span></span>


<span data-ttu-id="015a9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="015a9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="015a9-p101">リボンでは、リボン XML の作成およびカスタマイズを簡素化するテキストベースの宣言型 XML マークアップが使用されています。XML を数行記述するだけで、ユーザーに最適なインターフェイスを作成できます。Access では、柔軟にリボン ユーザー インターフェイスをカスタマイズできます。たとえば、カスタマイズしたマークアップをテーブルまたは別の Access データベースに格納する、VBA プロシージャに埋め込む、Excel のワークシートと関連付けるなどの操作ができます。このトピックでは、フォームまたはレポートを読み込むときにカスタマイズしたリボンを適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="015a9-p101">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides flexibility in customizing the ribbon user interface. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="015a9-109">リボンのカスタマイズ XML を使用できるようにする</span><span class="sxs-lookup"><span data-stu-id="015a9-109">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="015a9-110">**リボン機能拡張 XML をテーブルに保管する**</span><span class="sxs-lookup"><span data-stu-id="015a9-110">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="015a9-p102">リボンのカスタマイズを使用できるようにするための 1 つの方法は、リボンのカスタマイズをテーブルに保管することです。カスタマイズを " **USysRibbons** " という名前のテーブルに保管した場合、マクロまたは VBA コードを使用せずにカスタマイズを実装できます。</span><span class="sxs-lookup"><span data-stu-id="015a9-p102">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="015a9-p103">**USysRibbons** は、ユーザーが作成するシステム テーブルです。リボンのカスタマイズを実装するには、特定の列名を使用してこのテーブルを作成する必要があります。 **USysRibbons** テーブルを作成するときに使用する設定の一覧を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="015a9-p103">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="015a9-116">列名</span><span class="sxs-lookup"><span data-stu-id="015a9-116">Column Name</span></span></p></th>
<th><p><span data-ttu-id="015a9-117">データ型</span><span class="sxs-lookup"><span data-stu-id="015a9-117">Data Type</span></span></p></th>
<th><p><span data-ttu-id="015a9-118">説明</span><span class="sxs-lookup"><span data-stu-id="015a9-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="015a9-119"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="015a9-119"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="015a9-120">テキスト型 (Text)</span><span class="sxs-lookup"><span data-stu-id="015a9-120">Text</span></span></p></td>
<td><p><span data-ttu-id="015a9-121">このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="015a9-121">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="015a9-122"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="015a9-122"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="015a9-123">メモ型 (Memo)</span><span class="sxs-lookup"><span data-stu-id="015a9-123">Memo</span></span></p></td>
<td><p><span data-ttu-id="015a9-124">リボン、リボンのカスタマイズを定義する機能拡張 XML (RibbonX) が含まれています</span><span class="sxs-lookup"><span data-stu-id="015a9-124">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="015a9-125">**プログラムを使用してリボン拡張 XML を読み込む**</span><span class="sxs-lookup"><span data-stu-id="015a9-125">**Loading Ribbon Extensibility XML Programmatically**</span></span>

<span data-ttu-id="015a9-p104">**[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** メソッドを使用してリボンのカスタマイズをプログラムで読み込むことができます。通常、リボンを作成し、そのリボンをアプリケーションで使用できるようにするには、まず、リボンの名前と XML カスタマイズ マークアップを渡して **LoadCustomUI** メソッドを呼び出すプロシージャを使用して、データベースにモジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="015a9-p104">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="015a9-p105">XML マークアップには、テーブルから作成される **Recordset** オブジェクト、データベース外部のソース (文字列に解析する XML ファイルなど)、またはプロシージャの内部に直接埋め込まれた XML マークアップを指定できます。各リボンの名前およびリボンを構成するタブの **id** 属性が一意である限り、 **LoadCustomUI** メソッドへの呼び出しを複数回使用し、それぞれに異なる XML マークアップを渡すことで、異なるリボンを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="015a9-p105">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="015a9-p106">プロシージャが完了したら、"RunCode/プロシージャの実行" アクションを使用してプロシージャを呼び出す AutoExec マクロを作成します。これにより、アプリケーションが開始されたときに **LoadCustomUI** メソッドが自動的に実行され、すべてのカスタム リボンをアプリケーションで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="015a9-p106">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="015a9-132">カスタム リボンをフォームまたはレポートに割り当てる</span><span class="sxs-lookup"><span data-stu-id="015a9-132">Assigning Custom Ribbons to Forms or Reports</span></span>

1.  <span data-ttu-id="015a9-133">前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="015a9-133">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="015a9-134">デザイン ビューでフォームまたはレポートを開きます。</span><span class="sxs-lookup"><span data-stu-id="015a9-134">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="015a9-135">[デザイン] タブの [ **プロパティ シート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="015a9-135">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="015a9-136">[プロパティ] ウィンドウの [ **すべて**] タブで、[ **リボン名**] ボックスをクリックし、リボンを選択します。</span><span class="sxs-lookup"><span data-stu-id="015a9-136">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="015a9-p107">フォームまたはレポートを保存して閉じ、再度開きます。選択した リボン UI が表示されます。</span><span class="sxs-lookup"><span data-stu-id="015a9-p107">Save, close, and then reopen the form or report. The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="015a9-139">[!メモ] リボン UI に表示されるタブは付加的なものです。</span><span class="sxs-lookup"><span data-stu-id="015a9-139">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="015a9-140">具体的には、タブを非表示にするか、*最初から*属性を**True**に設定、しない限り、フォームのタブが表示されますか、レポートのリボンのユーザー インターフェイスは、既存のタブに追加します。</span><span class="sxs-lookup"><span data-stu-id="015a9-140">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="015a9-141">[!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="015a9-141">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


