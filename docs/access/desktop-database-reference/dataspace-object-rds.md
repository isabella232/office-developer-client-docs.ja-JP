---
title: DataSpace オブジェクト (RDS)
TOCTitle: DataSpace object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b5a5aa610483a59976461b6efada64fa4208f31a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615621"
---
# <a name="dataspace-object-rds"></a>DataSpace オブジェクト (RDS)

**適用先**: Access 2013、Office 2013

中間層にあるカスタム ビジネス オブジェクトにクライアント側プロキシを作成します。

## <a name="remarks"></a>注釈

リモート データ サービスでは、クライアント側コンポーネントが中間層にあるビジネス オブジェクトと通信するために、ビジネス オブジェクト プロキシが必要となります。プロキシは、プロセスまたはマシンの境界を越えて、アプリケーションの [Recordset](recordset-object-ado.md) データを簡単にパッケージ化したり、パッケージ化を解除したり、送信 (マーシャリング) したりできます。

リモート データ サービスは、 **RDS.DataSpace** オブジェクトの [CreateObject](createobject-method-rds.md) メソッドを使用して、ビジネス オブジェクト プロキシを作成します。ビジネス オブジェクト プロキシは、中間層のビジネス オブジェクトの相手方のインスタンスが作成されるたびに動的に作成されます。リモート データ サービスは、HTTP、HTTPS (HTTP Secure Sockets)、DCOM、およびインプロセス (クライアント コンポーネントとビジネス オブジェクトが同じコンピューター上に常駐している) の各プロトコルをサポートします。

> [!NOTE]
> [!メモ] **RDS.DataSpace** オブジェクトが HTTP プロトコルまたは HTTPS プロトコルを使用している場合、RDS は "状態のない" 形で動作します。つまり、クライアント要求に関する内部情報は、サーバーが応答を返した後破棄されます。

ビジネス オブジェクトは、ビジネス オブジェクト プロキシの存続期間中は存在しているように見えますが、実際には要求に対して応答を送信するまでの間しか存在しません。要求を発行すると (つまり、ビジネス オブジェクト上でメソッドを呼び出すと)、プロキシはサーバーへの新しい接続を開き、サーバーはビジネス オブジェクトの新しいインスタンスを作成します。ビジネス オブジェクトが要求に応答後、サーバーはビジネス オブジェクトを破棄し、接続を閉じます。

この動作から、ビジネス オブジェクト プロパティまたは変数を使用してデータを要求間で渡すことができないことがわかります。状態データを保持するには、ファイルやメソッドの引数など、別の機能を採用する必要があります。

**RDS.DataSpace** オブジェクトのクラス ID は、BD96C556-65A3-11D0-983A-00C04FC29E36 です。

