---
title: Recordset.RecordsetType プロパティ (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e521c4de48f45d080a3b201ac431b2d7da14bc22
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923225"
---
# <a name="recordsetrecordsettype-property-dao"></a>Recordset.RecordsetType プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

" **RecordsetType**/レコードセット" プロパティを使用すると、フォームで編集可能なレコードセットの種類を指定できます。値の取得および設定が可能です。バイト型 ( **Byte**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。レコード セット

*式*: **フォーム** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

Microsoft Office Access データベースでは、" **RecordsetType**/レコードセット" プロパティの設定値は次のとおりです。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>設定</p></th>
<th><p>レコードセットの種類</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>ダイナセット</p></td>
<td><p>(既定値)1 つのテーブルまたは一対一リレーションシップを持つテーブルを基に、連結コントロールを編集できます。 一対多リレーションシップを持つテーブルのフィールドにバインドされたコントロールでは、結合フィールドのデータを編集することはできません、 &quot;1&quot;面をリレーションシップのテーブル間で連鎖更新を有効にしない限り、します。</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>Dynaset (Inconsistent Updates)/ダイナセット (矛盾を許す)</p></td>
<td><p>フィールドに連結されたすべてのテーブルとコントロールを編集できます。</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>スナップショット</p></td>
<td><p>フィールドに連結されたテーブルまたはコントロールは編集できません。</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!メモ] フォームをフォーム ビューまたはデータシート ビューで表示しているときに、連結コントロール内のデータを編集できないようにするには、" **RecordsetType**/レコードセット" プロパティを 2 に設定します。



Microsoft Office Access プロジェクト (.adp) では、" **RecordsetType**/レコードセット" プロパティの設定値は次のとおりです。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>設定</p></th>
<th><p>レコードセットの種類</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>3</p></td>
<td><p>Snapshot/スナップショット</p></td>
<td><p>フィールドに連結されたテーブルまたはコントロールは編集できません。</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>Updatable Snapshot/更新可能なスナップショット</p></td>
<td><p>フィールドに連結されたすべてのテーブルとコントロールを編集できます。(既定値)</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!メモ] 開いているフォームまたはレポートの " **RecordsetType**/レコードセット" プロパティを変更すると、自動的にレコードセットが再作成されます。



複数のテーブルを基にフォームを作成し、コントロールをフィールドと連結させることができます。" **RecordsetType**/レコードセット" プロパティの設定値によって、どのコントロールを編集可能にするかを制限できます。

だけでなく、**レコード セット**によって提供される編集コントロールは、フォーム上の各コントロールは、コントロールとその基になるデータを編集できるかどうかを指定するのに設定することができます**ロック**プロパティを持ちます。 **編集ロック**] プロパティは、[はい] に設定されている場合は、データを編集することはできません。

## <a name="example"></a>例

次の使用例では、ユーザー ID が ADMIN の場合にだけ、レコードを更新できます。ここでは、パブリック変数 gstrUserID の値が ADMIN でない場合、"**RecordsetType**/レコードセット" プロパティを [Snapshot/スナップショット] に設定します。

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a>関連項目

- [Form オブジェクト](https://docs.microsoft.com/office/vba/api/Access.Form)


