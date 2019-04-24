---
title: '第 2 章: データの取得'
TOCTitle: 'Chapter 2: Getting data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f059e5dfe064442f10972fd36344e64f84fe7ea5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296445"
---
# <a name="chapter-2-getting-data"></a>第 2 章: データの取得

**適用先:** Access 2013、Office 2013

前の章では、ADO アプリケーションの作成に必要となる、データの取得、データの確認、データの編集、およびデータの更新という 4 つの主な操作について概説しました。この章では、最初の操作であるデータの取得に関連する概念の詳細について説明します。

この操作では、いくつかの ADO オブジェクトが一定の役割を果たします。まず、ADO **Connection** オブジェクトを使用して、データ ソースに接続します (このオブジェクトは暗黙的に作成される場合があります)。次に、ADO **Command** オブジェクトを使用して、実行内容に関する指示をデータ ソースに渡します (このオブジェクトも暗黙的に作成される場合があります)。データ ソースにコマンドを渡し、その応答を受信した結果は、通常、ADO **Recordset** オブジェクトとして表されます。

データを取得するには、アプリケーションがデータ ソース (DBMS、ファイル ストア、コンマ区切りテキスト ファイルなど) と通信できる状態にある必要があります。この通信とは、"接続"、つまりデータのやり取りに必要な環境を指します。

ADO のオブジェクト モデルでは、接続の概念を **Connection** オブジェクトで表します。これは、ADO の多くの機能の基盤となるものです。 **Connection** オブジェクトの目的は次のとおりです。

- ADO が、データ ソースと通信し、セッションを確立するために必要な情報を定義します。

- セッションのトランザクション機能を定義します。

- コマンドを作成し、データ ソースに対して実行できるようにします。

- 基になるデータ ソースのデザインに関する情報をスキーマ行セットの形で提供します。スキーマ行セットの詳細については、「[OpenSchema メソッド (ADO)](openschema-method-ado.md)」を参照してください。

この章では、次のトピックについて説明します。

- [接続の作成](making-a-connection.md)
- [connection オブジェクト参照 (ADO) の使用](using-the-connection-object-access.md)
- [command オブジェクト参照 (ADO) の使用](using-the-command-object-access.md)
- [Recordset にデータを追加する (ADO)](adding-data-to-a-recordset.md)
