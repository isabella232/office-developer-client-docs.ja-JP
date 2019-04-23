---
title: Parameter メンバー (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288113"
---
# <a name="parameter-members-dao"></a>Parameter メンバー (DAO)

**適用先:** Access 2013、Office 2013

Parameter オブジェクトは、クエリに指定する値を表します。 パラメーターは、パラメーター クエリを基に作成した QueryDef オブジェクトに関連付けられています。

## <a name="properties"></a>プロパティ

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
<td><p><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></p></td>
<td><p><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。 Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</p>
<p><strong><a href="parameter-object-dao.md">Parameter</a></strong> オブジェクトが入力パラメーター、出力パラメーター、その両方、またはプロシージャからの戻り値のいずれを表すかを示す値を設定または取得します (ODBCDirect ワークスペースのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-name-property-dao.md">Name</a></strong></p></td>
<td><p>指定したオブジェクトの名前を返します。 読み取り専用 <strong>文字列</strong> です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-type-property-dao.md">種類</a></strong></p></td>
<td><p>オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。 読み取り/書き込みの <strong>整数</strong> です。</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-value-property-dao.md">Value</a></strong></p></td>
<td><p>オブジェクトの値を設定または取得します。値の取得および設定が可能です。バリアント型 (<strong>Variant</strong>) の値を使用します。</p></td>
</tr>
</tbody>
</table>

