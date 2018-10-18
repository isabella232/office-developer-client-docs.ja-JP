---
<span data-ttu-id="9e0fc-101">タイトル: フォームにカスタム リボンを適用するか、TOCTitle を報告する: フォームまたはレポートにカスタム リボンを適用する <<<<<<< ヘッド ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 2015/09/18 ====== 説明: フォームまたはレポートを Access 2013 での読み込み時に、カスタマイズされたリボンを適用する方法です。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-101">title: Apply a custom ribbon to a form or report TOCTitle: Apply a custom ribbon to a form or report <<<<<<< HEAD ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 09/18/2015 ======= description: How to apply customized ribbons when loading a form or report in Access 2013.</span></span>
<span data-ttu-id="9e0fc-102">ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 2018/10/16</span><span class="sxs-lookup"><span data-stu-id="9e0fc-102">ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: 48545865 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="9e0fc-103">マスター mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="9e0fc-103">master mtps_version: v=office.15</span></span>
---

# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a><span data-ttu-id="9e0fc-104">フォームまたはレポートにカスタム リボンを適用します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-104">Apply a custom ribbon to a form or report</span></span>

<span data-ttu-id="9e0fc-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9e0fc-105"><<<<<<< HEAD</span></span>

<span data-ttu-id="9e0fc-106">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e0fc-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9e0fc-p102">リボンでは、リボン XML の作成およびカスタマイズを簡素化するテキストベースの宣言型 XML マークアップが使用されています。XML を数行記述するだけで、ユーザーに最適なインターフェイスを作成できます。Access では、柔軟にリボン ユーザー インターフェイスをカスタマイズできます。たとえば、カスタマイズしたマークアップをテーブルまたは別の Access データベースに格納する、VBA プロシージャに埋め込む、Excel のワークシートと関連付けるなどの操作ができます。このトピックでは、フォームまたはレポートを読み込むときにカスタマイズしたリボンを適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-p102">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon. With a few lines of XML, you can create just the right interface for the user. Access provides flexibility in customizing the ribbon user interface. For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet. This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="making-the-ribbon-customization-xml-available"></a><span data-ttu-id="9e0fc-112">リボンのカスタマイズ XML を使用できるようにする</span><span class="sxs-lookup"><span data-stu-id="9e0fc-112">Making the Ribbon Customization XML Available</span></span>

<span data-ttu-id="9e0fc-113">**リボン機能拡張 XML をテーブルに保管する**</span><span class="sxs-lookup"><span data-stu-id="9e0fc-113">**Storing Ribbon Extensibility XML in a Table**</span></span>

<span data-ttu-id="9e0fc-p103">リボンのカスタマイズを使用できるようにするための 1 つの方法は、リボンのカスタマイズをテーブルに保管することです。カスタマイズを " **USysRibbons** " という名前のテーブルに保管した場合、マクロまたは VBA コードを使用せずにカスタマイズを実装できます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-p103">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="9e0fc-p104">**USysRibbons** は、ユーザーが作成するシステム テーブルです。リボンのカスタマイズを実装するには、特定の列名を使用してこのテーブルを作成する必要があります。 **USysRibbons** テーブルを作成するときに使用する設定の一覧を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-p104">**USysRibbons** is a user-created system table. The table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
=======
<span data-ttu-id="9e0fc-119">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e0fc-119">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9e0fc-120">リボンでは、リボン XML の作成およびカスタマイズを簡素化するテキストベースの宣言型 XML マークアップが使用されています。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-120">The ribbon uses text-based, declarative XML markup that simplifies creating and customizing the ribbon.</span></span> <span data-ttu-id="9e0fc-121">XML を数行記述するだけで、ユーザーに最適なインターフェイスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-121">With a few lines of XML, you can create just the right interface for the user.</span></span> <span data-ttu-id="9e0fc-122">Access では、柔軟にリボン ユーザー インターフェイスをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-122">Access provides flexibility in customizing the ribbon user interface.</span></span> 

<span data-ttu-id="9e0fc-123">たとえば、カスタマイズしたマークアップをテーブルまたは別の Access データベースに格納する、VBA プロシージャに埋め込む、Excel のワークシートと関連付けるなどの操作ができます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-123">For example, customization markup can be stored in a table, embedded in a VBA procedure, stored in another Access database, or linked to from an Excel worksheet.</span></span> <span data-ttu-id="9e0fc-124">このトピックでは、フォームまたはレポートを読み込むときにカスタマイズしたリボンを適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-124">This topic describes how to apply customized ribbons when loading a form or report.</span></span>

## <a name="make-the-ribbon-customization-xml-available"></a><span data-ttu-id="9e0fc-125">リボンのカスタマイズ XML を使用できるように</span><span class="sxs-lookup"><span data-stu-id="9e0fc-125">Make the ribbon customization XML available</span></span>

