---
title: Connect プロパティ (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295983"
---
# <a name="connect-property-rds"></a>Connect プロパティ (RDS)

**適用先:** Access 2013、Office 2013

クエリおよび更新操作が実行されるデータベース名を示します。

**Connect** プロパティは、デザイン時に [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグ内で、または実行時にスクリプト コード (たとえば、VBScript) 内で設定できます。

## <a name="syntax"></a>構文

デザイン時: \<パラメーター名 = "Connect" VALUE = "ConnectionString"\>

実行時間: DataControl = "ConnectionString"

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ConnectionString* |有効な接続文字列を指定します。接続文字列全般の説明については、[ConnectionString](connectionstring-property-ado.md) プロパティかプロバイダーのマニュアルを参照してください。<br/><br/>**注**: MS Remote を RDS のプロバイダーとして指定し**ます。DataControl**は、4層のシナリオを作成します。 3 層を超えるシナリオについては未確認なので避けてください。|
|*DataControl* |**RDS.DataControl** オブジェクトを表すオブジェクト変数。|

