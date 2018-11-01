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
ms.openlocfilehash: 60baeabfce93c2987cb9621c7cc877a7525a954c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876744"
---
# <a name="convert-dao-code-to-ado"></a>DAO コードを ADO に変換する

**適用されます**Access 2013、Office 2013。

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
<th><p><strong>ADO (ADODB)</strong></p></th>
<th><p><strong>メモ</strong></p></th>
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
<td><p>レコード セット内のレコードへのポインターのセットを取得します。</p></td>
</tr>
<tr class="even">
<td><p>Snapshot-Type</p></td>
<td><p>Static</p></td>
<td><p>全レコードを取得しますが、静的レコード セットを更新することができます。</p></td>
</tr>
<tr class="odd">
<td><p>Table-Type</p></td>
<td><p>AdCmdTableDirect オプションを使用してキーセットです。</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>フィールド</p></td>
<td><p>フィールド</p></td>
<td><p>参照されたとき、レコード セットにします。</p></td>
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
> 最初に**CancelUpdate**メソッドを暗黙的に使用せず、 **MovePrevious、MoveNext、MoveLast、MoveFirst**を使用してカレント レコードからフォーカスを移動すると、 **Update**メソッドが実行されます。

### <a name="about-the-contributors"></a>投稿者について

**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。 UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。

- [DAO と ADO の間で選択する](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

