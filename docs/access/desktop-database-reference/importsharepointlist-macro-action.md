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
ms.openlocfilehash: 57c6630b1e9145c158a32a331ae91157e8e5e8f6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883072"
---
# <a name="importsharepointlist-macro-action"></a>"ImportSharePointList/SharePointリストのインポート" マクロ アクション

**適用されます**Access 2013、Office 2013。

**ImportSharePointList**アクションを使用するにはインポートまたは Microsoft SharePoint Foundation サイトからデータをリンクします。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。

## <a name="setting"></a>設定値

**ImportSharePointList**アクションには、次の引数があります。

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
<li><p>SharePoint Foundation のデータを Microsoft Access のテーブルにコピーするのには<strong>インポート</strong>を選択します。 Access でデータの更新は、SharePoint Foundation のデータには影響しません。 同様に、SharePoint Foundation のデータを更新しても、Access でデータには影響しません。</p></li>
<li><p>SharePoint Foundation のデータにリンクする Access でリンク テーブルを作成する<strong>リンク</strong>を選択します。 SharePoint Foundation には、Access でデータの更新が反映されます。 同様に、SharePoint Foundation でデータの更新は、アクセスに反映されます。</p></li>
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


## <a name="remarks"></a>解説

- このアクションの動作は、[ **外部データ**] タブの [ **インポート**] で [ **SharePoint リスト**] をクリックした場合の動作と同じです。このアクションでは、外部データの取り込みウィザードで選択した引数が使用されます。

- VBA モジュールでは、 **ImportSharePointList**アクションを実行するには、 **DoCmd**オブジェクトの**TransferSharePointList**メソッドを使用します。

- 存在しないリストまたはビューを指定しても、エラーは発生しませんが、データは変換されません。

- GUID とは、リストまたはビューの一意の 16 進数の識別子です。GUID は、次の形式で入力する必要があります。"F" は 16 進数 (0 ～ 9、A ～ F) を表します。
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  SharePoint サイトからリストまたはビューの GUID を取得するには、次の手順を実行します。
    
  1. SharePoint Foundation でリストを開きます。
    
  2. 対象のビューが表示されていない場合は、[ **ビュー**] ボックスの矢印をクリックし、対象のビューを選択します。
    
  3. **ビュー**のドロップダウン矢印をクリックし、**このビューの変更**を選択します.ブラウザーのアドレス バーのアドレスには、リストとビューの両方の Guid が含まれています。 リストの GUID に依存して**リスト =**、ビューの GUID に依存していると**ビュー =**。 ただし、アドレスの各 **{** (左中かっこ) 文字は、文字列で表される、 **%7b**、各**-**(ハイフン) は、文字列で表される **%2 D**、 **}** (右中かっこ) 文字は、文字列**によって表されます%7 D**です。 例:
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  **%7 b**の各文字列を **{** 文字に置き換えて、各を置き換える必要がありますアドレスから Guid を使用するにはこのマクロ アクションの引数として、前に **%2 D**の文字列、**-** 文字、および**各 %7d と**を交換して、**}** 文字です。 含めないでください、 **&** (アンパサンド) に続く文字を **%7 D**の文字列リストの GUID です。

