---
title: CREATE VIEW ステートメント (Microsoft Access SQL)
TOCTitle: CREATE VIEW Statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 292dddeab15c71fb188a928ac0e491063930214d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477371"
---
# <a name="create-view-statement-microsoft-access-sql"></a>CREATE VIEW ステートメント (Microsoft Access SQL)


**適用されます**Access 2013 |。Office 2013

新しいビューを作成します。


> [!NOTE]
> <P>[!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CREATE VIEW 句や DDL (データ定義言語) ステートメントを使用できません。</P>



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
<td><p>SQL SELECT ステートメント。詳細については、「<a href="select-statement-microsoft-access-sql.md">SELECT ステートメント</a>」を参照してください。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

ビューを定義するのは SELECT ステートメントであり、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントではありません。

ビューを定義する SELECT ステートメントは、パラメーターを含むことができません。

ビュー名は、既存のテーブルと同じ名前にしないでください。

SELECT ステートメントで定義されたクエリが更新されると、読み取り専用に設定されていない限り、ビューも更新されます。

SELECT ステートメントで定義されるクエリで 2 つのフィールドが同じ名前の場合、クエリでフィールドごとに一意の名前が指定されるフィールド リストを、ビューの定義に含む必要があります。

