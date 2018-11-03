---
title: Recordset プロパティと SourceRecordset プロパティ (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f842ad1498e0f6752299cd3d16d8c558042a850e
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945783"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Recordset プロパティと SourceRecordset プロパティ (RDS)


**適用されます**Access 2013、Office 2013。

カスタム ビジネス オブジェクトから返された **Recordset** オブジェクトを示します。

## <a name="syntax"></a>構文

*DataControl*。SourceRecordset =*レコード セット*

*レコード セット* = *DataControl*。レコード セット

## <a name="parameters"></a>パラメーター

- *DataControl*

  - [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。

- *Recordset*

  - **Recordset** オブジェクトを表すオブジェクト変数です。

## <a name="remarks"></a>解説

**SourceRecordset** プロパティをカスタム ビジネス オブジェクトから返される [Recordset](recordset-object-ado.md) に設定できます。

これらのプロパティを使用すると、カスタム プロセスによってバインド処理を実行できます。これらのプロパティは **Recordset** にラップされた行セットを受け取るので、 **Recordset** を直接操作して、プロパティの設定や **Recordset** の反復処理などの操作を実行できます。

**SourceRecordset** プロパティの値の設定や **Recordset** プロパティの値の取得は、実行時にスクリプト コードで行うことができます。

値の取得のみ可能なプロパティである **Recordset** プロパティとは対照的に、 **SourceRecordset** は値の設定のみ可能なプロパティです。

