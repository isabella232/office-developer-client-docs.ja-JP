---
title: DAO コードを ADO に変換する
TOCTitle: Converting DAO Code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7039d9322956e4fcbca4081eff75868ccf306e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476219"
---
# <a name="converting-dao-code-to-ado"></a>DAO コードを ADO に変換する

**適用されます**Access 2013 |。Office 2013

> [!NOTE]
> [!メモ] Access では、DAO 3.6 以前のオブジェクト ライブラリを提供およびサポートしていません。

## <a name="dao-to-ado-object-map"></a>ADO オブジェクトのマップに DAO

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><strong>DAO</strong></p></th>
<th><p><strong>ADO(ADODB)</strong></p></th>
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
<td><p>Field</p></td>
<td><p>Field</p></td>
<td><p>レコードセットを参照するとき。</p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a>DAO

#### <a name="open-a-recordset"></a>Recordset を開く場合

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a>Recordset を編集する場合

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a>ADO

#### <a name="open-a-recordset"></a>Recordset を開く場合

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a>Recordset を編集する場合

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> [!メモ] 最初に **CancelUpdate** メソッドを使用せずに、 **MoveNext、MoveLast、MoveFirst、MovePrevious** メソッドを使ってカレント レコードからフォーカスを移動すると、暗黙的に **Update** メソッドが実行されます。

### <a name="about-the-contributors"></a>投稿者について

**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。 UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。

- [DAO と ADO の間で選択する](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)



