---
title: Command オブジェクトの概要
TOCTitle: Command object overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f2c7697d4ae8b830afb53eee10e7dd59a7dc8db4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296165"
---
# <a name="command-object-overview"></a>Command オブジェクトの概要

**適用先:** Access 2013、Office 2013

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

