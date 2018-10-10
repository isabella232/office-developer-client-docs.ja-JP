---
title: Create メソッド (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cffaa8fb924d2fd272300c77fc5a9c3dc0b239db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479018"
---
# <a name="create-method-adox"></a>Create メソッド (ADOX)


**適用されます**Access 2013 |。Office 2013


新規カタログを作成します。

## <a name="syntax"></a>構文

*カタログ*です。*あわせて*を作成します。

## <a name="parameters"></a>パラメーター

  - *あわせて*

  - データ ソースとの接続に使用される文字列型 ( **String** ) の値を指定します。

## <a name="remarks"></a>解説

**Create** メソッドは、*ConnectString* で指定したデータ ソースへの新しい ADO [Connection](connection-object-ado.md) を作成して開きます。成功すると、新しい **Connection** オブジェクトが [ActiveConnection](activeconnection-property-adox.md) プロパティに割り当てられます。

プロバイダーが新しいカタログの作成をサポートしていない場合は、エラーが発生します。

