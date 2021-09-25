---
title: SortDirection プロパティ (RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3d8b7a42755d4efc18e5785efcbad92b9da6a709
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580854"
---
# <a name="sortdirection-property-rds"></a>SortDirection プロパティ (RDS)

**適用先:** Access 2013、Office 2013

並べ替え順序が昇順であるか、降順であるかを示します。

## <a name="syntax"></a>構文

*DataControl*.SortDirection = *value*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*Value* |ブール型 ( **Boolean** ) の値。 **True** に設定されている場合は、並べ替え順序が昇順であることを示します。 **False** は降順であることを示します。|

## <a name="remarks"></a>注釈

プロパティ [SortColumn](sortcolumn-property-rds.md)、**SortDirection**、[FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。**Reset** メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

