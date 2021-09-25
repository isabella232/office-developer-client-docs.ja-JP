---
title: TableDef.ConflictTable プロパティ (DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 81a28d566abf4225bbb7560cdba11639451f8a16
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589009"
---
# <a name="tabledefconflicttable-property-dao"></a>TableDef.ConflictTable プロパティ (DAO)


**適用先**: Access 2013、Office 2013

2 つのレプリカの同期中に競合したデータベース レコードを含む競合テーブルの名前を取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。文字列型 ( **String** ) の値を使用します。  

## <a name="syntax"></a>構文

*式* .ConflictTable

*式* TableDef オブジェクトを **返す式** 。

## <a name="remarks"></a>注釈

競合テーブルがないか、またはデータベースがレプリカではない場合、戻り値は文字列型 ( **String**) の長さがゼロの文字列 ("") です。

2 つの別のレプリカで 2 人のユーザーがそれぞれデータベースの同じレコードを変更した場合、一方のユーザーが行った変更は、他方のレプリカには適用されません。したがって、変更に失敗したユーザーは競合を解決する必要があります。

競合は、フィールド間ではなくレコード レベルで発生します。たとえば、あるユーザーが "住所" フィールドを変更し、別のユーザーが同じレコードの "電話" フィールドを更新した場合、一方の変更は拒否されます。競合はレコード レベルで発生するため、正常に行われた変更および拒否された変更により、情報が競合する可能性が実際には低い場合でも、変更が拒否されます。

同期メカニズムは、変更が正常に行われたらテーブルに配置されたはずの情報を含む競合テーブルを作成することで、レコードの競合を処理します。これらの競合テーブルを調べ、1 行ずつ作業し、適切になるように修正します。

すべての競合テーブルは、テーブルの競合という名前で、テーブルはテーブルの元の名前で、最大テーブル名の長 \_ さに切り捨てられて表示されます。

