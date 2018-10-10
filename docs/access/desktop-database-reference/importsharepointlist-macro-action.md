---
title: "'ImportSharePointList/SharePointリストのインポート' マクロ アクション"
TOCTitle: ImportSharePointList Macro Action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 246602826986af84bdfcff82ad3787eebb687060
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478907"
---
# <a name="importsharepointlist-macro-action"></a><span data-ttu-id="72dfe-102">"ImportSharePointList/SharePointリストのインポート" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="72dfe-102">ImportSharePointList Macro Action</span></span>

<span data-ttu-id="72dfe-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="72dfe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72dfe-104">**ImportSharePointList**アクションを使用するにはインポートまたは Microsoft SharePoint Foundation サイトからデータをリンクします。</span><span class="sxs-lookup"><span data-stu-id="72dfe-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span></span>

> [!NOTE]
> <span data-ttu-id="72dfe-p101">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72dfe-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>

## <a name="setting"></a><span data-ttu-id="72dfe-107">設定値</span><span class="sxs-lookup"><span data-stu-id="72dfe-107">Setting</span></span>

<span data-ttu-id="72dfe-108">**ImportSharePointList**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="72dfe-108">The **ImportSharePointList** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72dfe-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="72dfe-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="72dfe-110">説明</span><span class="sxs-lookup"><span data-stu-id="72dfe-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72dfe-111"><strong>Transfer Type/変換の種類</strong></span><span class="sxs-lookup"><span data-stu-id="72dfe-111"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="72dfe-112">変換の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-112">Select the type of transfer.</span></span></p>
<ul>
<li><p><span data-ttu-id="72dfe-113">SharePoint Foundation のデータを Microsoft Access のテーブルにコピーするのには<strong>インポート</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-113">Select <strong>Import</strong> to copy the SharePoint Foundation data into a table in Microsoft Access.</span></span> <span data-ttu-id="72dfe-114">Access でデータの更新は、SharePoint Foundation のデータには影響しません。</span><span class="sxs-lookup"><span data-stu-id="72dfe-114">Updates to the data in Access do not affect the data in SharePoint Foundation.</span></span> <span data-ttu-id="72dfe-115">同様に、SharePoint Foundation のデータを更新しても、Access でデータには影響しません。</span><span class="sxs-lookup"><span data-stu-id="72dfe-115">Likewise, updates to the data in SharePoint Foundation do not affect the data in Access.</span></span></p></li>
<li><p><span data-ttu-id="72dfe-116">SharePoint Foundation のデータにリンクする Access でリンク テーブルを作成する<strong>リンク</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-116">Select <strong>Link</strong> to create a linked table in Access that links to the data in SharePoint Foundation.</span></span> <span data-ttu-id="72dfe-117">SharePoint Foundation には、Access でデータの更新が反映されます。</span><span class="sxs-lookup"><span data-stu-id="72dfe-117">Updates to the data in Access are reflected in SharePoint Foundation.</span></span> <span data-ttu-id="72dfe-118">同様に、SharePoint Foundation でデータの更新は、アクセスに反映されます。</span><span class="sxs-lookup"><span data-stu-id="72dfe-118">Likewise, updates to the data in SharePoint Foundation are reflected in Access.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dfe-119"><strong>Site Address/サイトのアドレス</strong></span><span class="sxs-lookup"><span data-stu-id="72dfe-119"><strong>Site Address</strong></span></span></p></td>
<td><p><span data-ttu-id="72dfe-120">SharePoint サイトの完全パスを入力します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-120">Enter the full path of the SharePoint site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72dfe-121"><strong>List ID/リスト ID</strong></span><span class="sxs-lookup"><span data-stu-id="72dfe-121"><strong>List ID</strong></span></span></p></td>
<td><p><span data-ttu-id="72dfe-p104">変換するリストの名前または GUID を入力します。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="72dfe-p104">Enter the name or GUID of the list to be transferred. Required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dfe-124"><strong>View ID/ビュー ID</strong></span><span class="sxs-lookup"><span data-stu-id="72dfe-124"><strong>View ID</strong></span></span></p></td>
<td><p><span data-ttu-id="72dfe-p105">使用するリストのビューの GUID を入力します。リストのすべての行と列を変換する場合は、この引数を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="72dfe-p105">Enter the GUID of the view for the list you want to use. Leave this argument blank to transfer all rows and columns in the list.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72dfe-127"><strong>Table Name/テーブル名</strong></span><span class="sxs-lookup"><span data-stu-id="72dfe-127"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="72dfe-128">Access で表示されるテーブルまたはリンク テーブルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-128">Enter the name you want displayed for the table or linked table in Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72dfe-129"><strong>Get Lookup Display Values/ルックアップ表示値の取得</strong></span><span class="sxs-lookup"><span data-stu-id="72dfe-129"><strong>Get Lookup Display Values</strong></span></span></p></td>
<td><p><span data-ttu-id="72dfe-130">ルックアップの実行に使用される ID の代わりにルックアップ フィールドの表示値を変換する場合は [<strong>はい</strong>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-130">Select <strong>Yes</strong> to transfer display values for Lookup fields instead of the ID used to perform the lookup.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="72dfe-131">解説</span><span class="sxs-lookup"><span data-stu-id="72dfe-131">Remarks</span></span>

- <span data-ttu-id="72dfe-132">このアクションの動作は、[ **外部データ**] タブの [ **インポート**] で [ **SharePoint リスト**] をクリックした場合の動作と同じです。このアクションでは、外部データの取り込みウィザードで選択した引数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="72dfe-132">This action has the same effect as clicking **SharePoint List** in the **Import** group on the **External Data** tab. The arguments for the action correspond to the choices you make in the Get External Data Wizard.</span></span>

- <span data-ttu-id="72dfe-133">VBA モジュールでは、 **ImportSharePointList**アクションを実行するには、 **DoCmd**オブジェクトの**TransferSharePointList**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-133">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="72dfe-134">存在しないリストまたはビューを指定しても、エラーは発生しませんが、データは変換されません。</span><span class="sxs-lookup"><span data-stu-id="72dfe-134">If you specify a nonexistent list or view, no error occurs, and no data is transferred.</span></span>

- <span data-ttu-id="72dfe-p106">GUID とは、リストまたはビューの一意の 16 進数の識別子です。GUID は、次の形式で入力する必要があります。"F" は 16 進数 (0 ～ 9、A ～ F) を表します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-p106">A GUID is a unique hexadecimal identifier for a list or a view. A GUID must be entered in the following format, where each "F" is a hexadecimal number (0 through 9 or A through F).</span></span>
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  <span data-ttu-id="72dfe-137">SharePoint サイトからリストまたはビューの GUID を取得するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-137">You can obtain the GUID for a list or view from the SharePoint site by using the following procedure:</span></span>
    
  1. <span data-ttu-id="72dfe-138">SharePoint Foundation でリストを開きます。</span><span class="sxs-lookup"><span data-stu-id="72dfe-138">Open the list in SharePoint Foundation.</span></span>
    
  2. <span data-ttu-id="72dfe-139">対象のビューが表示されていない場合は、[ **ビュー**] ボックスの矢印をクリックし、対象のビューを選択します。</span><span class="sxs-lookup"><span data-stu-id="72dfe-139">If the view you want is not displayed, click the **View** drop-down arrow and then select the view you want.</span></span>
    
  3. <span data-ttu-id="72dfe-140">**ビュー**のドロップダウン矢印をクリックし、**このビューの変更**を選択します.ブラウザーのアドレス バーのアドレスには、リストとビューの両方の Guid が含まれています。</span><span class="sxs-lookup"><span data-stu-id="72dfe-140">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span></span> <span data-ttu-id="72dfe-141">リストの GUID に依存して**リスト =**、ビューの GUID に依存していると**ビュー =**。</span><span class="sxs-lookup"><span data-stu-id="72dfe-141">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span></span> <span data-ttu-id="72dfe-142">ただし、アドレスの各 **{** (左中かっこ) 文字は、文字列で表される、 **%7b**、各**-**(ハイフン) は、文字列で表される **%2 D**、 **}** (右中かっこ) 文字は、文字列**によって表されます%7 D**です。</span><span class="sxs-lookup"><span data-stu-id="72dfe-142">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span></span> <span data-ttu-id="72dfe-143">例:</span><span class="sxs-lookup"><span data-stu-id="72dfe-143">For example:</span></span>
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  <span data-ttu-id="72dfe-144">**%7 b**の各文字列を **{** 文字に置き換えて、各を置き換える必要がありますアドレスから Guid を使用するにはこのマクロ アクションの引数として、前に **%2 D**の文字列、**-** 文字、および**各 %7d と**を交換して、**}** 文字です。</span><span class="sxs-lookup"><span data-stu-id="72dfe-144">Before you can use the GUIDs from the address as arguments in this macro action, you must replace each **%7B** string with the **{** character, replace each **%2D** string with the **-** character, and replace each **%7D** string with the **}** character.</span></span> <span data-ttu-id="72dfe-145">含めないでください、 **&** (アンパサンド) に続く文字を **%7 D**の文字列リストの GUID です。</span><span class="sxs-lookup"><span data-stu-id="72dfe-145">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span></span>

