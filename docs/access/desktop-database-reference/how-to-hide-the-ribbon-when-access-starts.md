---
title: Access の起動時にリボンを非表示にする
TOCTitle: Hide the ribbon when Access starts
description: Access 2013 のすべての組み込みタブが非表示になっているカスタマイズされたリボンを読み込む方法について説明します。
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 384a575ae5e15b75ba7b0b891529c695cc3de599
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537830"
---
# <a name="hide-the-ribbon-when-access-starts"></a><span data-ttu-id="81745-103">Access の起動時にリボンを非表示にする</span><span class="sxs-lookup"><span data-stu-id="81745-103">Hide the ribbon when Access starts</span></span>

<span data-ttu-id="81745-104">**適用先**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="81745-104">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="81745-p101">既定では、Microsoft Access にはリボンを非表示にする方法は用意されていません。このトピックでは、すべての組み込みタブが非表示になっているカスタマイズされたリボンを読み込む方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="81745-p101">By default, Microsoft Access does not provide a method for hiding the ribbon. This topic describes how to load a customized ribbon that hides all of the built-in tabs.</span></span>

<span data-ttu-id="81745-107">Access の起動時にカスタマイズされたリボンを読み込むには、その設定を **USysRibbons** という名前のテーブルに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81745-107">To load the customized ribbon when Access starts, you should store its settings in a table named **USysRibbons**.</span></span>

<span data-ttu-id="81745-108">リボンのカスタマイズを実装するには、特定の列名を使用して **USysRibbons** テーブルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81745-108">The **USysRibbons** table must be created using specific column names for the ribbon customizations to be implemented.</span></span> 

<span data-ttu-id="81745-109">次のテーブルは、**USysRibbons** テーブルを作成するときに使用する設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="81745-109">The following table lists the settings to use when creating the **USysRibbons** table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81745-110">列名</span><span class="sxs-lookup"><span data-stu-id="81745-110">Column name</span></span></p></th>
<th><p><span data-ttu-id="81745-111">データ型</span><span class="sxs-lookup"><span data-stu-id="81745-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="81745-112">説明</span><span class="sxs-lookup"><span data-stu-id="81745-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81745-113"><strong>RibbonName</strong></span><span class="sxs-lookup"><span data-stu-id="81745-113"><strong>RibbonName</strong></span></span></p></td>
<td><p><span data-ttu-id="81745-114">テキスト</span><span class="sxs-lookup"><span data-stu-id="81745-114">Text</span></span></p></td>
<td><p><span data-ttu-id="81745-115">このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="81745-115">Contains the name of the custom ribbon to be associated with this customization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81745-116"><strong>RibbonXML</strong></span><span class="sxs-lookup"><span data-stu-id="81745-116"><strong>RibbonXML</strong></span></span></p></td>
<td><p><span data-ttu-id="81745-117">メモ</span><span class="sxs-lookup"><span data-stu-id="81745-117">Memo</span></span></p></td>
<td><p><span data-ttu-id="81745-118">リボンのカスタマイズを定義するリボン機能拡張 XML (RibbonX) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="81745-118">Contains the ribbon extensibility XML (RibbonX) that defines the ribbon customization.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="81745-119">次のテーブルは、**USysRibbons** テーブルに格納するリボンのカスタマイズ設定の一覧です。</span><span class="sxs-lookup"><span data-stu-id="81745-119">The following table lists the ribbon customization settings to store in the **USysRibbons** table.</span></span>

|<span data-ttu-id="81745-120">列名</span><span class="sxs-lookup"><span data-stu-id="81745-120">Column name</span></span>|<span data-ttu-id="81745-121">値</span><span class="sxs-lookup"><span data-stu-id="81745-121">Value</span></span>|
|:----------|:----|
|<span data-ttu-id="81745-122">**RibbonName**</span><span class="sxs-lookup"><span data-stu-id="81745-122">**RibbonName**</span></span>|<span data-ttu-id="81745-123">HideTheRibbon</span><span class="sxs-lookup"><span data-stu-id="81745-123">HideTheRibbon</span></span>|
|<span data-ttu-id="81745-124">**RibbonXML**</span><span class="sxs-lookup"><span data-stu-id="81745-124">**RibbonXML**</span></span>|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a><span data-ttu-id="81745-125">Access の起動時にカスタム リボンを適用する</span><span class="sxs-lookup"><span data-stu-id="81745-125">Apply a custom ribbon when Access starts</span></span>

<span data-ttu-id="81745-126">アプリケーションの起動時にカスタム リボン UI を使用できるように適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="81745-126">To apply a custom ribbon so that it is available when the application starts, use the following procedure:</span></span>

1.  <span data-ttu-id="81745-127">前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="81745-127">Follow the process described previously to make the customized ribbon available to the application.</span></span>

2.  <span data-ttu-id="81745-128">アプリケーションを閉じて、再起動します。</span><span class="sxs-lookup"><span data-stu-id="81745-128">Close and then restart the application.</span></span>

3.  <span data-ttu-id="81745-129">[**Microsoft Office ボタン**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")] を選択し、[**Access のオプション**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="81745-129">Choose the **Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), and then choose **Access Options**.</span></span>

4.  <span data-ttu-id="81745-130">[**カレント データベース**] オプションを選択し、[**リボンとツール バーのオプション**] セクションで [**リボン名**] 一覧を選択して [**HideTheRibbon** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="81745-130">Choose the **Current Database** option and then, in the **Ribbon and Toolbar Options** section, choose the **Ribbon Name** list and select **HideTheRibbon**.</span></span>

5.  <span data-ttu-id="81745-131">アプリケーションを閉じて、再起動します。</span><span class="sxs-lookup"><span data-stu-id="81745-131">Close and then restart the application.</span></span>

> [!NOTE]
> <span data-ttu-id="81745-132">[!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81745-132">For more information about the ribbon UI in other Office applications, see [Overview of the Office Fluent Ribbon](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).</span></span>


