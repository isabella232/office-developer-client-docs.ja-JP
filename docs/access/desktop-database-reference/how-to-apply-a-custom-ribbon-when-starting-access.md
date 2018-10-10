---
title: アクセスを開始するときにカスタム リボンを適用します。
TOCTitle: Apply a custom ribbon when starting Access
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 575834f818386a7ba536e826fff2b7da00b324d5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479719"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a><span data-ttu-id="478e8-102">アクセスを開始するときにカスタム リボンを適用します。</span><span class="sxs-lookup"><span data-stu-id="478e8-102">Apply a custom ribbon when starting Access</span></span>

<span data-ttu-id="478e8-103">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="478e8-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="478e8-p101">リボンでは、リボン XML の作成およびカスタマイズを簡素化するテキストベースの宣言型 XML マークアップが使用されています。XML を数行記述するだけで、ユーザーに最適なインターフェイスを作成できます。Access では、非常に柔軟にリボン UI をカスタマイズできます。たとえば、カスタマイズしたマークアップをテーブルまたは別の Access データベースに格納する、VBA プロシージャに埋め込む、Excel のワークシートと関連付けるなどの操作ができます。このトピックでは、データベースを開くときにカスタマイズしたリボンを適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="478e8-p101">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides tremendous flexibility in customizing the ribbon UI. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when opening a database.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="478e8-109">リボンのカスタマイズ XML を使用できるようにする</span><span class="sxs-lookup"><span data-stu-id="478e8-109">Making the Ribbon Customization XML Available</span></span>

### <a name="storing-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="478e8-110">リボン機能拡張 XML をテーブルに保管する</span><span class="sxs-lookup"><span data-stu-id="478e8-110">Storing Ribbon Extensibility XML in a Table</span></span>

<span data-ttu-id="478e8-p102">リボンのカスタマイズを使用できるようにするための 1 つの方法は、リボンのカスタマイズをテーブルに保管することです。カスタマイズを " **USysRibbons** " という名前のテーブルに保管した場合、マクロまたは VBA コードを使用せずにカスタマイズを実装できます。</span><span class="sxs-lookup"><span data-stu-id="478e8-p102">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="478e8-p103">**USysRibbons** は、ユーザーが作成するシステム テーブルです。リボンのカスタマイズを実装するには、特定の列名を使用してこのテーブルを作成する必要があります。 **USysRibbons** テーブルを作成するときに使用する設定の一覧を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="478e8-p103">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="478e8-116">列名</span><span class="sxs-lookup"><span data-stu-id="478e8-116">Column Name</span></span></p></th>
<th><p><span data-ttu-id="478e8-117">データ型</span><span class="sxs-lookup"><span data-stu-id="478e8-117">Data Type</span></span></p></th>
<th><p><span data-ttu-id="478e8-118">説明</span><span class="sxs-lookup"><span data-stu-id="478e8-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="478e8-119"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="478e8-119"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="478e8-120">テキスト型 (Text)</span><span class="sxs-lookup"><span data-stu-id="478e8-120">Text</span></span></p></td>
<td><p><span data-ttu-id="478e8-121">このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="478e8-121">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="478e8-122"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="478e8-122"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="478e8-123">メモ型 (Memo)</span><span class="sxs-lookup"><span data-stu-id="478e8-123">Memo</span></span></p></td>
<td><p><span data-ttu-id="478e8-124">リボンのカスタマイズを定義するリボン拡張 XML (RibbonX) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="478e8-124">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="loading-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="478e8-125">プログラムを使用してリボン拡張 XML を読み込む</span><span class="sxs-lookup"><span data-stu-id="478e8-125">Loading Ribbon Extensibility XML Programmatically</span></span>

<span data-ttu-id="478e8-p104">**[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** メソッドを使用してリボンのカスタマイズをプログラムで読み込むことができます。通常、リボンを作成し、そのリボンをアプリケーションで使用できるようにするには、まず、リボンの名前と XML カスタマイズ マークアップを渡して **LoadCustomUI** メソッドを呼び出すプロシージャを使用して、データベースにモジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="478e8-p104">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="478e8-p105">XML マークアップには、テーブルから作成される **Recordset** オブジェクト、データベース外部のソース (文字列に解析する XML ファイルなど)、またはプロシージャの内部に直接埋め込まれた XML マークアップを指定できます。各リボンの名前およびリボンを構成するタブの **id** 属性が一意である限り、 **LoadCustomUI** メソッドへの呼び出しを複数回使用し、それぞれに異なる XML マークアップを渡すことで、異なるリボンを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="478e8-p105">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="478e8-p106">プロシージャが完了したら、"RunCode/プロシージャの実行" アクションを使用してプロシージャを呼び出す AutoExec マクロを作成します。これにより、アプリケーションが開始されたときに **LoadCustomUI** メソッドが自動的に実行され、すべてのカスタム リボンをアプリケーションで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="478e8-p106">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="applying-customized-ribbons-when-access-starts"></a><span data-ttu-id="478e8-132">Access の起動時にカスタマイズされたリボンを適用する</span><span class="sxs-lookup"><span data-stu-id="478e8-132">Applying Customized Ribbons When Access Starts</span></span>

<span data-ttu-id="478e8-133">アプリケーションの起動時にカスタム UI を使用できるように適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="478e8-133">To apply a custom UI so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="478e8-134">前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="478e8-134">Follow the process described previously to make the customized ribbons available to the application.</span></span>

2.  <span data-ttu-id="478e8-135">アプリケーションを閉じて、再起動します。</span><span class="sxs-lookup"><span data-stu-id="478e8-135">Close and then restart the application.</span></span>

3.  <span data-ttu-id="478e8-136">**Microsoft Office ボタン**をクリックして![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") [ **Access のオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="478e8-136">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="478e8-137">[ **カレント データベース**] オプションをクリックし、[ **リボンとツール バーのオプション**] セクションで [ **リボン名**] ボックスをクリックして、リボンを選択します。</span><span class="sxs-lookup"><span data-stu-id="478e8-137">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select a ribbon.</span></span>

5.  <span data-ttu-id="478e8-p107">アプリケーションを閉じて、再起動します。選択した UI が表示されます。</span><span class="sxs-lookup"><span data-stu-id="478e8-p107">Now close and restart the application. The UI you selected is displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="478e8-140">[!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="478e8-140">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


