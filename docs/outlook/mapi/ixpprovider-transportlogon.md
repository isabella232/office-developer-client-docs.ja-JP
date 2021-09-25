---
title: IXPProviderTransportLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPProvider.TransportLogon
api_type:
- COM
ms.assetid: 534929f2-36a2-463d-8c4c-d86060cde127
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ab5b98ce47e35c820227bea9d666904026fbd76e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579719"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションがトランスポート プロバイダーにログオンするセッションを確立します。 
  
```cpp
HRESULT TransportLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG FAR * lpulFlags,
  LPMAPIERROR FAR * lppMAPIError,
  LPXPLOGON FAR * lppXPLogon
);
```

## <a name="parameters"></a>パラメーター

_lpMAPISup_: [in] このセッションの MAPI 内のコールバック関数のトランスポート プロバイダーのサポート オブジェクトへのポインター。 このオブジェクトは、トランスポート プロバイダーがリリースするまで有効なままです。
    
_ulUIParam_: [in] このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウを処理します。 _ulUIParam_ パラメーターは、たとえば lpulFlags パラメーターで LOGON_SETUPフラグが設定されている場合など _、null 以外の値を指定_ できます。 
    
_lpszProfileName_: [in] ユーザーのプロファイル名へのポインター。 _lpszProfileName_ パラメーターは、ダイアログ ボックスを表示する必要がある場合に主に使用されます。 
    
