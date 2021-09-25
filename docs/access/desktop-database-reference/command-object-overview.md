---
title: Command オブジェクトの概要
TOCTitle: Command object overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7f8be0fb8e199a33670f8388738b16b197ce9cf2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586138"
---
# <a name="command-object-overview"></a>Command オブジェクトの概要

**適用先**: Access 2013、Office 2013

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

