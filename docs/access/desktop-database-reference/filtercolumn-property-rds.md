---
title: filtercolumn プロパティ (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d29c591c88de4b53535c26430bf369cbd3f53284
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292441"
---
# <a name="filtercolumn-property-rds"></a>filtercolumn プロパティ (RDS)

**適用先:** Access 2013、Office 2013

フィルター条件を評価する列を示します。

## <a name="syntax"></a>構文

*DataControl*。filtercolumn = *String*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*String* |フィルター条件を評価する列を指定する文字列型 ( **String** ) の値を指定します。フィルター条件は [FilterCriterion](filtercriterion-property-rds.md) プロパティに指定します。|

## <a name="remarks"></a>注釈

プロパティ [SortColumn](sortcolumn-property-rds.md)、 [SortDirection](sortdirection-property-rds.md) 、 [FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および **FilterColumn** は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。 

並べ替え機能は、列の値でレコードを並べ替えます。 フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 

[Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

