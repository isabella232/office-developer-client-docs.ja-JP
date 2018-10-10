---
title: Command オブジェクトを使用する (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36d7bf1b39186eca841e417473e31e2bfd3a2dfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476671"
---
# <a name="using-the-command-object-access"></a>Command オブジェクトを使用する (Access)


**適用されます**Access 2013 |。Office 2013

データ ソースに接続した後、データ ソースに対して要求を実行して結果セットを取得する必要があります。ADO では、この種類のコマンド機能を **Command** オブジェクトでカプセル化します。

**Command** オブジェクトを使用すると、プロバイダーがコマンド文字列を正しく解釈できる場合、プロバイダーに任意の種類の操作を要求できます。データ プロバイダーに対する一般的な操作では、データベースを照会して、**Recordset** オブジェクトにレコードを返します。**Recordset** については、この章とその他の章で後述しますが、ここでは、結果セットを保持および表示するためのツールと考えてください。多くの ADO オブジェクトと同様に、プロバイダーの機能によっては、**Command** オブジェクトのコレクション、メソッド、またはプロパティを参照したときにエラーが発生する場合があります。

データ ソースに対してコマンドを実行する際に、 **Command** オブジェクトを必ず作成しなければならないわけではありません。 **Connection** オブジェクトで **Execute** メソッドを使用することも、 **Recordset** オブジェクトで **Open** メソッドを使用することもできます。ただし、コード内でコマンドを再利用する必要がある場合、またはコマンドに詳細なパラメーター情報を渡す必要がある場合は、 **Command** オブジェクトを使用する必要があります。これらのシナリオについては、この章の後半で詳しく説明します。


> [!NOTE]
> <P>プロバイダーがサポートしている場合、特定の <STRONG>Command</STRONG> は、結果セットを <STRONG>Recordset</STRONG> としてではなく、バイナリ ストリームまたは 1 つの <STRONG>Record</STRONG> として返すことができます。また、結果セットをまったく返さない <STRONG>Command</STRONG> もあります (SQL Update クエリなど)。ただし、この章では、<STRONG>Recordset</STRONG> オブジェクトに結果を返す <STRONG>Command</STRONG> の実行という最も一般的なシナリオについて説明します。結果を <STRONG>Record</STRONG> または <STRONG>Stream</STRONG> に返す方法の詳細については、「<A href="chapter-10-records-and-streams.md">10 章: レコードとストリーム</A>」を参照してください。</P>


