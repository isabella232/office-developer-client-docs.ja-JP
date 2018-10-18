---
<span data-ttu-id="ee923-101">タイトル: アクセスは、TOCTitle を起動したときにリボンを非表示: Access の起動時にリボンを非表示にする <<<<<<< ヘッド ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 2015/09/18 ===説明: すべての Access 2013 の組み込みタブを非表示にするカスタマイズされたリボンを読み込む方法です。</span><span class="sxs-lookup"><span data-stu-id="ee923-101">title: Hide the ribbon when Access starts TOCTitle: Hide the ribbon when Access starts <<<<<<< HEAD ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 09/18/2015 ======= description: How to load a customized ribbon that hides all of the built-in tabs in Access 2013.</span></span>
<span data-ttu-id="ee923-102">ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 2018/10/16</span><span class="sxs-lookup"><span data-stu-id="ee923-102">ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="ee923-103">マスター mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ee923-103">master mtps_version: v=office.15</span></span>
---

# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="ee923-104">Access の起動時にリボンを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="ee923-104">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="ee923-105">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee923-105">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="ee923-p102">既定では、Microsoft Access にはリボンを非表示にする方法は用意されていません。このトピックでは、すべての組み込みタブが非表示になっているカスタマイズされたリボンを読み込む方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ee923-p102">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="ee923-108">Access の起動時にカスタマイズされたリボンを読み込むには、その設定を **USysRibbons** という名前のテーブルに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee923-108">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="ee923-109"><<<<<<< ヘッドを実装するのには、リボンをカスタマイズするために特定の列名を使用して**USysRibbons**テーブルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee923-109"><<<<<<< HEAD The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented.</span></span> <span data-ttu-id="ee923-110">次の表に、 **USysRibbons** テーブルを作成するときに使用する設定を示します。</span><span class="sxs-lookup"><span data-stu-id="ee923-110">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
<span data-ttu-id="ee923-111">=== リボンのカスタマイズの特定の列名を使用して実装することを、 **USysRibbons**テーブルを作成しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ee923-111">======= The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="ee923-112">次の表に、 **USysRibbons** テーブルを作成するときに使用する設定を示します。</span><span class="sxs-lookup"><span data-stu-id="ee923-112">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>
>>>>>>> <span data-ttu-id="ee923-113">master</span><span class="sxs-lookup"><span data-stu-id="ee923-113">master</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<span data-ttu-id="ee923-114"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="ee923-114"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="ee923-115">列名</span><span class="sxs-lookup"><span data-stu-id="ee923-115">Column Name</span></span></p></th>
<th><p><span data-ttu-id="ee923-116">データ型</span><span class="sxs-lookup"><span data-stu-id="ee923-116">Data Type</span></span></p></th>
=======
<th><p><span data-ttu-id="ee923-117">列名</span><span class="sxs-lookup"><span data-stu-id="ee923-117">Column name</span></span></p></th>
<th><p><span data-ttu-id="ee923-118">データ型</span><span class="sxs-lookup"><span data-stu-id="ee923-118">Data type</span></span></p></th><span data-ttu-id="ee923-119">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="ee923-119">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="ee923-120">説明</span><span class="sxs-lookup"><span data-stu-id="ee923-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee923-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="ee923-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="ee923-122">テキスト型 (Text)</span><span class="sxs-lookup"><span data-stu-id="ee923-122">Text</span></span></p></td>
<td><p><span data-ttu-id="ee923-123">このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee923-123">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee923-124"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="ee923-124"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="ee923-125">メモ型 (Memo)</span><span class="sxs-lookup"><span data-stu-id="ee923-125">Memo</span></span></p></td>
<span data-ttu-id="ee923-126"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="ee923-126"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="ee923-127">リボンのカスタマイズを定義するリボン拡張 XML (RibbonX) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee923-127">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
=======
<td><p><span data-ttu-id="ee923-128">リボン機能拡張 (RibbonX)、リボンのカスタマイズを定義する XML が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee923-128">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td><span data-ttu-id="ee923-129">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="ee923-129">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<span data-ttu-id="ee923-130"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="ee923-130"><<<<<<< HEAD</span></span>

<span data-ttu-id="ee923-131">次の表に、 **USysRibbons** テーブルに保存するリボンのカスタマイズ設定を示します。</span><span class="sxs-lookup"><span data-stu-id="ee923-131">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee923-132">列名</span><span class="sxs-lookup"><span data-stu-id="ee923-132">Column Name</span></span></p></th>
<th><p><span data-ttu-id="ee923-133">値</span><span class="sxs-lookup"><span data-stu-id="ee923-133">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee923-134"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="ee923-134"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="ee923-135">して HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="ee923-135">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee923-136"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="ee923-136"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="ee923-137">&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot。&gt; &lt;リボンの startFromScratch =&quot;真&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="ee923-137">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="ee923-138">Access の起動時にカスタム リボンを適用する</span><span class="sxs-lookup"><span data-stu-id="ee923-138">Applying a Custom Ribbon When Access Starts</span></span>
=======
<br/>

<span data-ttu-id="ee923-139">次の表に、 **USysRibbons** テーブルに保存するリボンのカスタマイズ設定を示します。</span><span class="sxs-lookup"><span data-stu-id="ee923-139">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="ee923-140">列名</span><span class="sxs-lookup"><span data-stu-id="ee923-140">Column name</span></span>|<span data-ttu-id="ee923-141">値</span><span class="sxs-lookup"><span data-stu-id="ee923-141">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="ee923-142">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="ee923-142">**RibbonName**</span></span>|<span data-ttu-id="ee923-143">して HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="ee923-143">HideTheRibbon</span></span>|
|<span data-ttu-id="ee923-144">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="ee923-144">**RibbonXML**</span></span>|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="ee923-145">Access の起動時にカスタム リボンを適用します。</span><span class="sxs-lookup"><span data-stu-id="ee923-145">Apply a custom ribbon when Access starts</span></span>
>>>>>>> <span data-ttu-id="ee923-146">master</span><span class="sxs-lookup"><span data-stu-id="ee923-146">master</span></span>

<span data-ttu-id="ee923-147">アプリケーションの起動時にカスタム リボン UI を使用できるように適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ee923-147">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="ee923-148">前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ee923-148">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="ee923-149">アプリケーションを閉じて、再起動します。</span><span class="sxs-lookup"><span data-stu-id="ee923-149">Close and then restart the application.</span></span>

<span data-ttu-id="ee923-150"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="ee923-150"><<<<<<< HEAD</span></span>
3.  <span data-ttu-id="ee923-151">**Microsoft Office ボタン**をクリックして![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") [ **Access のオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ee923-151">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="ee923-152">[ **カレント データベース**] オプションをクリックし、[ **リボンとツール バーのオプション**] セクションで [ **リボン名**] ボックスの一覧をクリックして [ **HideTheRibbon** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee923-152">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
=======
3.  <span data-ttu-id="ee923-153">**Microsoft Office ボタン**をクリックして![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")、し、 **[Access のオプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee923-153">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="ee923-154">**カレント データベース**] オプションを選択し、**リボンとツールバーのオプション**] セクションで、[**リボン名**] ボックスの一覧を選択**して HideTheRibbon**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ee923-154">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>
>>>>>>> <span data-ttu-id="ee923-155">master</span><span class="sxs-lookup"><span data-stu-id="ee923-155">master</span></span>

5.  <span data-ttu-id="ee923-156">アプリケーションを閉じて、再起動します。</span><span class="sxs-lookup"><span data-stu-id="ee923-156">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="ee923-157">[!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee923-157">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


