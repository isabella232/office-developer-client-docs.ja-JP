---
title: フォームまたはレポートにカスタム リボンを適用する
TOCTitle: Apply a custom ribbon to a form or report
description: Access 2013 でフォームまたはレポートを読み込むときにカスタマイズされたリボンを適用する方法。
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 329f184a1bcd3c856ccfd0b15c3fa92bc6230c98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291916"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="7d6a7-103">フォームまたはレポートにカスタム リボンを適用する</span><span class="sxs-lookup"><span data-stu-id="7d6a7-103">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="7d6a7-104">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d6a7-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d6a7-105">リボンでは、リボン XML の作成およびカスタマイズを簡素化するテキストベースの宣言型 XML マークアップが使用されています。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-105">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="7d6a7-106">XML を数行記述するだけで、ユーザーに最適なインターフェイスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-106">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="7d6a7-107">Access では、柔軟にリボン ユーザー インターフェイスをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-107">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="7d6a7-108">たとえば、カスタマイズしたマークアップをテーブルまたは別の Access データベースに格納する、VBA プロシージャに埋め込む、Excel のワークシートと関連付けるなどの操作ができます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-108">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="7d6a7-109">このトピックでは、フォームまたはレポートを読み込むときにカスタマイズしたリボンを適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-109">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="7d6a7-110">リボン カスタマイズ XML を利用可能にする</span><span class="sxs-lookup"><span data-stu-id="7d6a7-110">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="7d6a7-111">リボン機能拡張 XML をテーブルに格納する</span><span class="sxs-lookup"><span data-stu-id="7d6a7-111">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="7d6a7-p103">リボンのカスタマイズを使用できるようにするための 1 つの方法は、リボンのカスタマイズをテーブルに保管することです。カスタマイズを " **USysRibbons** " という名前のテーブルに保管した場合、マクロまたは VBA コードを使用せずにカスタマイズを実装できます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-p103">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="7d6a7-114">**USysRibbons** はユーザーが作成したシステム テーブルです。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-114">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="7d6a7-115">リボンのカスタマイズを実装するには、特定の列名を使用してテーブルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-115">The table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="7d6a7-116">次のテーブルは、**USysRibbons** テーブルを作成するときに使用する設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-116">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d6a7-117">列名</span><span class="sxs-lookup"><span data-stu-id="7d6a7-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="7d6a7-118">データ型</span><span class="sxs-lookup"><span data-stu-id="7d6a7-118">Data type</span></span></p></th>
<th><p><span data-ttu-id="7d6a7-119">説明</span><span class="sxs-lookup"><span data-stu-id="7d6a7-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d6a7-120"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="7d6a7-120"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="7d6a7-121">テキスト</span><span class="sxs-lookup"><span data-stu-id="7d6a7-121">Text</span></span></p></td>
<td><p><span data-ttu-id="7d6a7-122">このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-122">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d6a7-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="7d6a7-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="7d6a7-124">メモ</span><span class="sxs-lookup"><span data-stu-id="7d6a7-124">Memo</span></span></p></td>
<td><p><span data-ttu-id="7d6a7-125">リボンのカスタマイズを定義するリボン機能拡張 XML (RibbonX) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-125">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="7d6a7-126">プログラムでリボン機能拡張 XML を読み込む</span><span class="sxs-lookup"><span data-stu-id="7d6a7-126">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="7d6a7-p105">**[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** メソッドを使用してリボンのカスタマイズをプログラムで読み込むことができます。通常、リボンを作成し、そのリボンをアプリケーションで使用できるようにするには、まず、リボンの名前と XML カスタマイズ マークアップを渡して **LoadCustomUI** メソッドを呼び出すプロシージャを使用して、データベースにモジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-p105">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>

<span data-ttu-id="7d6a7-p106">XML マークアップには、テーブルから作成される **Recordset** オブジェクト、データベース外部のソース (文字列に解析する XML ファイルなど)、またはプロシージャの内部に直接埋め込まれた XML マークアップを指定できます。各リボンの名前およびリボンを構成するタブの **id** 属性が一意である限り、 **LoadCustomUI** メソッドへの呼び出しを複数回使用し、それぞれに異なる XML マークアップを渡すことで、異なるリボンを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-p106">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="7d6a7-p107">プロシージャが完了したら、"RunCode/プロシージャの実行" アクションを使用してプロシージャを呼び出す AutoExec マクロを作成します。これにより、アプリケーションが開始されたときに **LoadCustomUI** メソッドが自動的に実行され、すべてのカスタム リボンをアプリケーションで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-p107">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="7d6a7-133">フォームやレポートにカスタム リボンを割り当てる</span><span class="sxs-lookup"><span data-stu-id="7d6a7-133">Assign custom ribbons to forms or reports</span></span>

1.  <span data-ttu-id="7d6a7-134">前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-134">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="7d6a7-135">デザイン ビューでフォームまたはレポートを開きます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-135">Open the form or report in Design view.</span></span>

3.  <span data-ttu-id="7d6a7-136">[デザイン] タブの [**プロパティ シート**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-136">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="7d6a7-137">[プロパティ] ウィンドウの [**すべて**] タブで、[**リボン名**] リストを選択し、リボンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-137">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>

5.  <span data-ttu-id="7d6a7-138">フォームまたはレポートを保存して閉じ、再度開きます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-138">Save, close, and then reopen the form or report.</span></span> <span data-ttu-id="7d6a7-139">選択した リボン UI が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-139">The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="7d6a7-p109">リボン UI に表示されるタブは付加的なものです。つまり、特にタブを非表示にしない限り、また *Start from Scratch* 属性を **True** に設定しない限り、フォームまたはレポートのリボン ユーザー インターフェイスは既存のタブに付加されて表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-p109">The tabs displayed in the ribbon UI are additive. That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="7d6a7-142">[!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7d6a7-142">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


