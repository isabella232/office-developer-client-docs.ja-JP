---
title: Command オブジェクトを使用する (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b89d292d86035e565ad18413062274dfbfc74db
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709328"
---
# <a name="using-the-command-object-access"></a>コマンド オブジェクト (Access) を使用してください。


**適用されます**Access 2013、Office 2013。

データ ソースに接続した後、データ ソースに対して要求を実行して結果セットを取得する必要があります。ADO では、この種類のコマンド機能を **Command** オブジェクトでカプセル化します。

**Command** オブジェクトを使用すると、プロバイダーがコマンド文字列を正しく解釈できる場合、プロバイダーに任意の種類の操作を要求できます。データ プロバイダーに対する一般的な操作では、データベースを照会して、**Recordset** オブジェクトにレコードを返します。**Recordset** については、この章とその他の章で後述しますが、ここでは、結果セットを保持および表示するためのツールと考えてください。多くの ADO オブジェクトと同様に、プロバイダーの機能によっては、**Command** オブジェクトのコレクション、メソッド、またはプロパティを参照したときにエラーが発生する場合があります。

データ ソースに対してコマンドを実行する際に、 **Command** オブジェクトを必ず作成しなければならないわけではありません。 **Connection** オブジェクトで **Execute** メソッドを使用することも、 **Recordset** オブジェクトで **Open** メソッドを使用することもできます。ただし、コード内でコマンドを再利用する必要がある場合、またはコマンドに詳細なパラメーター情報を渡す必要がある場合は、 **Command** オブジェクトを使用する必要があります。これらのシナリオについては、この章の後半で詳しく説明します。

> [!NOTE]
> 特定のコマンドは、プロバイダーでサポートされる場合、結果セットのバイナリ ストリームとしてまたは 1 つのレコードとしてではなく、レコード セットを返すことができます。 いくつかのコマンドは結果セットのすべての (SQL Update クエリなど) を取得するものではありません。 この章では説明の最も一般的なシナリオ、ただし: 結果を返す Recordset オブジェクトにコマンドを実行します。 レコードまたはストリームに結果を取得する方法の詳細についてを参照してください[第 10 章: レコードとストリーム](chapter-10-records-and-streams.md)。

このセクションには、次のトピックが含まれています。

- [Command オブジェクトの概要](command-object-overview.md)
- [簡単なコマンドの作成と実行](creating-and-executing-a-simple-command.md)
- [Command オブジェクトのパラメーター](command-object-parameters.md)
- [コマンドを使用したストアド プロシージャの呼び出し](calling-a-stored-procedure-with-a-command.md)
- [名前付きコマンド](named-commands.md)
