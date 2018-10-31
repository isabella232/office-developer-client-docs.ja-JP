---
title: CREATE VIEW ステートメント (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f1d13cef4551975dc316b2fbedf2388028956fb3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862906"
---
# <a name="create-view-statement-microsoft-access-sql"></a>CREATE VIEW ステートメント (Microsoft Access SQL)

**適用されます**Access 2013 |。Office 2013

新しいビューを作成します。

> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CREATE VIEW 句や DDL (データ定義言語) ステートメントを使用できません。

## <a name="syntax"></a>構文

*ビュー*のビューの作成\[(*フィールド 1*\[、*フィールド 2*\[、.\] \])\]として*使いましょう*

CREATE VIEW ステートメントには次の指定項目があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>指定項目</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>作成するビューの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p><em>selectstatement</em> で指定された関連フィールドのフィールド名。</p></td>
</tr>
<tr class="odd">
<td><p><em>selectstatement</em></p></td>
<td><p>SQL SELECT ステートメント。 詳細については、 <a href="select-statement-microsoft-access-sql.md">SELECT ステートメントを</a>参照してください。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

ビューを定義するのは SELECT ステートメントであり、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントではありません。

ビューを定義する SELECT ステートメントは、パラメーターを含むことができません。

ビュー名は、既存のテーブルと同じ名前にしないでください。

SELECT ステートメントによって定義されたクエリが更新可能な場合は、ビューも更新できます。 それ以外の場合、ビューは読み取り専用です。

SELECT ステートメントで定義されるクエリで 2 つのフィールドが同じ名前の場合、クエリでフィールドごとに一意の名前が指定されるフィールド リストを、ビューの定義に含む必要があります。

