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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706738"
---
# <a name="connect-property-rds"></a>Connect プロパティ (RDS)

**適用されます**Access 2013、Office 2013。

クエリおよび更新操作が実行されるデータベース名を示します。

**Connect** プロパティは、デザイン時に [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグ内で、または実行時にスクリプト コード (たとえば、VBScript) 内で設定できます。

## <a name="syntax"></a>構文

デザイン時:\<パラメーターの名前 [接続] の値を = =「接続文字列」\>

実行時間: DataControl.Connect =「接続文字列」

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ConnectionString* |有効な接続文字列を指定します。接続文字列全般の説明については、[ConnectionString](connectionstring-property-ado.md) プロパティかプロバイダーのマニュアルを参照してください。<br/><br/>**注**: rds. の**のプロバイダーとして MS Remote を指定します。DataControl** 4 層のシナリオを作成します。 3 層を超えるシナリオについては未確認なので避けてください。|
|*DataControl* |**RDS.DataControl** オブジェクトを表すオブジェクト変数を指定します。|

