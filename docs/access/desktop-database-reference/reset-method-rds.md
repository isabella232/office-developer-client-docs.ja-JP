---
title: Reset メソッド (RDS-Access デスクトップデータベースリファレンス)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306644"
---
# <a name="reset-method-rds"></a>Reset メソッド (RDS)

**適用先:** Access 2013、Office 2013

指定されたソートとフィルターのプロパティに基づいて、クライアント側の **Recordset** でソートまたはフィルターを実行します。

## <a name="syntax"></a>構文

*DataControl*。Reset (*値*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*value* |省略可能です。ブール型 ( **Boolean** ) の値を指定します。現在 "フィルター選択されている" 行セットでフィルターを実行する場合は、 **True** (既定値) を指定します。 **False** は、以前のフィルター オプションをすべて破棄して元の行セットでフィルターを実行する場合に指定します。|

## <a name="remarks"></a>注釈

[SortColumn](sortcolumn-property-rds.md)、[SortDirection](sortdirection-property-rds.md)、[FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) の各プロパティは、クライアント側のキャッシュ上でソート機能とフィルター機能を提供します。ソート機能では、1 つの列の値でレコードを並べます。フィルター機能では、抽出条件に基づいてレコードのサブセットを表示します。このとき、キャッシュには [Recordset](recordset-object-ado.md) 全体が保持されています。**Reset** メソッドは、抽出条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

元のデータの変更がまだ適用されていない場合、 **Reset** メソッドは失敗します。まず [SubmitChanges](submitchanges-method-rds.md) メソッドを使用して、読み取り/書き込み可能な **Recordset** に加えられた変更を保存し、その後 **Reset** メソッドを使用してレコードに対するソートまたはフィルターを実行します。

行セットに複数のフィルターを実行する場合、**Reset** メソッドで *Boolean* 引数を使用できます。次の例は、その方法を示しています。

