---
title: コマンド オブジェクトの概要
TOCTitle: Command object overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 65ca58b7a2edc0397207cf7bbf6a001349ffc636
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947393"
---
# <a name="command-object-overview"></a>コマンド オブジェクトの概要

**適用されます**Access 2013、Office 2013。

**Command** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。

  - **CommandText** プロパティを使用して、コマンドの実行可能なテキスト (SQL ステートメントやストアド プロシージャなど) を定義できます。

  - **Parameter** オブジェクトと **Parameters** コレクションを使用して、パラメーター付きクエリやストアド プロシージャの引数を定義できます。

  - **Execute** メソッドを使用して、コマンドを実行し、必要に応じて **Recordset** オブジェクトを返すことができます。

  - **CommandType** プロパティを使用して、コマンドを実行する前にそのコマンドの種類を指定し、パフォーマンスを向上させることができます。

  - **Prepared** プロパティを使用して、コマンドの実行前に、プロバイダーがそのコマンドの準備された (コンパイル済みの) バージョンを保存するかどうかを制御できます。

  - **CommandTimeout** プロパティを使用して、コマンドの実行までプロバイダーが待機する時間を秒数で設定できます。

  - **Command** オブジェクトの **ActiveConnection** プロパティを使用して、開いている接続をそのオブジェクトに関連付けることができます。

  - **Name** プロパティを設定して、 **Command** オブジェクトを関連付けられている **Connection** オブジェクトのメソッドとして識別できます。

  - **Command** オブジェクトを **Recordset** の **Source** プロパティに渡すことにより、データを取得できます。

