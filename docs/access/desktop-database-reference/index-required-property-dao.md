---
title: Index.Required プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 02cf71cbd5c1692fb68829902191922536061e43
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626380"
---
# <a name="indexrequired-property-dao"></a>Index.Required プロパティ (DAO)

**適用先**: Access 2013、Office 2013

**[Field](field-object-dao.md)** オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。

## <a name="syntax"></a>構文

*式* .必須

*式* Index オブジェクトを表す **変数** 。

## <a name="remarks"></a>注釈

> [!NOTE]
> [!メモ] **Index** オブジェクトまたは **Field** オブジェクトのいずれかにこのプロパティを設定できる場合は、 **Field** オブジェクトに設定します。 **Field** オブジェクトのプロパティ設定の妥当性が検査された後、 **Index** オブジェクトの設定が検査されます。

**Required** プロパティを使用できるかどうかは、次の表に示すように、 [Fields](fields-collection-dao.md) コレクションが含まれているオブジェクトによって決まります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fields コレクションの所属先</p></th>
<th><p>Required プロパティの使用</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong> オブジェクト</p></td>
<td><p>サポートしません。</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong> オブジェクト</p></td>
<td><p>非サポート</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> オブジェクト</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
</tbody>
</table>

