---
title: オブジェクトと、RDS プログラミング モデル
TOCTitle: RDS programming model with objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 079106e1c1a6651f68d10c5b93675c9b28b473e5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945521"
---
# <a name="rds-programming-model-with-objects"></a>オブジェクトと、RDS プログラミング モデル

**適用されます**Access 2013、Office 2013。

RDS の目的は、IIS などを中継してデータ ソースに対するアクセスおよび更新を行うことです。プログラミング モデルでは、この目的の達成に必要な一連の操作を指定します。オブジェクト モデルでは、プログラミング モデルに作用するメソッドおよびプロパティを持つオブジェクトを指定します。

RDS は、次に示す一連の操作を実行する手段を提供します。

- サーバー上で呼び出すプログラムを指定し、クライアント ([RDS.DataSpace](dataspace-object-rds.md)) がそのプログラムを参照する手段 (プロキシ) を獲得します。

- サーバー プログラムを呼び出します。データ ソースおよび発行するコマンドを識別するためのパラメーターをサーバー プログラムに渡します (プロキシまたは [RDS.DataControl](datacontrol-object-rds.md))。

- サーバー プログラムは、データ ソースから [Recordset](recordset-object-ado.md) オブジェクトを取得します。通常は、ADO を使用して取得します。また、**Recordset** オブジェクトをサーバー上で処理することもできます ([RDSServer.DataFactory](datafactory-object-rdsserver.md))。

- サーバー プログラムは、処理結果の **Recordset** オブジェクトをクライアント アプリケーション (プロキシ) に返します。

- クライアントでは、返された **Recordset** オブジェクトを、ビジュアル コントロールで使用しやすい形式に変換します (ビジュアル コントロールおよび **RDS.DataControl**)。

- **Recordset** オブジェクトに加えられた変更がサーバーに送り返され、その変更がデータ ソースに反映されます (**RDS.DataControl** または **RDSServer.DataFactory**)。

