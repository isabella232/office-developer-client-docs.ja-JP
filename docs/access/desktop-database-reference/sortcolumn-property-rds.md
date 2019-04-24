---
title: sortcolumn プロパティ (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54e6df1f2a94bd59f1e4cf9f9c0be77d785a3048
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306889"
---
# <a name="sortcolumn-property-rds"></a>sortcolumn プロパティ (RDS)

**適用先:** Access 2013、Office 2013

レコードの並べ替えに使用する列を示します。

## <a name="syntax"></a>構文

*DataControl*。sortcolumn = *String*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*String* |レコードの並べ替えに使用する列の名前または別名を表す文字列型 ( **String** ) の値。|

## <a name="remarks"></a>注釈

プロパティ **SortColumn**、[SortDirection](sortdirection-property-rds.md)、[FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。[Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

**Recordset** の並べ替えを実行するには、まず保留になっている変更をすべて保存します。 **RDS.DataControl** を使用している場合は、 [SubmitChanges](submitchanges-method-rds.md) メソッドを使用できます。 たとえば、RDS がある場合など**です。DataControl**の名前は ADC1 で、コードは ADC1 になります。SubmitChanges. ADO **Recordset** を使用している場合は、 [UpdateBatch](updatebatch-method-ado.md) メソッドを使用できます。 **CreateRecordset** メソッドで作成した **Recordset** オブジェクトには、 [UpdateBatch](createrecordset-method-rds.md) を使用することをお勧めします。 たとえば、myrs またはを使用してコードを作成することができます。 ADO **Recordset** を使用している場合は、 [UpdateBatch](updatebatch-method-ado.md) メソッドを使用できます。 **CreateRecordset** メソッドで作成した **Recordset** オブジェクトには、 [UpdateBatch](createrecordset-method-rds.md) を使用することをお勧めします。 たとえば、myrs. UpdateBatch または ADC1 のようなコードがあるとします。(Recordset. UpdateBatch)