### <a name="store-ribbon-extensibility-xml-in-a-table"></a><span data-ttu-id="9e0fc-126">リボン機能拡張 XML をテーブルに格納します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-126">Store ribbon extensibility XML in a table</span></span>

<span data-ttu-id="9e0fc-p107">リボンのカスタマイズを使用できるようにするための 1 つの方法は、リボンのカスタマイズをテーブルに保管することです。カスタマイズを " **USysRibbons** " という名前のテーブルに保管した場合、マクロまたは VBA コードを使用せずにカスタマイズを実装できます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-p107">One method that you can use to make ribbon customizations available is to store them in a table. If you store the customizations in a table named **USysRibbons**, the customizations can be implemented without using macros or VBA code.</span></span>

<span data-ttu-id="9e0fc-129">**USysRibbons** は、ユーザーが作成するシステム テーブルです。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-129">**USysRibbons** is a user-created system table.</span></span> <span data-ttu-id="9e0fc-130">実装するリボンのカスタマイズの特定の列名を使用して、テーブルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-130">The table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="9e0fc-131">次の表に、 **USysRibbons** テーブルを作成するときに使用する設定を示します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-131">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="9e0fc-132">master</span><span class="sxs-lookup"><span data-stu-id="9e0fc-132">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="9e0fc-133"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9e0fc-133"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="9e0fc-134">列名</span><span class="sxs-lookup"><span data-stu-id="9e0fc-134">Column Name</span></span></p></th>
<th><p><span data-ttu-id="9e0fc-135">データ型</span><span class="sxs-lookup"><span data-stu-id="9e0fc-135">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="9e0fc-136">列名</span><span class="sxs-lookup"><span data-stu-id="9e0fc-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="9e0fc-137">データ型</span><span class="sxs-lookup"><span data-stu-id="9e0fc-137">Data type</span></span></p></th><span data-ttu-id="9e0fc-138">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="9e0fc-138">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="9e0fc-139">説明</span><span class="sxs-lookup"><span data-stu-id="9e0fc-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e0fc-140"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="9e0fc-140"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="9e0fc-141">テキスト型 (Text)</span><span class="sxs-lookup"><span data-stu-id="9e0fc-141">Text</span></span></p></td>
<span data-ttu-id="9e0fc-142"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9e0fc-142"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="9e0fc-143">このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-143">Contains the name of the custom ribbon to be associated with this customization</span></span></p></td>
=======
<td><p><span data-ttu-id="9e0fc-144">このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-144">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td><span data-ttu-id="9e0fc-145">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="9e0fc-145">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e0fc-146"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="9e0fc-146"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="9e0fc-147">メモ型 (Memo)</span><span class="sxs-lookup"><span data-stu-id="9e0fc-147">Memo</span></span></p></td>
<span data-ttu-id="9e0fc-148"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9e0fc-148"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="9e0fc-149">リボン、リボンのカスタマイズを定義する機能拡張 XML (RibbonX) が含まれています</span><span class="sxs-lookup"><span data-stu-id="9e0fc-149">Contains the ribbon Extensibility XML (RibbonX) that defines the ribbon customization</span></span></p></td>
=======
<td><p><span data-ttu-id="9e0fc-150">リボン機能拡張 (RibbonX)、リボンのカスタマイズを定義する XML が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-150">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="9e0fc-151">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="9e0fc-151">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>


<span data-ttu-id="9e0fc-152"><<<<<<< ヘッドの**プログラムを使用して、リボン機能拡張 XML を読み込み中**</span><span class="sxs-lookup"><span data-stu-id="9e0fc-152"><<<<<<< HEAD **Loading Ribbon Extensibility XML Programmatically**</span></span>

