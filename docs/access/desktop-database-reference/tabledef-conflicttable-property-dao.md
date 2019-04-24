---
title: ConflictTable プロパティ (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 0189a5163dd5e225ad34841264cf84e85785d7fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308429"
---
# <a name="tabledefconflicttable-property-dao"></a>ConflictTable プロパティ (DAO)


**適用先:** Access 2013、Office 2013

2 つのレプリカの同期中に競合したデータベース レコードを含む競合テーブルの名前を取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。文字列型 ( **String** ) の値を使用します。  

## <a name="syntax"></a>構文

*式*。ConflictTable

*式***TableDef**オブジェクトを返すオブジェクト式を指定します。

## <a name="remarks"></a>注釈

競合テーブルがないか、またはデータベースがレプリカではない場合、戻り値は文字列型 ( **String**) の長さがゼロの文字列 ("") です。

2 つの別のレプリカで 2 人のユーザーがそれぞれデータベースの同じレコードを変更した場合、一方のユーザーが行った変更は、他方のレプリカには適用されません。したがって、変更に失敗したユーザーは競合を解決する必要があります。

競合は、フィールド間ではなくレコード レベルで発生します。たとえば、あるユーザーが "住所" フィールドを変更し、別のユーザーが同じレコードの "電話" フィールドを更新した場合、一方の変更は拒否されます。競合はレコード レベルで発生するため、正常に行われた変更および拒否された変更により、情報が競合する可能性が実際には低い場合でも、変更が拒否されます。

同期メカニズムは、変更が正常に行われたらテーブルに配置されたはずの情報を含む競合テーブルを作成することで、レコードの競合を処理します。これらの競合テーブルを調べ、1 行ずつ作業し、適切になるように修正します。

すべての競合テーブルはテーブル\_の名前が競合しています。 table はテーブルの元の名前で、テーブル名の最大長に切り詰められます。

