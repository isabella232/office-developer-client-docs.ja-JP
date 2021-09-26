---
title: Create メソッド (ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cf9d2b74aae4c13bb3e1349ffd4a7d23ed95b3aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626954"
---
# <a name="create-method-adox"></a>Create メソッド (ADOX)

**適用先**: Access 2013、Office 2013

新規カタログを作成します。

## <a name="syntax"></a>構文

*カタログ*.*Create ConnectString*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ConnectString* |データ ソースとの接続に使用される文字列型 ( **String** ) の値を指定します。|

## <a name="remarks"></a>注釈

**Create** メソッドは、*ConnectString* で指定したデータ ソースへの新しい ADO [Connection](connection-object-ado.md) を作成して開きます。成功すると、新しい **Connection** オブジェクトが [ActiveConnection](activeconnection-property-adox.md) プロパティに割り当てられます。

プロバイダーが新しいカタログの作成をサポートしていない場合は、エラーが発生します。

