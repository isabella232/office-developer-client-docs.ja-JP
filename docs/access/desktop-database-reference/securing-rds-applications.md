---
title: RDS アプリケーションをセキュリティ保護する
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a531c01750117ae7abbf87e5ba4cb23daf37851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308779"
---
# <a name="securing-rds-applications"></a>RDS アプリケーションをセキュリティ保護する

**適用先:** Access 2013、Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Microsoft Internet Explorer のセキュリティの問題点

Microsoft Internet Explorer に追加された新しいセキュリティ機能により、一部の ADO および RDS オブジェクトは "安全な" モード環境でのみ実行されるように制限されています。 そのため、ゾーンの相違、セキュリティ レベル、動作の制限、安全でない操作、カスタマイズされたセキュリティ設定などの問題に注意を払う必要があります。

これらの問題の詳細については、「ADO」 (英語) の「ADO and RDS Security Issues in Microsoft Internet Explorer」 (英語) を参照してください。

## <a name="security-and-your-web-server"></a>セキュリティと web サーバー

インターネット web サーバーで[rdsserver.datafactory](datafactory-object-rdsserver.md)オブジェクトを使用する場合は、そのような場合にセキュリティ上のリスクが生じる可能性があることに注意してください。 有効なデータ ソース名 (DSN)、ユーザー ID、およびパスワードの情報を持っている外部ユーザーであれば、そのデータ ソースにクエリを送信するページを作成できます。 データ ソースへのアクセスを制限する方法の 1 つとして、 **RDSServer.DataFactory** オブジェクト (msadcf.dll) の登録を解除して削除し、その代わりに、ハード コーディングされたクエリを使うカスタム ビジネス オブジェクトを使う方法があります。

rdsserver.datafactory オブジェクトを使用した場合のセキュリティの影響の詳細については、microsoft[セキュリティ web サイト](https://www.microsoft.com/en-us/security/default.aspx)の「マイクロソフトセキュリティ情報 MS99-025 を参照してください。

## <a name="client-impersonation-and-security"></a>クライアントの偽装とセキュリティ

IIS web サーバーの**パスワード認証**プロパティが、windows nt チャレンジ/レスポンス認証 (windows nt 4.0 の場合) または統合 windows 認証 (windows 2000 の場合) に設定されている場合、ビジネスオブジェクトはクライアントの下で呼び出されます。セキュリティコンテキスト。 This is a new feature in RDS 1.5 that allows Client Impersonation over HTTP. このモードで作業している場合、web サーバー (IIS) へのログオンは匿名ではありませんが、クライアントコンピューターが実行しているユーザー ID とパスワードを使用します。 If the ODBC DSNs are set up to use Trusted Connection, then access to databases, such as SQL Server, also happens under the client's security context. But this only works if the database is on the same computer as the IIS; the client credentials cannot be carried over to yet another computer.

たとえば、クライアントの John Doe、userid = "JohnD"、password = "secret" がクライアントコンピューターにログオンしているとします。 rdsserver.datafactory オブジェクトにアクセスして、IIS を実行している "MyServer" コンピューターで SQL クエリを実行することによって、[レコードセット](recordset-object-ado.md)を作成するために、 **DataFactory**オブジェクトにアクセスする必要があるブラウザーベースのアプリケーションを実行します。 windows nt Server 4.0 を実行しているシステムは、windows nt チャレンジ/レスポンス認証を使用するように設定されており、ODBC DSN には [信頼された接続の使用] が選択されており、サーバーにも SQL Server データソースが含まれています。 web サーバーで要求が受信されると、クライアントにユーザー ID とパスワードが要求されます。 このため、要求は、iuser\_MyServer (匿名パスワード認証がオンになっている場合の既定値) ではなく、"JohnD"/"Secret" ではなく、myserver に記録されます。 同様に、SQL Server にログオンするときに、"JohnD"/"Secret" が使用されます。

したがって、IIS の Windows NT チャレンジ/レスポンス認証モードでは、ユーザーはデータベースへのログオンに必要なユーザー ID とパスワードを明示的に要求されることなく HTML ページを作成できます。IIS の基本認証が使われている場合は、これらが要求されます。

## <a name="password-authentication"></a>パスワード認証

RDS は、3つのパスワード認証モード (windows 2000 では統合 Windows 認証と呼ばれます) のいずれかで実行されている IIS web サーバーと通信できます。 これらの設定は、クライアントコンピューターが NT web サーバーに対して明示的なアクセス権限を持っている必要があるなど、web サーバーによるアクセスを制御する方法を定義します。

