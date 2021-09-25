---
title: RDS アプリケーションをセキュリティ保護する
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49476ab8bf3af8fadf4127fabd2966e888981af6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596877"
---
# <a name="securing-rds-applications"></a>RDS アプリケーションをセキュリティ保護する

**適用先**: Access 2013、Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Microsoft Internet Explorer のセキュリティの問題点

Microsoft Internet Explorer に新しいセキュリティ強化が追加され、一部の ADO オブジェクトと RDS オブジェクトは"安全" モード環境でのみ実行に制限されます。 そのため、ゾーンの相違、セキュリティ レベル、動作の制限、安全でない操作、カスタマイズされたセキュリティ設定などの問題に注意を払う必要があります。

これらの問題の詳細については、「ADO」 (英語) の「ADO and RDS Security Issues in Microsoft Internet Explorer」 (英語) を参照してください。

## <a name="security-and-your-web-server"></a>セキュリティと Web サーバー

インターネット Web サーバーで [RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを使用する場合は、セキュリティリスクが発生する可能性があります。 有効なデータ ソース名 (DSN)、ユーザー ID、およびパスワードの情報を持っている外部ユーザーであれば、そのデータ ソースにクエリを送信するページを作成できます。 データ ソースへのアクセスを制限する方法の 1 つとして、 **RDSServer.DataFactory** オブジェクト (msadcf.dll) の登録を解除して削除し、その代わりに、ハード コーディングされたクエリを使うカスタム ビジネス オブジェクトを使う方法があります。

RDSServer.DataFactory オブジェクトを使用する場合のセキュリティへの影響の詳細については、Microsoft セキュリティ Web サイトの Microsoft セキュリティ情報 MS99-025 を [参照してください](https://www.microsoft.com/en-us/security/default.aspx)。

## <a name="client-impersonation-and-security"></a>クライアントの偽装とセキュリティ

IIS  Web サーバーのパスワード認証プロパティが Windows NT チャレンジ/応答認証 (Windows NT 4.0 の場合) または統合 Windows 認証 (Windows 2000 の場合) に設定されている場合、ビジネス オブジェクトはクライアントのセキュリティ コンテキストで呼び出されます。 This is a new feature in RDS 1.5 that allows Client Impersonation over HTTP. このモードで作業する場合、Web サーバー (IIS) へのログオンは匿名ではなく、クライアント コンピューターが実行されているユーザー ID とパスワードを使用します。 If the ODBC DSNs are set up to use Trusted Connection, then access to databases, such as SQL Server, also happens under the client's security context. But this only works if the database is on the same computer as the IIS; the client credentials cannot be carried over to yet another computer.

たとえば、userid="JohnD" と password="secret" を持つクライアント John Doe がクライアント コンピューターにログオンします。 IIS を実行している "MyServer" コンピューターで SQL クエリを実行して **、RDSServer.DataFactory** オブジェクトにアクセスして [Recordset](recordset-object-ado.md)を作成する必要があるブラウザー ベースのアプリケーションを実行します。 Windows NT Server 4.0 を実行しているシステムである MyServer は、Windows NT チャレンジ/応答認証を使用するためにセットアップされ、ODBC DSN の [信頼できる接続の使用] が選択され、サーバーには SQL Server データ ソースも含まれる。 Web サーバーで要求を受信すると、クライアントにユーザー ID とパスワードを要求します。 したがって、要求は IUSER MyServer ではなく "JohnD"/"Secret" からの要求として MyServer に記録されます (これは、匿名パスワード認証がオンの場合の既定値 \_ です)。 同様に、ユーザーにログオンSQL Server"JohnD"/"Secret" が使用されます。

したがって、IIS の Windows NT チャレンジ/レスポンス認証モードでは、ユーザーはデータベースへのログオンに必要なユーザー ID とパスワードを明示的に要求されることなく HTML ページを作成できます。IIS の基本認証が使われている場合は、これらが要求されます。

## <a name="password-authentication"></a>パスワード認証

RDS は、匿名認証、基本認証、NT チャレンジ/応答認証 (Windows 2000 年の統合 Windows 認証と呼ばれる) のいずれかの 3 つのパスワード認証モードで実行されている IIS Web サーバーと通信できます。 これらの設定は、クライアント コンピューターが NT Web サーバーに対して明示的なアクセス権を持つ必要があるなど、Web サーバーがアクセスを制御する方法を定義します。

