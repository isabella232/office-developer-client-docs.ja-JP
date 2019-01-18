---
title: 関係メンバー (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84e18afe4a11e53d68397efad71ac6136c779143
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722726"
---
# <a name="relation-members-dao"></a>関係メンバー (DAO)


**適用されます**Access 2013、Office 2013。

Relation オブジェクトは、テーブルまたはクエリのフィールド間のリレーションシップを表します (Microsoft Access データベース エンジン データベースのみ)。

## <a name="methods"></a>メソッド

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>新しい <strong><a href="field-object-dao.md">Field</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Properties

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></p></td>
<td><p><strong>Relation</strong> オブジェクトの 1 つまたは複数の属性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>指定されたオブジェクト用に保存されているすべての <strong>Field</strong> オブジェクトを表す <strong>Fields</strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-foreigntable-property-dao.md">外部テーブル</a></strong></p></td>
<td><p>リレーションシップの外部テーブルの名前を設定または取得します (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-name-property-dao.md">Name</a></strong></p></td>
<td><p>指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-partialreplica-property-dao.md">必要</a></strong></p></td>
<td><p>フル レプリカから部分レプリカに値を設定するときに、 <strong>Relation</strong> オブジェクトのリレーションシップを考慮する必要があるかどうかを示す値を設定または取得します (Microsoft Access データベース エンジンのデータベースのみ)。値の取得および設定が可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="relation-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="relation-table-property-dao.md">テーブル</a></strong></p></td>
<td><p><strong><a href="relation-object-dao.md">Relation</a></strong> オブジェクトの主テーブルの名前を示します。これは、 <strong><a href="connection-name-property-dao.md">TableDef</a></strong> オブジェクトまたは <strong><a href="tabledef-object-dao.md">QueryDef</a></strong> オブジェクトの <strong><a href="querydef-object-dao.md">Name</a></strong> プロパティの設定値と同じである必要があります (Microsoft Access ワークスペースのみ)。</p></td>
</tr>
</tbody>
</table>

