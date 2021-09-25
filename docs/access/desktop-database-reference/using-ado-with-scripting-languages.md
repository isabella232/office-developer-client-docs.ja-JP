---
title: スクリプト言語で ADO を使用する
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ae1812a3d141f9466d1ff4d332cb09f557dfd53b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580623"
---
# <a name="using-ado-with-scripting-languages"></a>スクリプトの言語での ADO の使用


**適用先:** Access 2013、Office 2013

スクリプト環境では、ADO を使用することで、サーバー側スクリプトによりデータを公開できます。 このシナリオでは、ADO、ADO が利用する基盤の OLE DB プロバイダー、および特定のデータ ストアを参照するために必要な他のコンポーネントが、インターネット インフォメーション サービス (IIS) を実行するサーバーにインストールされます。 たとえば、Active Server Pages (ASP) を使用する場合、ADO は HTML を生成できるスクリプトで参照されるコンポーネントです。 この HTML コンテンツは、HTTP 経由でクライアント Web ブラウザーに渡されます。 スクリプトを使用することで、Web ページはアクションをサーバー側スクリプトに送り返し、特定のデータを更新、トラバース、または表示できます。

## <a name="odbc-data-sources"></a>ODBC データ ソース

スクリプト ADO コードと非スクリプト ADO コードの大きな違いの 1 つは、ODBC データ ソースです (使用した場合)。非スクリプト アプリケーションの場合、ODBC データ ソース アドミニストレーターでユーザー DSN を作成できます。IIS で実行するスクリプトの場合は、システム DSN を作成する必要があります。システム DSN を作成しないと、スクリプトは作成したデータ ソースを認識できません。このことは、Microsoft IIS を通して Microsoft OLE DB Provider for ODBC を使用するすべての ADO スクリプト アプリケーションに当てはまります。

## <a name="referencing-the-ado-library"></a>ADO ライブラリの参照

スクリプト言語では使用できません。

## <a name="handling-events"></a>イベントの処理

スクリプト言語では使用できません。

以下のトピックでは、スクリプト言語で ADO を使用する方法を詳細に説明しています。

- [JScript での ADO プログラミング](jscript-ado-programming.md)

- [VBScript での ADO プログラミング](vbscript-ado-programming.md)
