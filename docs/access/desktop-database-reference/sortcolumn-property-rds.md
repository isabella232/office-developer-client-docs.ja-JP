---
title: SortColumn プロパティ (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61d31ba6044448d2b2534d6affa6157765e9cbc7
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949636"
---
# <a name="sortcolumn-property-rds"></a>SortColumn プロパティ (RDS)

**適用されます**Access 2013、Office 2013。

レコードの並べ替えに使用する列を示します。

## <a name="syntax"></a>構文

*DataControl*。SortColumn =*文字列*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*String* |レコードの並べ替えに使用する列の名前または別名を表す文字列型 ( **String** ) の値。|

## <a name="remarks"></a>解説

プロパティ **SortColumn**、 [SortDirection](sortdirection-property-rds.md) 、 [FilterValue](filtervalue-property-rds.md)、[FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 [Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

**Recordset** の並べ替えを実行するには、まず保留になっている変更をすべて保存します。 **RDS.DataControl** を使用している場合は、 [SubmitChanges](submitchanges-method-rds.md) メソッドを使用できます。 などの場合、**の rds.DataControl** 、ADC1 という名前で、コードになります ADC1。SubmitChanges。 ADO **Recordset** を使用している場合は、 [UpdateBatch](updatebatch-method-ado.md) メソッドを使用できます。 **CreateRecordset** メソッドで作成した **Recordset** オブジェクトには、 [UpdateBatch](createrecordset-method-rds.md) を使用することをお勧めします。 たとえば、コードは myRS.UpdateBatch 可能性がありますか。 ADO **Recordset** を使用している場合は、 [UpdateBatch](updatebatch-method-ado.md) メソッドを使用できます。 **CreateRecordset** メソッドで作成した **Recordset** オブジェクトには、 [UpdateBatch](createrecordset-method-rds.md) を使用することをお勧めします。 などのコードは myRS.UpdateBatch または ADC1 する。Recordset.UpdateBatch。

