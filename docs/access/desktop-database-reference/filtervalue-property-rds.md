---
title: FilterValue プロパティ (RDS)
TOCTitle: FilterValue Property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 818a38c4c7d11442b1deb7ddeef72a828283c897
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887335"
---
# <a name="filtervalue-property-rds"></a>FilterValue プロパティ (RDS)


**適用されます**Access 2013、Office 2013。


レコードをフィルター処理するための値を示します。

## <a name="syntax"></a>構文

*DataControl*。FilterValue =*文字列*

## <a name="parameters"></a>パラメーター

  - *DataControl*

  - [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。

  - *String*

  - **文字列**を表す値 (たとえば、'プログラマ' または 125) のフィルター処理に使用するデータ値を記録します。

## <a name="remarks"></a>解説

プロパティ [SortColumn](sortcolumn-property-rds.md)、[SortDirection](sortdirection-property-rds.md)、 **FilterValue** 、 [FilterCriterion](filtercriterion-property-rds.md)、および [FilterColumn](filtercolumn-property-rds.md) は、クライアント側のキャッシュ上で並べ替え機能とフィルター機能を提供します。並べ替え機能は、列の値でレコードを並べ替えます。フィルター機能は、キャッシュ内の完全な [Recordset](recordset-object-ado.md) は保持したまま、検索条件に基づいてレコードのサブセットを表示します。 [Reset](reset-method-rds.md) メソッドは検索条件を実行し、現在の **Recordset** を更新可能な **Recordset** に置き換えます。

Null 値は型の不一致エラーになります。

