---
title: 同等の ANSI SQL のデータ型
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293512"
---
# <a name="equivalent-ansi-sql-data-types"></a>同等の ANSI SQL のデータ型


**適用先**: Access 2013、Office 2013

次の表は、ANSI SQL データ型、同等の Microsoft Access データベース エンジンの SQL データ型、有効な類義語を一覧表示しています。 また、この表には同等の Microsoft SQL Server™ のデータ型も示されています。

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ANSI SQL のデータ型</p></th>
<th><p>Microsoft Access SQL のデータ型</p></th>
<th><p>類義語</p></th>
<th><p>Microsoft SQL Server のデータ型</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BIT、BIT VARYING</p></td>
<td><p>BINARY (次の「メモ」を参照)</p></td>
<td><p>VARBINARY、BINARY VARYING BIT VARYING</p></td>
<td><p>BINARY、VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>サポート対象外</p></td>
<td><p>BIT (次の「メモ」を参照)</p></td>
<td><p>BOOLEAN、LOGICAL、LOGICAL1、YESNO</p></td>
<td><p>BIT</p></td>
</tr>
<tr class="odd">
<td><p>サポート対象外</p></td>
<td><p>TINYINT</p></td>
<td><p>INTEGER1、BYTE</p></td>
<td><p>TINYINT</p></td>
</tr>
<tr class="even">
<td><p>サポート対象外</p></td>
<td><p>COUNTER (次の「メモ」を参照)</p></td>
<td><p>AUTOINCREMENT</p></td>
<td><p>(メモを参照)</p></td>
</tr>
<tr class="odd">
<td><p>サポート対象外</p></td>
<td><p>MONEY</p></td>
<td><p>CURRENCY</p></td>
<td><p>MONEY</p></td>
</tr>
<tr class="even">
<td><p>DATE、TIME、TIMESTAMP</p></td>
<td><p>DATETIME</p></td>
<td><p>DATE、TIME (メモを参照)</p></td>
<td><p>DATETIME</p></td>
</tr>
<tr class="odd">
<td><p>非サポート</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>GUID</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
</tr>
<tr class="even">
<td><p>DECIMAL</p></td>
<td><p>DECIMAL</p></td>
<td><p>NUMERIC、DEC</p></td>
<td><p>DECIMAL</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>REAL</p></td>
<td><p>SINGLE、FLOAT4、IEEESINGLE</p></td>
<td><p>REAL</p></td>
</tr>
<tr class="even">
<td><p>DOUBLE PRECISION、FLOAT</p></td>
<td><p>FLOAT</p></td>
<td><p>DOUBLE、FLOAT8、IEEEDOUBLE、NUMBER (次の「メモ」を参照)</p></td>
<td><p>FLOAT</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>SMALLINT</p></td>
<td><p>SHORT、INTEGER2</p></td>
<td><p>SMALLINT</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>INTEGER</p></td>
<td><p>LONG、INT、INTEGER4</p></td>
<td><p>INTEGER</p></td>
</tr>
<tr class="odd">
<td><p>INTERVAL</p></td>
<td><p>非サポート</p></td>
<td><p></p></td>
<td><p>サポートされていません。</p></td>
</tr>
<tr class="even">
<td><p>非サポート</p></td>
<td><p>IMAGE</p></td>
<td><p>LONGBINARY、GENERAL、OLEOBJECT</p></td>
<td><p>IMAGE</p></td>
</tr>
<tr class="odd">
<td><p>非サポート</p></td>
<td><p>TEXT (メモを参照)</p></td>
<td><p>LONGTEXT、LONGCHAR、MEMO、NOTE、NTEXT (次の「メモ」を参照)</p></td>
<td><p>TEXT</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER、CHARACTER VARYING、NATIONAL CHARACTER、NATIONAL CHARACTER VARYING</p></td>
<td><p>CHAR (次の「メモ」を参照)</p></td>
<td><p>TEXT(n)、ALPHANUMERIC、CHARACTER, STRING、VARCHAR、CHARACTER VARYING、NCHAR、NATIONAL CHARACTER、NATIONAL CHAR、NATIONAL CHARACTER VARYING、NATIONAL CHAR VARYING (メモを参照)</p></td>
<td><p>CHAR、VARCHAR、NCHAR、NVARCHAR</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - Microsoft Access SQL のデータ型 BIT は、ANSI SQL のデータ型 BIT とは異なります。Microsoft Access SQL のデータ型 BINARY が ANSI SQL のデータ型 BIT と同じ役割を果たします。Microsoft Access SQL のデータ型 BIT に相当する ANSI SQL のデータ型はありません。
> - データ型 TIMESTAMP を、データ型 DATETIME の別名として使用することはできません。
> - データ型 NUMERIC を、データ型 FLOAT または DOUBLE の別名として使用することはできません。データ型 NUMERIC を、データ型 DECIMAL の別名として使用することはできません。
> - LONGTEXT 型フィールドでは、データは常に Unicode 表示形式で格納されます。
> - データ型 TEXT を文字列の長さ (たとえば TEXT(25)) を指定しないで使用すると、LONGTEXT 型フィールドが作成されます。このため、[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントのデータ型と Microsoft SQL Server のデータ型の整合性を保つことが可能になります。
> - CHAR 型フィールドでは、データは常に Unicode 表示形式で格納されます。データ型 CHAR は、ANSI SQL のデータ型 NATIONAL CHAR に相当します。
> - たとえば TEXT(25) のように、フィールドのデータ型が、文字列の長さを指定したデータ型 TEXT である場合、そのフィールドのデータ型はデータ型 CHAR と一致します。データ型が一致することによって、文字列の長さが指定されていない TEXT データ型と Microsoft SQL Server のデータ型の間の整合性が保たれると共に、以前に作成された Microsoft Jet 用のアプリケーションで使用されているデータ型との下位互換性が保たれます。


