---
title: ImportSharePointList マクロ アクション
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291860"
---
# <a name="importsharepointlist-macro-action"></a><span data-ttu-id="bfbc1-102">ImportSharePointList マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="bfbc1-102">ImportSharePointList macro action</span></span>

<span data-ttu-id="bfbc1-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfbc1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bfbc1-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span><span class="sxs-lookup"><span data-stu-id="bfbc1-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span></span>

> [!NOTE]
> <span data-ttu-id="bfbc1-105">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="bfbc1-106">設定値</span><span class="sxs-lookup"><span data-stu-id="bfbc1-106">Setting</span></span>

<span data-ttu-id="bfbc1-107">"ImportSharePointList/SharePointリストのインポート" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-107">The **ImportSharePointList** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bfbc1-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="bfbc1-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="bfbc1-109">説明</span><span class="sxs-lookup"><span data-stu-id="bfbc1-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfbc1-110"><strong>Transfer Type/変換の種類</strong></span><span class="sxs-lookup"><span data-stu-id="bfbc1-110"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="bfbc1-111">変換の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-111">Select the type of transfer.</span></span></p>
<ul>
<li><p><span data-ttu-id="bfbc1-112">[<strong>インポート</strong>] を選択して、Microsoft access のテーブルに SharePoint Foundation データをコピーします。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-112">Select <strong>Import</strong> to copy the SharePoint Foundation data into a table in Microsoft Access.</span></span> <span data-ttu-id="bfbc1-113">Access のデータを更新しても、SharePoint Foundation のデータには影響しません。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-113">Updates to the data in Access do not affect the data in SharePoint Foundation.</span></span> <span data-ttu-id="bfbc1-114">同様に、SharePoint Foundation のデータを更新しても、Access のデータには影響しません。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-114">Likewise, updates to the data in SharePoint Foundation do not affect the data in Access.</span></span></p></li>
<li><p><span data-ttu-id="bfbc1-115">[<strong>リンク</strong>] を選択して、SharePoint Foundation のデータにリンクするリンクテーブルを Access に作成します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-115">Select <strong>Link</strong> to create a linked table in Access that links to the data in SharePoint Foundation.</span></span> <span data-ttu-id="bfbc1-116">Access のデータに対する更新は、SharePoint Foundation に反映されます。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-116">Updates to the data in Access are reflected in SharePoint Foundation.</span></span> <span data-ttu-id="bfbc1-117">同様に、SharePoint Foundation のデータに対する更新は Access に反映されます。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-117">Likewise, updates to the data in SharePoint Foundation are reflected in Access.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfbc1-118"><strong>Site Address/サイトのアドレス</strong></span><span class="sxs-lookup"><span data-stu-id="bfbc1-118"><strong>Site Address</strong></span></span></p></td>
<td><p><span data-ttu-id="bfbc1-119">SharePoint サイトの完全パスを入力します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-119">Enter the full path of the SharePoint site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfbc1-120"><strong>List ID/リスト ID</strong></span><span class="sxs-lookup"><span data-stu-id="bfbc1-120"><strong>List ID</strong></span></span></p></td>
<td><p><span data-ttu-id="bfbc1-121">変換するリストの名前または GUID を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-121">Enter the name or GUID of the list to be transferred.</span></span> <span data-ttu-id="bfbc1-122">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-122">Required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfbc1-123"><strong>View ID/ビュー ID</strong></span><span class="sxs-lookup"><span data-stu-id="bfbc1-123"><strong>View ID</strong></span></span></p></td>
<td><p><span data-ttu-id="bfbc1-p104">使用するリストのビューの GUID を入力します。リストのすべての行と列を変換する場合は、この引数を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-p104">Enter the GUID of the view for the list you want to use. Leave this argument blank to transfer all rows and columns in the list.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfbc1-126"><strong>Table Name/テーブル名</strong></span><span class="sxs-lookup"><span data-stu-id="bfbc1-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="bfbc1-127">Access で表示されるテーブルまたはリンク テーブルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-127">Enter the name you want displayed for the table or linked table in Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfbc1-128"><strong>Get Lookup Display Values/ルックアップ表示値の取得</strong></span><span class="sxs-lookup"><span data-stu-id="bfbc1-128"><strong>Get Lookup Display Values</strong></span></span></p></td>
<td><p><span data-ttu-id="bfbc1-129">ルックアップの実行に使用される ID の代わりにルックアップ フィールドの表示値を変換する場合は [<strong>はい</strong>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-129">Select <strong>Yes</strong> to transfer display values for Lookup fields instead of the ID used to perform the lookup.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bfbc1-130">注釈</span><span class="sxs-lookup"><span data-stu-id="bfbc1-130">Remarks</span></span>

- <span data-ttu-id="bfbc1-131">このアクションの動作は、[ **外部データ**] タブの [ **インポート**] で [ **SharePoint リスト**] をクリックした場合の動作と同じです。このアクションでは、外部データの取り込みウィザードで選択した引数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-131">This action has the same effect as clicking **SharePoint List** in the **Import** group on the **External Data** tab. The arguments for the action correspond to the choices you make in the Get External Data Wizard.</span></span>

- <span data-ttu-id="bfbc1-132">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="bfbc1-132">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="bfbc1-133">存在しないリストまたはビューを指定しても、エラーは発生しませんが、データは変換されません。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-133">If you specify a nonexistent list or view, no error occurs, and no data is transferred.</span></span>

- <span data-ttu-id="bfbc1-p105">GUID とは、リストまたはビューの一意の 16 進数の識別子です。GUID は、次の形式で入力する必要があります。"F" は 16 進数 (0 ～ 9、A ～ F) を表します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-p105">A GUID is a unique hexadecimal identifier for a list or a view. A GUID must be entered in the following format, where each "F" is a hexadecimal number (0 through 9 or A through F).</span></span>
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  <span data-ttu-id="bfbc1-136">SharePoint サイトからリストまたはビューの GUID を取得するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-136">You can obtain the GUID for a list or view from the SharePoint site by using the following procedure:</span></span>
    
  1. <span data-ttu-id="bfbc1-137">SharePoint Foundation でリストを開きます。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-137">Open the list in SharePoint Foundation.</span></span>
    
  2. <span data-ttu-id="bfbc1-138">対象のビューが表示されていない場合は、[ **ビュー**] ボックスの矢印をクリックし、対象のビューを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-138">If the view you want is not displayed, click the **View** drop-down arrow and then select the view you want.</span></span>
    
  3. <span data-ttu-id="bfbc1-139">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span><span class="sxs-lookup"><span data-stu-id="bfbc1-139">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span></span> <span data-ttu-id="bfbc1-140">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span><span class="sxs-lookup"><span data-stu-id="bfbc1-140">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span></span> <span data-ttu-id="bfbc1-141">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span><span class="sxs-lookup"><span data-stu-id="bfbc1-141">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span></span> <span data-ttu-id="bfbc1-142">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="bfbc1-142">For example:</span></span>
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  <span data-ttu-id="bfbc1-143">address の guid をこのマクロアクションの引数として使用するには、各 **% 7b**文字列を **{** 文字に置き換え、各 **% 2d**文字列を**-** 文字に置き換え、各% **7d**文字列を次のように置き換えます。**}** 文字</span><span class="sxs-lookup"><span data-stu-id="bfbc1-143">Before you can use the GUIDs from the address as arguments in this macro action, you must replace each **%7B** string with the **{** character, replace each **%2D** string with the **-** character, and replace each **%7D** string with the **}** character.</span></span> <span data-ttu-id="bfbc1-144">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span><span class="sxs-lookup"><span data-stu-id="bfbc1-144">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span></span>

