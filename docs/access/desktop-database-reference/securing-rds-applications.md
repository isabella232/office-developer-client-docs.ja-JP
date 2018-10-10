---
title: RDS アプリケーションをセキュリティ保護する
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16dd0fd983d6e04f01c7d848a8d45f82b0f1c85a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476677"
---
# <a name="securing-rds-applications"></a>RDS アプリケーションをセキュリティ保護する

**適用されます**Access 2013 |。Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Microsoft Internet Explorer のセキュリティの問題点

Microsoft® Internet Explorer に新しいセキュリティ機能が追加されたことに伴い、いくつかの ADO オブジェクトと RDS オブジェクトは "セーフ" モード環境でしか動作しなくなりました。そのため、ゾーンの相違、セキュリティ レベル、動作の制限、安全でない操作、カスタマイズされたセキュリティ設定などの問題に注意を払う必要があります。

これらの問題の詳細については、「ADO」 (英語) の「ADO and RDS Security Issues in Microsoft Internet Explorer」 (英語) を参照してください。

## <a name="security-and-your-web-server"></a>セキュリティと Web サーバー

インターネット Web サーバーで [DataFactory (RDSServer)](datafactory-object-rdsserver.md) オブジェクトを使う場合は、それによりセキュリティ上の潜在的なリスクが発生することに留意してください。有効なデータ ソース名 (DSN)、ユーザー ID、およびパスワードの情報を持っている外部ユーザーであれば、そのデータ ソースにクエリを送信するページを作成できます。データ ソースへのアクセスを制限する方法の 1 つとして、 **RDSServer.DataFactory** オブジェクト (msadcf.dll) の登録を解除して削除し、その代わりに、ハード コーディングされたクエリを使うカスタム ビジネス オブジェクトを使う方法があります。

RDSServer.DataFactory オブジェクトを使用する場合のセキュリティへの影響の詳細については、[マイクロソフト セキュリティ web サイト](https://www.microsoft.com/en-us/security/default.aspx)マイクロソフト セキュリティ情報 MS99-025 を参照してください。

## <a name="client-impersonation-and-security"></a>クライアントの偽装とセキュリティ

(Windows NT 4.0) を Windows NT チャレンジ/レスポンス認証または統合 Windows 認証 (Windows 2000) を IIS Web サーバーの**パスワード認証**のプロパティが設定されている場合は、クライアントの [ビジネス オブジェクトが呼び出されます。セキュリティ コンテキストです。 これは、HTTP 経由でクライアントの偽装を可能にする RDS 1.5 の新機能です。 このモードで作業するとき、Web サーバー (IIS) へのログオンは匿名ではありませんが、ユーザー ID とクライアント コンピューターが実行されているパスワードを使用します。 ODBC の Dsn が信頼関係接続を使用する設定はなど、SQL Server のデータベースへのアクセスは、クライアントのセキュリティ コンテキストの下で。 これはデータベースが、IIS と同じコンピューター上にある場合にのみ有効ですが、さらに別のコンピューター上でクライアントの資格情報を実行できません。

例では、クライアントの場合、John Doe では、ユーザー id =「JohnD」とパスワード =「シークレット」は、クライアント コンピューターにログオンします。 彼は、IIS を実行している"MyServer"コンピューターで、SQL クエリを実行して[レコード セット](recordset-object-ado.md)を作成するのには**RDSServer.DataFactory**オブジェクトにアクセスする必要のあるブラウザー ベースのアプリケーションを実行します。 MyServer を Windows NT Server 4.0 を実行しているシステムが Windows NT チャレンジ/レスポンス認証を使用する設定、その ODBC DSN"を使用して、信頼関係接続] が選択されているが、サーバーは、SQL Server データ ソースも含まれています。 Web サーバーに要求が受信されると、ユーザー ID とパスワードをクライアントに要求します。 したがって、要求は、MyServer としてログオン「JohnD」から IUSER 代わりに「秘密」/\_MyServer (これは既定では匿名のパスワード認証がオンの場合)。 同様に、SQL Server、「JohnD」へのログオン時に「秘密」を使用します。

したがって、IIS の Windows NT チャレンジ/レスポンス認証モードでは、ユーザーはデータベースへのログオンに必要なユーザー ID とパスワードを明示的に要求されることなく HTML ページを作成できます。IIS の基本認証が使われている場合は、これらが要求されます。

## <a name="password-authentication"></a>パスワード認証

RDS は、匿名認証、基本認証、または Windows NT チャレンジ/レスポンス認証 (Windows 2000 では統合 Windows 認証) の 3 種類のパスワード認証モードのうち、どのモードで実行している IIS Web サーバーとも通信できます。これらの設定によって、たとえばクライアント コンピューターが NT Web サーバーに対して明示的なアクセス特権を持っている必要があるなど、Web サーバーがそのサーバーを介するアクセスを制御する方法が定義されます。

