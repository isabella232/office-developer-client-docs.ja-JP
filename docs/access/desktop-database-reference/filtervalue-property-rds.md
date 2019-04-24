---
title: filtervalue プロパティ (RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70dca16f4a949cc6088779c1406e0c77cb477ba1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292406"
---
# <a name="filtervalue-property-rds"></a>filtervalue プロパティ (RDS)

**適用先:** Access 2013、Office 2013

レコードをフィルター処理するための値を示します。

## <a name="syntax"></a>構文

*DataControl*。filtervalue = *String*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*String* |レコードをフィルター処理するためのデータ値を表す**文字列型 (String** ) の値を指定します (例: ' プログラマーズ ' または 125)。|

## <a name="remarks"></a>注釈

プロパティ [SortColumn](sortcolumn-property-rds.md)、 [SortDirection](sortdirection-property-rds.md) 、 **FilterValue**、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。 

並べ替え機能は、列の値でレコードを並べ替えます。 フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 [Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

Null 値は型の不一致エラーになります。

