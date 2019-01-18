---
title: Recordset プロパティと SourceRecordset プロパティ (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f83ab385b1fab511ab71ea9ff3456fe466efa17c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703525"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Recordset プロパティと SourceRecordset プロパティ (RDS)

**適用されます**Access 2013、Office 2013。

カスタム ビジネス オブジェクトから返された **Recordset** オブジェクトを示します。

## <a name="syntax"></a>構文

*DataControl*。SourceRecordset =*レコード セット*

*レコード セット* = *DataControl*。レコード セット

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*Recordset* |**Recordset** オブジェクトを表すオブジェクト変数です。|

## <a name="remarks"></a>解説

**SourceRecordset** プロパティをカスタム ビジネス オブジェクトから返される [Recordset](recordset-object-ado.md) に設定できます。

これらのプロパティを使用すると、カスタム プロセスによってバインド処理を実行できます。これらのプロパティは **Recordset** にラップされた行セットを受け取るので、 **Recordset** を直接操作して、プロパティの設定や **Recordset** の反復処理などの操作を実行できます。

**SourceRecordset** プロパティの値の設定や **Recordset** プロパティの値の取得は、実行時にスクリプト コードで行うことができます。

値の取得のみ可能なプロパティである **Recordset** プロパティとは対照的に、 **SourceRecordset** は値の設定のみ可能なプロパティです。

