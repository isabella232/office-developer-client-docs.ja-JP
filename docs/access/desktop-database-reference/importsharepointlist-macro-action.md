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
ms.localizationpriority: medium
ms.openlocfilehash: 650429c53855f12cc90c51fb4307d84a5520fa3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594182"
---
# <a name="importsharepointlist-macro-action"></a>ImportSharePointList マクロ アクション

**適用先**: Access 2013、Office 2013

You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

"ImportSharePointList/SharePointリストのインポート" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Transfer Type/転送の種類</strong></p></td>
<td><p>変換の種類を指定します。</p>
<ul>
<li><p>[<strong>インポート] を</strong>選択して、SharePointデータを Microsoft Access のテーブルにコピーします。 Access のデータに対する更新は、SharePoint Foundation のデータには影響を与えかねない。 同様に、SharePoint Foundation のデータの更新は Access のデータには影響を与えかねない。</p></li>
<li><p>[<strong>リンク] を</strong>選択して、Access でリンクされたテーブルを作成し、このテーブルは、SharePointされます。 Access のデータに対する更新は、SharePointに反映されます。 同様に、財団のデータの更新SharePoint Access に反映されます。</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Site Address/サイトのアドレス</strong></p></td>
<td><p>SharePoint サイトの完全パスを入力します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>List ID/リスト ID</strong></p></td>
<td><p>変換するリストの名前または GUID を入力します。この引数は省略できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>View ID/ビュー ID</strong></p></td>
<td><p>使用するリストのビューの GUID を入力します。リストのすべての行と列を変換する場合は、この引数を指定しないでください。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Table Name/テーブル名</strong></p></td>
<td><p>Access で表示されるテーブルまたはリンク テーブルの名前を入力します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Get Lookup Display Values/ルックアップ表示値の取得</strong></p></td>
<td><p>ルックアップの実行に使用される ID の代わりにルックアップ フィールドの表示値を変換する場合は [<strong>はい</strong>] を選択します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

- このアクションの動作は、[ **外部データ**] タブの [ **インポート**] で [ **SharePoint リスト**] をクリックした場合の動作と同じです。このアクションでは、外部データの取り込みウィザードで選択した引数が使用されます。

- To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.

- 存在しないリストまたはビューを指定しても、エラーは発生しませんが、データは変換されません。

- GUID とは、リストまたはビューの一意の 16 進数の識別子です。GUID は、次の形式で入力する必要があります。"F" は 16 進数 (0 ～ 9、A ～ F) を表します。
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  SharePoint サイトからリストまたはビューの GUID を取得するには、次の手順を実行します。
    
  1. SharePoint Foundation でリストを開きます。
    
  2. 対象のビューが表示されていない場合は、[ **ビュー**] ボックスの矢印をクリックし、対象のビューを選択します。
    
  3. Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view. The GUID for the list follows **List=**, and the GUID for the view follows **View=**. However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**. 以下に例を示します。
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  このマクロ アクションでアドレスの GUID を引数として使用する前に、各 **%7B** 文字列を **{** 文字に置き換え、各 **%2D** 文字列を文字に置き換え、各 **-** **%7D** 文字列を **}** 文字に置き換える必要があります。 Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.

