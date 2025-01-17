---
title: MAPI へのログオン
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: df5bb9c117c568889af18c4fd1accd6589390d5f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579633"
---
# <a name="logging-on-to-mapi"></a>MAPI へのログオン
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションは、MAPILogonEx 関数を呼び出して **MAPI サブシステムにログオン** します。 詳細については [、「MAPILogonEx」を参照してください](mapilogonex.md)。 **MAPILogonEx** は、プロファイルの選択と、プロファイル内の各サービス プロバイダーの構成を検証します。 構成が完了すると、MAPI はメッセージ ストア プロバイダーを開始する前にアドレス帳プロバイダーを開始します。 トランスポート プロバイダーは、サービスが最初に必要なときに開始されます。 
  
## <a name="choose-a-profile"></a>プロファイルの選択
  
- _lpszProfileName_ パラメーター内のプロファイルの名前を表す文字列を **MAPILogonEx** に渡します。
    
- _lpszProfileName_ パラメーターに NULL を渡し、MAPI_LOGON_UIフラグを設定することで、プロファイルを指定できます。 

- _lpszProfileName_ パラメーターに NULL を渡し、既定のプロファイルフラグをMAPI_USE_DEFAULTします。 
    
既定のプロファイル以外の特定のプロファイルが必要な場合は、その名前を独自の構成データベースに保存するか、特定の名前付け規則を使用する必要があります。 MAPI では、プロファイル テーブルの名前と既定のフラグ以外のプロファイル属性は公開されません。既定のプロファイル フラグはメッセージング クライアントおよび関連する IPM アプリケーション用に予約されています。
  
**MAPILogonEx** に部分的なプロファイルまたはプロバイダー構成情報を提供するクライアントは、ダイアログ ボックスを表示できるようにして、ユーザーに追加データの入力を求める必要があります。 情報が不足し **、MAPILogonEx** がユーザーに入力を求めできない場合、ログオンは失敗します。 ユーザー入力を必要としないクライアントは、ダイアログ ボックスの表示を抑制できます。 
  
**MAPILogonEx がユーザー** インターフェイスを有効にするために使用するフラグは、相互に排他的です。設定できるのは 1 つのみです。 これらのフラグを設定解除すると、ユーザー インターフェイスの表示が抑制され、必要な情報が見つからない場合 **に MAPILogonEx** が失敗します。 つまり、ユーザー インターフェイスを無効にし  _、lpszProfileName_ パラメーターに NULL を渡し、MAPI_USE_DEFAULT フラグを設定しない場合 **、MAPILogonEx** はプロファイル名を取得できないので失敗します。 
  
**MAPILogonEx** が確立するセッションには、個別のメッセージング セッション、共有メッセージング セッション、または非messaging セッションを指定できます。 個々のメッセージング セッションは、クライアントと MAPI サブシステム間のプライベート接続であり **、MAPILogonEx** への呼び出しで MAPI_NEW_SESSION フラグを設定することで確立できます。
  
共有メッセージング セッションは、複数のメッセージング クライアントが使用できる接続です。 共有セッションは、通常、クライアントが同じプロファイルを使用するために確立されます。 共有セッションとして新しいセッションを確立するには、MAPI_ALLOW_OTHERS設定します。 
  
## <a name="use-an-existing-shared-session"></a>既存の共有セッションを使用する
  
- このフラグを設定MAPI_NEW_SESSIONしない。
    
- このフラグを設定MAPI_ALLOW_OTHERSしない。
    
- _lpszProfileName パラメーターに NULL を渡_ します。 
    
- _lpszPassword パラメーターに NULL を渡_ します。 
    
非messaging セッションでは、クライアントは MAPI サブシステムにアクセスできますが、メッセージの送信または受信は許可されません。 構成アプリケーションまたは管理アプリケーションは、非messaging セッションを確立する必要がある可能性があるクライアントの例です。 非messaging セッションを要求するには、次のフラグMAPI_NO_MAILします。 このフラグを設定すると、MAPI スプーラーに通知せずにクライアントがログオンします。 このフラグを使用して MAPI にログオンするクライアントは、読み取り状態レポートを受け取る必要があります。
  
次MAPI_NO_MAILフラグを設定する必要があります。
  
- セッション中にクライアントがメッセージを送受信しない場合。
    
- クライアントがプロファイルの内容を完全に制御し、Microsoft Exchange プロバイダーなどの緊密に結合されたメッセージ ストアとトランスポート プロバイダーを使用してメッセージを送信および受信する場合。
    
メッセージング クライアントは、セッションを非メッシュクライアントと共有できます。 共有セッションの 1 つのメンバーの特性は、他のメンバーの特性の影響を受け取る必要があります。 つまり、MAPI_NO_MAIL フラグと MAPI_ALLOW_OTHERS フラグセットを使用してログオンすると、セッションにログオンするメッセージング クライアントはクライアントの操作に影響を与え、その逆も影響を受け取らなくなります。 メッセージング クライアントは引き続きメッセージを送受信できます。クライアントはメッセージを送受信しません。
  
**MAPILogonEx には** 、設定できるその他のフラグがいくつか定義されています。 
  
- MAPI_FORCE_DOWNLOAD MAPILogonEx が返される前に受信メッセージをダウンロード **する必要があります。** このフラグを設定しない場合、メッセージは後でバックグラウンドでダウンロードされます。 
    
- MAPI_SERVICE_UI_ALWAYS内のすべてのメッセージ サービスに構成ダイアログ ボックスが表示されるという要求があります。
    
- MAPI_NT_SERVICEクライアントがサービスとして実装Windowsします。 クライアントがサービスの場合は、このフラグを設定する必要があります。
    
ログオンが成功すると **、MAPILogonEx** は MAPI セッションへのポインターを返します。 このポインターを使用して **、IMAPISession インターフェイスのメソッドを呼び出** します。 詳細については [、「IMAPISession : IUnknown 」を参照してください](imapisessioniunknown.md)。 セッション ポインターは、セッションの種類に関係なく、それらを受け取るクライアントに固有であり、タスク間では無効です。
  

