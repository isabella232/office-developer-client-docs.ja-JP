---
title: CREATE VIEW ステートメント (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 2f46b897ba4e37f454c656f39333f5c4e0389e94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581589"
---
# <a name="create-view-statement-microsoft-access-sql"></a>CREATE VIEW ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

新しいビューを作成します。

> [!NOTE]
> Microsoft Access データベース エンジンでは、Microsoft Access データベース エンジン以外のデータベースで CREATE VIEW やその他の DDL ステートメントを使用することはできません。

## <a name="syntax"></a>構文

CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*

CREATE VIEW ステートメントでは、次の引数を使用します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パーツ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>作成するビューの名前です。</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>、<em>field2</em></p></td>
<td><p>
            <em>selectstatement</em> に指定されている該当フィールドのフィールド名です。</p></td>
</tr>
<tr class="odd">
<td><p><em>selectstatement</em></p></td>
<td><p>SQL SELECT ステートメント。詳細については、「<a href="select-statement-microsoft-access-sql.md">SELECT ステートメント</a>」を参照してください。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

ビューを定義するのは SELECT ステートメントであり、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントではありません。

ビューを定義する SELECT ステートメントには、パラメーターを含めることができません。

ビューの名前は、既存のテーブルの名前と同じにすることができません。

SELECT ステートメントで定義されたクエリが更新されると、読み取り専用に設定されていない限り、ビューも更新されます。

SELECT ステートメントで定義されるクエリに名前が同じフィールドが 2 つある場合、ビューの定義にフィールド リストを追加し、クエリの各フィールドに一意の名前を指定する必要があります。

