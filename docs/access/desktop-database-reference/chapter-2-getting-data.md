---
title: '第 2 章: データの取得'
TOCTitle: 'Chapter 2: Getting Data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b045676cad97ffa1dc60f7370ec5013d4c30bdf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888077"
---
# <a name="chapter-2-getting-data"></a>第 2 章: データの取得


**適用されます**Access 2013、Office 2013。

前の章では、ADO アプリケーションの作成に必要となる、データの取得、データの確認、データの編集、およびデータの更新という 4 つの主な操作について概説しました。この章では、最初の操作であるデータの取得に関連する概念の詳細について説明します。

この操作では、いくつかの ADO オブジェクトが一定の役割を果たします。まず、ADO **Connection** オブジェクトを使用して、データ ソースに接続します (このオブジェクトは暗黙的に作成される場合があります)。次に、ADO **Command** オブジェクトを使用して、実行内容に関する指示をデータ ソースに渡します (このオブジェクトも暗黙的に作成される場合があります)。データ ソースにコマンドを渡し、その応答を受信した結果は、通常、ADO **Recordset** オブジェクトとして表されます。

データを取得するには、アプリケーションは、DBMS、ファイル ストア、コンマ区切りテキスト ファイルなど、データ ソースとの通信にする必要があります。 この通信*接続*とは、データを交換するために必要な環境。

ADO のオブジェクト モデルでは、接続の概念を **Connection** オブジェクトで表します。これは、ADO の多くの機能の基盤となるものです。 **Connection** オブジェクトの目的は次のとおりです。

  - ADO が、データ ソースと通信し、セッションを確立するために必要な情報を定義します。

  - セッションのトランザクション機能を定義します。

  - コマンドを作成し、データ ソースに対して実行できるようにします。

  - 基になるデータ ソースのデザインに関する情報をスキーマ行セットの形で提供します。スキーマ行セットの詳細については、「[OpenSchema メソッド (ADO)](openschema-method-ado.md)」を参照してください。

この章では、次のトピックについて説明します。

  - [接続を作成する](making-a-connection.md)

  - [Connection オブジェクトの使用のリファレンス (ADO)](using-the-connection-object-access.md)

  - [Command オブジェクトの使用のリファレンス (ADO)](using-the-command-object-access.md)

  - [レコードセットにデータを追加する (ADO)](adding-data-to-a-recordset.md)