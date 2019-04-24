---
title: スクリプト言語で ADO を使用する
TOCTitle: Using ADO with Scripting Languages
ms:assetid: 2e163ffb-22fe-36f5-9960-8f6bcb148183
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249074(v=office.15)
ms:contentKeyID: 48543985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ab0615d1c16900e86a844635fad4ac9a90751a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312042"
---
# <a name="using-ado-with-scripting-languages"></a>スクリプトの言語での ADO の使用


**適用先:** Access 2013、Office 2013

スクリプト環境では、ADO を使用することで、サーバー側スクリプトによりデータを公開できます。 このシナリオでは、ADO、ADO が利用する基盤の OLE DB プロバイダー、および特定のデータ ストアを参照するために必要な他のコンポーネントが、インターネット インフォメーション サービス (IIS) を実行するサーバーにインストールされます。 たとえば、Active Server Pages (ASP) を使用する場合、ADO は HTML を生成できるスクリプトで参照されるコンポーネントです。 この HTML コンテンツは、HTTP を介してクライアント web ブラウザーに渡すことができます。 スクリプトを使用すると、web ページはサーバー側スクリプトにアクションを送り返すことができるため、特定のデータを更新、スキャン、または表示することができます。

## <a name="odbc-data-sources"></a>ODBC データ ソース

スクリプト ADO コードと非スクリプト ADO コードの大きな違いの 1 つは、ODBC データ ソースです (使用した場合)。非スクリプト アプリケーションの場合、ODBC データ ソース アドミニストレーターでユーザー DSN を作成できます。IIS で実行するスクリプトの場合は、システム DSN を作成する必要があります。システム DSN を作成しないと、スクリプトは作成したデータ ソースを認識できません。このことは、Microsoft IIS を通して Microsoft OLE DB Provider for ODBC を使用するすべての ADO スクリプト アプリケーションに当てはまります。

## <a name="referencing-the-ado-library"></a>ADO ライブラリの参照

スクリプト言語では使用できません。

## <a name="handling-events"></a>イベントの処理

スクリプト言語では使用できません。

以下のトピックでは、スクリプト言語で ADO を使用する方法を詳細に説明しています。

- [JScript での ADO プログラミング](jscript-ado-programming.md)

- [VBScript での ADO プログラミング](vbscript-ado-programming.md)
