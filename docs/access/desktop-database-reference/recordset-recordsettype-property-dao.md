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
ms.localizationpriority: medium
ms.openlocfilehash: fe9106d661567da70299de40f3c93aea45c539c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606073"
---
# <a name="recordsetrecordsettype-property-dao"></a>Recordset.RecordsetType プロパティ (DAO)

**適用先**: Access 2013、Office 2013

"**RecordsetType**/レコードセット" プロパティを使用すると、フォームで編集可能なレコードセットの種類を指定できます。値の取得および設定が可能です。バイト型 (**Byte**) の値を使用します。

## <a name="syntax"></a>構文

*式* .RecordsetType

*式*: **Form** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

Microsoft Office Access データベースでは、"**RecordsetType**/レコードセット" プロパティの設定値は次のとおりです。

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
<td><p>(既定)1 対 1 のリレーションシップを持つ 1 つのテーブルまたはテーブルに基づいてバインド されたコントロールを編集できます。 1 対多のリレーションシップを持つテーブルに基づくフィールドにバインドされたコントロールの場合、テーブル間でカスケード更新が有効になっていない限り、リレーションシップの一方の結合フィールドからデータを編集 &quot; &quot; することはできません。</p></td>
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
<td><p>スナップショット</p></td>
<td><p>フィールドに連結されたテーブルまたはコントロールは編集できません。</p></td>
</tr>
<tr class="even">
<td><p>4 </p></td>
<td><p>Updatable Snapshot/更新可能なスナップショット</p></td>
<td><p>フィールドに連結されたすべてのテーブルとコントロールを編集できます。(既定値)</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!メモ] 開いているフォームまたはレポートの " **RecordsetType**/レコードセット" プロパティを変更すると、自動的にレコードセットが再作成されます。

複数のテーブルを基にフォームを作成し、コントロールをフィールドと連結させることができます。" **RecordsetType**/レコードセット" プロパティの設定値によって、どのコントロールを編集可能にするかを制限できます。

"**RecordsetType**/レコードセット" プロパティによって提供される編集の制御機能のほかに、フォームの各コントロールには "**Locked**/編集ロック" プロパティがあります。このプロパティを使うと、コントロールとその基になるデータを編集できるかどうかを指定できます。"**Locked**/編集ロック" プロパティが [Yes/はい] に設定されている場合は、データを編集することはできません。

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


