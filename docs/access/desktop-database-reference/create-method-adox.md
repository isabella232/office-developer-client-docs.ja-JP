---
title: Create メソッド (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e98854665185d682b9049b000bf4b600040ba624
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295423"
---
# <a name="create-method-adox"></a>Create メソッド (ADOX)

**適用先:** Access 2013、Office 2013

新規カタログを作成します。

## <a name="syntax"></a>構文

*カタログ*。*connectstring*を作成する

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ConnectString* |データ ソースとの接続に使用される文字列型 ( **String** ) の値を指定します。|

## <a name="remarks"></a>注釈

**Create** メソッドは、*ConnectString* で指定したデータ ソースへの新しい ADO [Connection](connection-object-ado.md) を作成して開きます。成功すると、新しい **Connection** オブジェクトが [ActiveConnection](activeconnection-property-adox.md) プロパティに割り当てられます。

プロバイダーが新しいカタログの作成をサポートしていない場合は、エラーが発生します。

