---
title: FilterCriterion プロパティ (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e290f51e134c331c3944e65da4fa6a0758384c0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612121"
---
# <a name="filtercriterion-property-rds"></a>FilterCriterion プロパティ (RDS)

**適用先**: Access 2013、Office 2013

フィルター値に使う評価演算子を表します。

## <a name="syntax"></a>構文

*DataControl*.FilterCriterion = *String*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*String* |レコードに **FilterValue** の評価演算子を指定する文字列型 ( [String](filtervalue-property-rds.md) ) の値を指定します。 、=、=、またはのいずれかを \<, \<=, \> \> 指定できます \<\> 。|

## <a name="remarks"></a>注釈

プロパティ [SortColumn](sortcolumn-property-rds.md)、[SortDirection](sortdirection-property-rds.md)、[FilterValue](filtervalue-property-rds.md)、**FilterCriterion**、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。[Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

" \! =" 演算子は **FilterCriterion** に対して無効です。代わりに"" を使用 \<\> します。

フィルター プロパティと並べ替えプロパティの両方を設定して **Reset** メソッドを呼び出した場合、行セットでは最初にフィルターが実行され、次に並べ替えが実行されます。昇順の並べ替えでは Null 値が最初に、降順の並べ替えでは Null 値が最後になります (昇順が既定の動作です)。

