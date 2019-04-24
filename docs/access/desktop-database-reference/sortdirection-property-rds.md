---
title: sortdirection プロパティ (RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fd09eb22d9f751ab1140db948356d2b168b30afb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308618"
---
# <a name="sortdirection-property-rds"></a>sortdirection プロパティ (RDS)

**適用先:** Access 2013、Office 2013

並べ替え順序が昇順であるか、降順であるかを示します。

## <a name="syntax"></a>構文

*DataControl*。sortdirection =*値*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*Value* |ブール型 ( **Boolean** ) の値。 **True** に設定されている場合は、並べ替え順序が昇順であることを示します。 **False** は降順であることを示します。|

## <a name="remarks"></a>注釈

プロパティ [SortColumn](sortcolumn-property-rds.md)、**SortDirection**、[FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。**Reset** メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

