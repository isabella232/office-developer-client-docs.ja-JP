---
title: Connect プロパティ (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49f62accab5a4da7d89c545bf82d0593238be1c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597619"
---
# <a name="connect-property-rds"></a>Connect プロパティ (RDS)

**適用先**: Access 2013、Office 2013

クエリおよび更新操作が実行されるデータベース名を示します。

**Connect** プロパティは、デザイン時に [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグ内で、または実行時にスクリプト コード (たとえば、VBScript) 内で設定できます。

## <a name="syntax"></a>構文

設計時間: \<PARAM NAME="Connect" VALUE="ConnectionString"\>

実行時: DataControl。Connect = "ConnectionString"

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ConnectionString* |有効な接続文字列を指定します。接続文字列全般の説明については、[ConnectionString](connectionstring-property-ado.md) プロパティかプロバイダーのマニュアルを参照してください。<br/><br/>**メモ**: RDS のプロバイダーとして MS Remote を **指定します。DataControl は** 4 層のシナリオを作成します。 3 層を超えるシナリオについては未確認なので避けてください。|
|*DataControl* |**RDS.DataControl** オブジェクトを表すオブジェクト変数。|

