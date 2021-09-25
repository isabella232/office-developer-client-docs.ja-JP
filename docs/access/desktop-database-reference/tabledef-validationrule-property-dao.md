---
title: TableDef.ValidationRule プロパティ (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 99c849f6154c10d6d6cc42cdec9a72cd9df12a79
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588994"
---
# <a name="tabledefvalidationrule-property-dao"></a>TableDef.ValidationRule プロパティ (DAO)

**適用先**: Access 2013、Office 2013

データの変更時またはテーブルへの追加時に、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ) 。値の取得および設定が可能です。文字列型 ( **String** ) の値を使用します。    

## <a name="syntax"></a>構文

*式* .ValidationRule

*式***TableDef** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

設定値または戻り値は、予約語 WHERE を指定しない SQL WHERE 句形式での比較を示す文字列型 ( **String**) の値となります。 **Fields** コレクションにまだ追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。

**ValidationRule** プロパティは、フィールドに有効なデータが含まれているかどうかを示します。データが無効の場合は、トラップ可能な実行時エラーが発生します。エラー メッセージには、 **ValidationText** プロパティが設定されている場合はそのテキストが表示され、それ以外は **ValidationRule** に指定されている式のテキストが表示されます。

検証は、Microsoft Access データベース エンジンを使用しているデータベースに対してのみサポートされます。

**Field** オブジェクトの **ValidationRule** プロパティで指定される文字列式は、該当する **Field** のみ参照できます。ユーザー定義関数、SQL 集計関数、またはクエリを参照することはできません。 **Field** オブジェクトの **ValidateOnSet** プロパティが **True** に設定されているときに、このオブジェクトの **ValidationRule** プロパティを設定するには、この式の解析が正常に終了し (フィールド名を暗黙のオペランドとして)、 **True** と評価される必要があります。 **ValidateOnSet** プロパティが **False** に設定されている場合、 **ValidationRule** プロパティの設定は無視されます。

**Recordset** オブジェクトまたは **TableDef** オブジェクトの **ValidationRule** プロパティは、該当するオブジェクトの複数のフィールドを参照できます。このプロパティには、 **Field** オブジェクトに関する前述の制限が当てはまります。

リンク テーブルに基づく **TableDef** オブジェクトの場合、 **ValidationRule** プロパティは、基になるベース テーブルの **ValidationRule** プロパティの設定値を継承します。基になるベース テーブルが検証をサポートしていない場合、このプロパティの値は長さ 0 の文字列 ("") となります。

> [!NOTE]
> 整数以外の値で連結された文字列にプロパティを設定し、システム パラメーターで米国以外の値を指定する場合。コンマなどの 10 進文字 (strRule = "PRICE &gt; " &amp; lngPrice、lngPrice = 125,50 など) は、コードがデータを検証しようとするときにエラーが発生します。 連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。
