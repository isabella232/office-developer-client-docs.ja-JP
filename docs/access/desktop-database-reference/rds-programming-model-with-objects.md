---
title: RDS プログラミング モデルとオブジェクト
TOCTitle: RDS programming model with objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9743fb1e7329457abb60ed8ed41bc39067f3551d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710966"
---
# <a name="rds-programming-model-with-objects"></a>RDS プログラミング モデルとオブジェクト

**適用されます**Access 2013、Office 2013。

RDS の目的は、IIS などを中継してデータ ソースに対するアクセスおよび更新を行うことです。プログラミング モデルでは、この目的の達成に必要な一連の操作を指定します。オブジェクト モデルでは、プログラミング モデルに作用するメソッドおよびプロパティを持つオブジェクトを指定します。

RDS は、次に示す一連の操作を実行する手段を提供します。

- サーバー上で呼び出すプログラムを指定し、クライアント ([RDS.DataSpace](dataspace-object-rds.md)) がそのプログラムを参照する手段 (プロキシ) を獲得します。

- サーバー プログラムを呼び出します。データ ソースおよび発行するコマンドを識別するためのパラメーターをサーバー プログラムに渡します (プロキシまたは [RDS.DataControl](datacontrol-object-rds.md))。

- サーバー プログラムは、データ ソースから [Recordset](recordset-object-ado.md) オブジェクトを取得します。通常は、ADO を使用して取得します。また、**Recordset** オブジェクトをサーバー上で処理することもできます ([RDSServer.DataFactory](datafactory-object-rdsserver.md))。

- サーバー プログラムは、処理結果の **Recordset** オブジェクトをクライアント アプリケーション (プロキシ) に返します。

- クライアントでは、返された **Recordset** オブジェクトを、ビジュアル コントロールで使用しやすい形式に変換します (ビジュアル コントロールおよび **RDS.DataControl**)。

- **Recordset** オブジェクトに加えられた変更がサーバーに送り返され、その変更がデータ ソースに反映されます (**RDS.DataControl** または **RDSServer.DataFactory**)。

