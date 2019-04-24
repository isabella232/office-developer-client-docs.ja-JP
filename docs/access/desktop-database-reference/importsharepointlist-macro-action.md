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
# <a name="importsharepointlist-macro-action"></a>ImportSharePointList マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。 

## <a name="setting"></a>設定値

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
<td><p><strong>Transfer Type/変換の種類</strong></p></td>
<td><p>変換の種類を指定します。</p>
<ul>
<li><p>[<strong>インポート</strong>] を選択して、Microsoft access のテーブルに SharePoint Foundation データをコピーします。 Access のデータを更新しても、SharePoint Foundation のデータには影響しません。 同様に、SharePoint Foundation のデータを更新しても、Access のデータには影響しません。</p></li>
<li><p>[<strong>リンク</strong>] を選択して、SharePoint Foundation のデータにリンクするリンクテーブルを Access に作成します。 Access のデータに対する更新は、SharePoint Foundation に反映されます。 同様に、SharePoint Foundation のデータに対する更新は Access に反映されます。</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Site Address/サイトのアドレス</strong></p></td>
<td><p>SharePoint サイトの完全パスを入力します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>List ID/リスト ID</strong></p></td>
<td><p>変換するリストの名前または GUID を入力します。 この引数は省略できません。</p></td>
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
    
  3. Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view. The GUID for the list follows **List=**, and the GUID for the view follows **View=**. However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**. 次に例を示します。
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  address の guid をこのマクロアクションの引数として使用するには、各 **% 7b**文字列を **{** 文字に置き換え、各 **% 2d**文字列を**-** 文字に置き換え、各% **7d**文字列を次のように置き換えます。**}** 文字 Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.

