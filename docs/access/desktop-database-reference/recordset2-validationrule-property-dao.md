---
title: "\"Recordset2/入力規則\" プロパティ (DAO)"
TOCTitle: ValidationRule Property
ms:assetid: d46cc255-e588-e9e6-66d7-31fc26ae45b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835002(v=office.15)
ms:contentKeyID: 48547940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7b146aa0278db278f3831bc0e00987d21e14b70a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307155"
---
# <a name="recordset2validationrule-property-dao"></a>"Recordset2/入力規則" プロパティ (DAO)


**適用先:** Access 2013、Office 2013

データの変更時またはテーブルへの追加時に、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ) 。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。    

## <a name="syntax"></a>構文

*式*。規則

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

設定値または戻り値は、予約語 WHERE を指定しない SQL WHERE 句形式での比較を示す文字列型 ( **String**) の値となります。 **Fields** コレクションにまだ追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。

**ValidationRule** プロパティは、フィールドに有効なデータが含まれているかどうかを示します。データが無効の場合は、トラップ可能な実行時エラーが発生します。エラー メッセージには、 **ValidationText** プロパティが設定されている場合はそのテキストが表示され、それ以外は **ValidationRule** に指定されている式のテキストが表示されます。

**Recordset** オブジェクトの場合、 **ValidationRule** プロパティは値の取得のみ可能です。 **TableDef** オブジェクトの場合、 **ValidationRule** プロパティの使用方法は、次の表に示すように **TableDef** オブジェクトのステータスによって変わります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>TableDef</p></th>
<th><p>使用方法</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ベース テーブル</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p>リンク テーブル</p></td>
<td><p>読み取り専用</p></td>
</tr>
</tbody>
</table>


検証は、Microsoft Access データベース エンジンを使用しているデータベースに対してのみサポートされます。

**Field** オブジェクトの **ValidationRule** プロパティで指定される文字列式は、該当する **Field** のみ参照できます。ユーザー定義関数、SQL 集計関数、またはクエリを参照することはできません。 **Field** オブジェクトの **ValidateOnSet** プロパティが **True** に設定されているときに、このオブジェクトの **ValidationRule** プロパティを設定するには、この式の解析が正常に終了し (フィールド名を暗黙のオペランドとして)、 **True** と評価される必要があります。 **ValidateOnSet** プロパティが **False** に設定されている場合、 **ValidationRule** プロパティの設定は無視されます。

**Recordset** オブジェクトまたは **TableDef** オブジェクトの **ValidationRule** プロパティは、該当するオブジェクトの複数のフィールドを参照できます。このプロパティには、 **Field** オブジェクトに関する前述の制限が当てはまります。

テーブル タイプの **Recordset** オブジェクトの場合、 **ValidationRule** プロパティは、テーブル タイプの **Recordset** オブジェクトの作成に使用する **TableDef** オブジェクトの **ValidationRule** プロパティの設定を継承します。

> [!NOTE]
> このプロパティに整数以外の値を連結した文字列を設定した場合、システムパラメーターでコンマ以外の小数点 (例: strrule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125, 50) を指定すると、エラーが発生します。コードがデータを検証しようとしています。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。</P>

