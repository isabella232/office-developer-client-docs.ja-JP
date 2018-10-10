---
title: Access の起動時にリボンを非表示にします。
TOCTitle: Hide the ribbon when Access starts
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b2b3e28157662a585fa03353da92a598b96bd2c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476876"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="68641-102">Access の起動時にリボンを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="68641-102">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="68641-103">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="68641-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="68641-p101">既定では、Microsoft Access にはリボンを非表示にする方法は用意されていません。このトピックでは、すべての組み込みタブが非表示になっているカスタマイズされたリボンを読み込む方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68641-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="68641-106">Access の起動時にカスタマイズされたリボンを読み込むには、その設定を **USysRibbons** という名前のテーブルに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68641-106">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="68641-p102">リボンのカスタマイズを実装するには、特定の列名を使用して **USysRibbons** テーブルを作成する必要があります。次の表に、 **USysRibbons** テーブルを作成するときに使用する設定を示します。</span><span class="sxs-lookup"><span data-stu-id="68641-p102">The **USysRibbons** table must be created using specific column names in order for the ribbon customizations to be implemented. The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68641-109">列名</span><span class="sxs-lookup"><span data-stu-id="68641-109">Column Name</span></span></p></th>
<th><p><span data-ttu-id="68641-110">データ型</span><span class="sxs-lookup"><span data-stu-id="68641-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="68641-111">説明</span><span class="sxs-lookup"><span data-stu-id="68641-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68641-112"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="68641-112"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="68641-113">テキスト型 (Text)</span><span class="sxs-lookup"><span data-stu-id="68641-113">Text</span></span></p></td>
<td><p><span data-ttu-id="68641-114">このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="68641-114">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68641-115"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="68641-115"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="68641-116">メモ型 (Memo)</span><span class="sxs-lookup"><span data-stu-id="68641-116">Memo</span></span></p></td>
<td><p><span data-ttu-id="68641-117">リボンのカスタマイズを定義するリボン拡張 XML (RibbonX) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="68641-117">Contains the Ribbon Extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="68641-118">次の表に、 **USysRibbons** テーブルに保存するリボンのカスタマイズ設定を示します。</span><span class="sxs-lookup"><span data-stu-id="68641-118">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68641-119">列名</span><span class="sxs-lookup"><span data-stu-id="68641-119">Column Name</span></span></p></th>
<th><p><span data-ttu-id="68641-120">値</span><span class="sxs-lookup"><span data-stu-id="68641-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68641-121"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="68641-121"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="68641-122">して HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="68641-122">HideTheRibbon</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68641-123"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="68641-123"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="68641-124">&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot。&gt; &lt;リボンの startFromScratch =&quot;真&quot;/&gt;&lt;/CustomUI&gt;</span><span class="sxs-lookup"><span data-stu-id="68641-124">&lt;CustomUI xmlns=&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot;&gt; &lt;ribbon startFromScratch=&quot;true&quot;/&gt;&lt;/CustomUI&gt;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="68641-125">Access の起動時にカスタム リボンを適用する</span><span class="sxs-lookup"><span data-stu-id="68641-125">Applying a Custom Ribbon When Access Starts</span></span>

<span data-ttu-id="68641-126">アプリケーションの起動時にカスタム リボン UI を使用できるように適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="68641-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="68641-127">前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="68641-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="68641-128">アプリケーションを閉じて、再起動します。</span><span class="sxs-lookup"><span data-stu-id="68641-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="68641-129">**Microsoft Office ボタン**をクリックして![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") [ **Access のオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68641-129">Click the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") and then click **Access Options**.</span></span>

4.  <span data-ttu-id="68641-130">[ **カレント データベース**] オプションをクリックし、[ **リボンとツール バーのオプション**] セクションで [ **リボン名**] ボックスの一覧をクリックして [ **HideTheRibbon** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="68641-130">Click the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, click the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="68641-131">アプリケーションを閉じて、再起動します。</span><span class="sxs-lookup"><span data-stu-id="68641-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="68641-132">[!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68641-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


