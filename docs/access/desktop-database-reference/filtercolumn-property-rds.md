---
title: FilterColumn プロパティ (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 23fbdbc8c546d99456a5e898ea835d3b157e7728
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602627"
---
# <a name="filtercolumn-property-rds"></a>FilterColumn プロパティ (RDS)

**適用先**: Access 2013、Office 2013

フィルター条件を評価する列を示します。

## <a name="syntax"></a>構文

*DataControl*.FilterColumn = *String*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*String* |フィルター条件を評価する列を指定する文字列型 ( **String** ) の値を指定します。フィルター条件は [FilterCriterion](filtercriterion-property-rds.md) プロパティに指定します。|

## <a name="remarks"></a>注釈

プロパティ [SortColumn](sortcolumn-property-rds.md)、 [SortDirection](sortdirection-property-rds.md) 、 [FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および **FilterColumn** は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。 

並べ替え機能は、列の値でレコードを並べ替えます。 フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 

[Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

