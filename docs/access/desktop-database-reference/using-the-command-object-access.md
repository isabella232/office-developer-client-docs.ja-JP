---
title: Command オブジェクトを使用する (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 63c7b2a572281353e1d498960f9f9ea59b2e6c08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562063"
---
# <a name="using-the-command-object-access"></a>Command オブジェクトの使用 (Access)


**適用先:** Access 2013、Office 2013

データ ソースに接続した後、データ ソースに対して要求を実行して結果セットを取得する必要があります。ADO では、この種類のコマンド機能を **Command** オブジェクトでカプセル化します。

**Command** オブジェクトを使用すると、プロバイダーがコマンド文字列を正しく解釈できる場合、プロバイダーに任意の種類の操作を要求できます。データ プロバイダーに対する一般的な操作では、データベースを照会して、**Recordset** オブジェクトにレコードを返します。**Recordset** については、この章とその他の章で後述しますが、ここでは、結果セットを保持および表示するためのツールと考えてください。多くの ADO オブジェクトと同様に、プロバイダーの機能によっては、**Command** オブジェクトのコレクション、メソッド、またはプロパティを参照したときにエラーが発生する場合があります。

データ ソースに対してコマンドを実行する際に、 **Command** オブジェクトを必ず作成しなければならないわけではありません。 **Connection** オブジェクトで **Execute** メソッドを使用することも、 **Recordset** オブジェクトで **Open** メソッドを使用することもできます。ただし、コード内でコマンドを再利用する必要がある場合、またはコマンドに詳細なパラメーター情報を渡す必要がある場合は、 **Command** オブジェクトを使用する必要があります。これらのシナリオについては、この章の後半で詳しく説明します。

> [!NOTE]
> プロバイダーがサポートしている場合、特定の Command は、結果セットを Recordset としてではなく、バイナリ ストリームまたは 1 つの Record として返すことができます。 また、結果セットをまったく返さない Command もあります (SQL Update クエリなど)。 ただし、この章では、Recordset オブジェクトに結果を返す Command の実行という最も一般的なシナリオについて説明します。 結果を Record または Stream に返す方法の詳細については、「[10 章: レコードとストリーム](chapter-10-records-and-streams.md)」を参照してください。

このセクションでは、以下のトピックについて説明します。

- [Command オブジェクトの概要](command-object-overview.md)
- [簡単なコマンドの作成と実行](creating-and-executing-a-simple-command.md)
- [Command オブジェクトのパラメーター](command-object-parameters.md)
- [コマンドを使用したストアド プロシージャの呼び出し](calling-a-stored-procedure-with-a-command.md)
- [名前付きコマンド](named-commands.md)