_lpulFlags_: [in, out] ログオン セッションの確立方法を制御するフラグのビットマスク。 MAPI スプーラーは、次のフラグを入力時に設定できます。
    
  - LOGON_NO_CONNECT: ユーザー アカウントは、メッセージの送受信以外の目的で、このトランスポート プロバイダーにログオンしています。 トランスポート プロバイダーは、他のメッセージング システムへの接続を試みる必要があります。
        
  - LOGON_NO_DIALOG: 現在保存されているユーザー資格情報が無効またはログオンに不十分な場合でも、ダイアログ ボックスは表示されません。
        
  - LOGON_NO_INBOUND: トランスポート プロバイダーはメッセージの受信を初期化する必要はありません。受信メッセージを受け入れる必要はありません。 MAPI スプーラーは、 [後で IXPLogon::TransportNotify](ixplogon-transportnotify.md) メソッドを使用して、受信メッセージ処理を有効にすることをトランスポート プロバイダーに通知できます。 
        
  - LOGON_NO_OUTBOUND: MAPI スプーラーが提供していないので、トランスポート プロバイダーはメッセージを送信するために初期化する必要があります。 クライアント アプリケーションがメッセージの構成中にリモート プロバイダーへの接続を必要とする場合 [、IXPLogon::AddressTypes](ixplogon-addresstypes.md) メソッド呼び出しを行うには、トランスポート プロバイダーが接続を確立する必要があります。 MAPI スプーラーは **、TransportNotify** を使用して、送信操作を開始できる場合にトランスポート プロバイダーに信号を送信できます。 
      
  - MAPI_UNICODE: プロファイル名の渡された文字列は Unicode 形式です。 MAPI UNICODE フラグ \_ が設定されていない場合、文字列は ANSI 形式です。
      
    次のフラグは、トランスポート プロバイダーによって出力に設定できます。
      
  - LOGON_SP_IDLE: MAPI スプーラーが、アイドル時間処理のためにトランスポート プロバイダー [の IXPLogon::Idle](ixplogon-idle.md) メソッドを頻繁に呼び出す要求。 
      
  - LOGON_SP_POLL: MAPI スプーラーが返されたログオン オブジェクトの [IXPLogon::P oll](ixplogon-poll.md) メソッドを頻繁に呼び出して、新しいメッセージを確認する要求。 このフラグが設定されていない場合、MAPI スプーラーは、トランスポート プロバイダーが [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドを使用して、処理する新しいメッセージが含まれることをスプーラーに通知するときにのみ、新しいメッセージをチェックします。 トランスポート プロバイダーは、このフラグを設定しないし、MAPI スプーラーにメッセージの受信を通知しない方法で、送信専用になります。 
      
  - LOGON_SP_RESOLVE: MAPI スプーラーが完全に解決する要求は、このトランスポート プロバイダーでサポートされていない受信者のすべてのメッセージ アドレスに対応します。 したがって、トランスポート プロバイダーは、すべての受信者の返信パスを作成できます。
      
  - MAPI_UNICODE: [MAPIERROR](mapierror.md) 構造体で返される文字列 (指定されている場合) は、Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
_lppMAPIError_: [out] エラーのバージョン、コンポーネント、およびコンテキスト情報を含む、返される **MAPIERROR** 構造体へのポインターを指すポインターがある場合。 _戻す MAPIERROR 構造体がない場合、lppMAPIError_ パラメーターを **NULL に** 設定できます。 
    
_lppXPLogon_: [out] 返されるトランスポート プロバイダー ログオン オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK: 呼び出しは成功し、予期される値または値を返しました。
    
MAPI_E_FAILONEPROVIDER: このプロバイダーはログオンできませんが、このエラーはサービスを無効にすることはできません。 
    
MAPI_E_UNCONFIGURED: プロファイルには、ログオンを完了するのに十分な情報が含まれている必要があります。 MAPI は、プロバイダーのメッセージ サービス エントリ ポイント関数を呼び出します。
    
MAPI_E_UNKNOWN_CPID: プロバイダーはクライアントのコード ページをサポートできません。
    
MAPI_E_UNKNOWN_LCID: プロバイダーは、クライアントのロケール情報をサポートできません。
    
MAPI_E_USER_CANCEL: ユーザーは、通常、ダイアログ ボックスの [キャンセル] ボタンをクリックして、操作をキャンセルしました。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーは **、IXPProvider::TransportLogon** メソッドを呼び出して、ユーザーのログオン セッションを確立します。 
  
ほとんどのトランスポート プロバイダーは、ユーザー ID 情報、サーバー アドレス、および資格情報を保存および取得するために _、lpMAPISup_ パラメーターが指すサポート オブジェクトで提供される [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを使用します。 **OpenProfileSection を使用** すると、トランスポート プロバイダーは任意の情報を保存し、それを特定のリソースへのログオンに関連付けできます。 たとえば、プロバイダーは **OpenProfileSection** を使用して、特定のセッションに関連付けられているアカウント名とパスワード、そのセッションのリソースにアクセスするために必要なサーバー名、その他の必要な情報を保存できます。 MAPI は、リソースに関連付けられた情報を外部アクセスから非表示にします。 _lpMAPISup_ を介して使用可能なプロファイル セクションは MAPI スプーラーによって管理されます。そのため、このユーザー コンテキストに関連するデータは、他のコンテキストのデータから分離されます。 
  
トランスポート プロバイダーは、サポート オブジェクトの **IUnknown::AddRef** メソッドを呼び出し、プロバイダー ログオン オブジェクトの一部としてこのオブジェクトへのポインターのコピーを保持する必要があります。 
  
_lpszProfileName_ のプロファイル表示名は、トランスポート プロバイダーがエラー メッセージまたはログオン ダイアログ ボックスで使用できるよう提供されます。 プロバイダーがこの名前を保持する場合は、プロバイダーによって割り当てられた記憶域にコピーする必要があります。 
  
他のサービス プロバイダーと緊密に結合されているトランスポート プロバイダーは、コンパニオン プロバイダー間の操作に必要な適切な資格情報を確立するために、ログオン時に追加の作業を行う必要があります。
  
通常、トランスポート プロバイダーは、ユーザーが最初にプロファイルにログオンするときに開きます。 したがって、プロファイルへの最初のログオンは通常、任意のメッセージ ストアにログオンする前に実行されるため、MAPI スプーラーは通常 _、lpulFlags_ で LOGON_NO_INBOUND フラグと LOGON_NO_OUTBOUND フラグの両方を設定して **TransportLogon** を呼び出します。 後で、適切なメッセージ ストアがプロファイル セッションで使用できる場合、MAPI スプーラーは **TransportNotify** を呼び出して、トランスポート プロバイダーの受信および送信操作を開始します。 
  
_lpulFlags_ LOGON_NO_CONNECTフラグを渡すと、トランスポート プロバイダーのオフライン操作が示されます。 このフラグは、外部接続を行う必要がないかどうかを示します。トランスポート プロバイダーが外部接続なしでセッションを確立できない場合は、ログオンのエラー値を返す必要があります。 
  
システムがアイドル状態で使用する時間を使用するように設計されている場合、トランスポート プロバイダーは初期化時に  _lpulFlags_ の LOGON_SP_IDLE フラグを設定する必要があります。 このような時間は、自動メッセージのダウンロード、時限メッセージのダウンロード、時限メッセージの送信など、自動操作を処理するためによく使用されます。 このフラグが設定されている場合、MAPI スプーラーは、このような操作を開始するためにシステム アイドル時間が発生するとアイドル状態を呼び出します。 MAPI スプーラーは、設定された **間隔で Idle** を呼び出す必要があります。むしろ、これは本当のアイドル時間の間にのみ呼び出されます。 したがって、プロバイダーは、Idle メソッドの呼び出し頻度に関するいかなる前提にも取り組む必要があります。 アイドル時間操作をサポートするプロバイダーは、プロバイダー のプロパティ シートに構成ユーザー インターフェイスを提供する必要があります。 
  
トランスポート プロバイダーのログオンが成功した場合、プロバイダーはログオン オブジェクトへのポインター  _を lppXPLogon_ パラメーターに返す必要があります。 MAPI スプーラーは、追加のプロバイダー アクセスにこのオブジェクトを使用します。 **TransportLogon がログオン** ダイアログ ボックスを表示し、ユーザーが通常、ダイアログ ボックスの [キャンセル] ボタンをクリックしてログオンを取り消した場合、プロバイダーはユーザーにログオンをMAPI_E_USER_CANCEL。 
  
**TransportLogon** から返されるほとんどのエラー値では、MAPI はプロバイダーが属するメッセージ サービスを無効にします。 MAPI は、そのサービスに属するプロバイダーを MAPI セッションの残りの部分で呼び出す必要があります。 これに対し **、TransportLogon** がログオンMAPI_E_FAILONEPROVIDERエラー値を返しても、MAPI はプロバイダーが属するメッセージ サービスを無効にしない。 **TransportLogon は** 、MAPI_E_FAILONEPROVIDERサービスを無効にしないエラーが発生した場合は、このエラーを返す必要があります。 
  
プロバイダーがログオンからMAPI_E_UNCONFIGURED場合、MAPI はプロバイダーのメッセージ サービス エントリ関数を呼び出し、ログオンを再試行します。 MAPI はMSG_SERVICE_CONFIGUREをコンテキストとして渡し、サービスに自身を構成する機会を与えます。 クライアントがログオン時にユーザー インターフェイスを許可する場合、サービスは構成プロパティ シートを提示して、ユーザーが構成情報を入力できます。 
  
プロバイダーが必要なすべての情報がプロファイルに含されていないと見つけた場合は、MAPI がプロバイダーのメッセージ サービス エントリ ポイント関数を呼び出すMAPI_E_UNCONFIGURED を返す必要があります。 
  
## <a name="see-also"></a>関連項目

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

