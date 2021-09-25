---
title: DAO コードを ADO に変換する
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 175f168fdc384570ad99c86db9e0c185b7d6cf38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569252"
---
# <a name="convert-dao-code-to-ado"></a>DAO コードを ADO に変換する

**適用先**: Access 2013、Office 2013

> [!NOTE]
> 3.6より前のバージョンの DAO ライブラリは、Access では提供もサポートもされていません。

## <a name="dao-to-ado-object-map"></a>DAO から ADO へのオブジェクト マップ

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<th><p><strong>ADO (ADODB)</strong></p></th>
<th><p><strong>注</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBEngine</p></td>
<td><p>なし</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Workspace</p></td>
<td><p>なし</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Database</p></td>
<td><p>Connection</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Recordset</p></td>
<td><p>Recordset</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Dynaset-Type</p></td>
<td><p>Keyset</p></td>
<td><p>レコードセットのレコードへのポインターを取得します。</p></td>
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<td><p>共にフル レコードを取得しますが、Static レコードセットは更新可能です。</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>adCmdTableDirect オプションを持つ Keyset。</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>フィールド</p></td>
<td><p>フィールド</p></td>
<td><p>レコードセットを参照するとき。</p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Recordset を開く

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Recordset を編集する

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Recordset を開く

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Recordset を編集する

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> 最初に **CancelUpdate** メソッドを使用せずに、 **MoveNext、MoveLast、MoveFirst、MovePrevious** メソッドを使ってカレント レコードからフォーカスを移動すると、暗黙的に **Update** メソッドが実行されます。

### <a name="about-the-contributors"></a>投稿者について

**リンクの提供元:**[UtterAccess](https://www.utteraccess.com) コミュニティ。 UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。

- [DAO と ADO 間の選択](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