<span data-ttu-id="9e0fc-p109">**[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** メソッドを使用してリボンのカスタマイズをプログラムで読み込むことができます。通常、リボンを作成し、そのリボンをアプリケーションで使用できるようにするには、まず、リボンの名前と XML カスタマイズ マークアップを渡して **LoadCustomUI** メソッドを呼び出すプロシージャを使用して、データベースにモジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-p109">You can use the **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a><span data-ttu-id="9e0fc-155">リボン機能拡張 XML をプログラムによって読み込む</span><span class="sxs-lookup"><span data-stu-id="9e0fc-155">Load ribbon extensibility XML programmatically</span></span>

<span data-ttu-id="9e0fc-p110">**[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** メソッドを使用してリボンのカスタマイズをプログラムで読み込むことができます。通常、リボンを作成し、そのリボンをアプリケーションで使用できるようにするには、まず、リボンの名前と XML カスタマイズ マークアップを渡して **LoadCustomUI** メソッドを呼び出すプロシージャを使用して、データベースにモジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-p110">You can use the **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** method to load ribbon customizations programmatically. Typically, to create and make the ribbon available to the application, you first create a module in the database with a procedure that calls the **LoadCustomUI** method, passing in the name of the ribbon and the XML customization markup.</span></span>
>>>>>>> <span data-ttu-id="9e0fc-158">master</span><span class="sxs-lookup"><span data-stu-id="9e0fc-158">master</span></span>

<span data-ttu-id="9e0fc-p111">XML マークアップには、テーブルから作成される **Recordset** オブジェクト、データベース外部のソース (文字列に解析する XML ファイルなど)、またはプロシージャの内部に直接埋め込まれた XML マークアップを指定できます。各リボンの名前およびリボンを構成するタブの **id** 属性が一意である限り、 **LoadCustomUI** メソッドへの呼び出しを複数回使用し、それぞれに異なる XML マークアップを渡すことで、異なるリボンを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-p111">The XML markup can come from a **Recordset** object created from a table, from a source external to the database such as an XML file that you parse into a string, or from XML markup embedded directly inside the procedure. You can make different ribbons using multiple calls to the **LoadCustomUI** method, passing in different XML markup as long as the name of each ribbon and the **id** attribute of the tabs that make up the ribbon are unique.</span></span>

<span data-ttu-id="9e0fc-p112">プロシージャが完了したら、"RunCode/プロシージャの実行" アクションを使用してプロシージャを呼び出す AutoExec マクロを作成します。これにより、アプリケーションが開始されたときに **LoadCustomUI** メソッドが自動的に実行され、すべてのカスタム リボンをアプリケーションで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-p112">After the procedure is complete, you then create an AutoExec macro that calls the procedure by using the RunCode action. That way, when the application is started, the **LoadCustomUI** method is automatically executed and all of the custom ribbons are made available to the application.</span></span>

<span data-ttu-id="9e0fc-163"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9e0fc-163"><<<<<<< HEAD</span></span>
## <a name="assigning-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="9e0fc-164">カスタム リボンをフォームまたはレポートに割り当てる</span><span class="sxs-lookup"><span data-stu-id="9e0fc-164">Assigning Custom Ribbons to Forms or Reports</span></span>
=======
## <a name="assign-custom-ribbons-to-forms-or-reports"></a><span data-ttu-id="9e0fc-165">フォームまたはレポートにカスタム リボンを割り当てる</span><span class="sxs-lookup"><span data-stu-id="9e0fc-165">Assign custom ribbons to forms or reports</span></span>
>>>>>>> <span data-ttu-id="9e0fc-166">master</span><span class="sxs-lookup"><span data-stu-id="9e0fc-166">master</span></span>

1.  <span data-ttu-id="9e0fc-167">前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-167">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="9e0fc-168">デザイン ビューでフォームまたはレポートを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-168">Open the form or report in Design view.</span></span>

<span data-ttu-id="9e0fc-169"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9e0fc-169"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="9e0fc-170">[デザイン] タブの [ **プロパティ シート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-170">On the Design tab, click **Property Sheet**.</span></span>

4.  <span data-ttu-id="9e0fc-171">[プロパティ] ウィンドウの [ **すべて**] タブで、[ **リボン名**] ボックスをクリックし、リボンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-171">On the **All** tab of the Property window, click the **Ribbon Name** list and then select a ribbon.</span></span>
=======
3.  <span data-ttu-id="9e0fc-172">[デザイン] タブで、**プロパティ シート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-172">On the Design tab, choose **Property Sheet**.</span></span>

4.  <span data-ttu-id="9e0fc-173">[プロパティ] ウィンドウの [**すべて**] タブで、[**リボン名**] ボックスの一覧を選択し、リボンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-173">On the **All** tab of the Property window, choose the **Ribbon Name** list and then select a ribbon.</span></span>
>>>>>>> <span data-ttu-id="9e0fc-174">master</span><span class="sxs-lookup"><span data-stu-id="9e0fc-174">master</span></span>

5.  <span data-ttu-id="9e0fc-p113">フォームまたはレポートを保存して閉じ、再度開きます。選択した リボン UI が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-p113">Save, close, and then reopen the form or report. The ribbon UI you selected is displayed.</span></span>


> [!NOTE]
> <span data-ttu-id="9e0fc-177">[!メモ] リボン UI に表示されるタブは付加的なものです。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-177">The tabs displayed in the ribbon UI are additive.</span></span> <span data-ttu-id="9e0fc-178">具体的には、タブを非表示にするか、*最初から*属性を**True**に設定、しない限り、フォームのタブが表示されますか、レポートのリボンのユーザー インターフェイスは、既存のタブに追加します。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-178">That is, unless you specifically hide the tabs or set the *Start from Scratch* attribute to **True**, the tabs displayed in a form's or report's ribbon user interface are in addition to the existing tabs.</span></span>

> [!NOTE]
> <span data-ttu-id="9e0fc-179">[!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e0fc-179">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


