---
title: IXPProviderTransportLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.TransportLogon
api_type:
- COM
ms.assetid: 534929f2-36a2-463d-8c4c-d86060cde127
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 01a8e3c479ab3ddd1be9386e033b993fda5835a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801308"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**適用されます**: Outlook 
  
クライアント アプリケーションへのログオンに、トランスポート プロバイダーのセッションを確立します。 
  
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

## <a name="parameters"></a>Parameters

_lpMAPISup_: [in] コールバック関数は、このセッションの MAPI 内のトランスポート プロバイダーのサポートのオブジェクトへのポインター。 このオブジェクトは、トランスポート プロバイダーは、それを解放するまで、有効なままになります。
    
_ulUIParam_: [入力] ダイアログ ボックスの親ウィンドウまたは windows のこのメソッドは、表示へのハンドルです。 _UlUIParam_パラメーターは null 以外であることができます、たとえば、 _lpulFlags_パラメーターに設定されて、LOGON_SETUP フラグを設定するとします。 
    
_lpszProfileName_: [in] ユーザーのプロファイルの名前へのポインター。 _LpszProfileName_パラメーターは、ダイアログ ボックスを表示する必要があるときに主に使用します。 
    
_lpulFlags_: [で, out] ログオン セッションが確立される方法を制御するフラグのビットマスクです。 MAPI スプーラーによって、入力時に次のフラグを設定できます。
    
  - LOGON_NO_CONNECT: ユーザー アカウントにログオンしているメッセージの送受信以外の目的では、このトランスポート プロバイダー。 トランスポート プロバイダーは、他のメッセージング システムへの接続を確認するのにはしないようにします。
        
  - LOGON_NO_DIALOG:] ダイアログ ボックスする必要があります表示しない場合でも、現在保存されているユーザーの資格情報が無効であるか、またはログオンの不足のためには。
        
  - LOGON_NO_INBOUND: トランスポート プロバイダーは、受信メッセージのために初期化する必要はありませんし、着信メッセージを受け付けませんする必要があります。 MAPI スプーラーは、着信メッセージの処理を有効にするのにトランスポート プロバイダーを通知するのに[IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッドを後で使用できます。 
        
  - LOGON_NO_OUTBOUND: MAPI スプーラーがいずれかを指定しないため、メッセージを送信するために初期化するために、トランスポート プロバイダーがありませんでした。 クライアント アプリケーションは、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドの呼び出しを行うことができるように、メッセージの構成時にリモートのプロバイダーへの接続を必要とするトランスポート プロバイダーは接続を確立する必要があります。 MAPI スプーラーは、送信操作を開始できる場合、トランスポート プロバイダーを通知するのに**TransportNotify**を使用できます。 
      
  - MAPI_UNICODE: プロファイル名に渡された文字列は Unicode 形式で表示します。 場合、MAPI\_ユニコード フラグが設定されていない、文字列が ANSI 形式では。
      
    トランスポート プロバイダーによって、出力に次のフラグを設定できます。
      
  - LOGON_SP_IDLE: 要求は、MAPI スプーラーは、アイドル時の処理のトランスポート プロバイダーの[IXPLogon::Idle](ixplogon-idle.md)メソッドを頻繁に呼び出します。 
      
  - LOGON_SP_POLL: MAPI スプーラー頻繁にメソッドを呼び出す[IXPLogon::Poll](ixplogon-poll.md)を確認する返されるログオン オブジェクトで新しいメッセージを要求します。 このフラグが設定されていない場合、MAPI スプーラーのみ新着メッセージをチェック トランスポート プロバイダーでは、 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを使用して、処理する新しいメッセージがあることをスプーラーに通知するとします。 トランスポート プロバイダー効果的になり、送信専用でこのフラグを設定していないメッセージの受信確認の MAPI スプーラーに通知しません。 
      
  - LOGON_SP_RESOLVE: 要求を解決するには、MAPI スプーラーを完全にこのトランスポート プロバイダーによっては、受信者のすべてのメッセージのアドレスがサポートされていないアドレスです。 したがってトランスポート プロバイダーがすべての受信者の返信パスを作成できます。
      
  - MAPI_UNICODE: [MAPIERROR](mapierror.md)構造体で返される文字列存在する場合、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
_lppMAPIError_: [出力] 返された**MAPIERROR**構造体へのポインターへのポインター、存在する場合、情報が含まれるバージョン、コンポーネント、およびコンテキスト、エラーが発生します。 取得する**MAPIERROR**構造体がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
_lppXPLogon_: [出力] 返されたトランスポート プロバイダー ログオン オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK: 呼び出しが成功し、予期される値または値が返されました。
    
MAPI_E_FAILONEPROVIDER: このプロバイダーは、ログオンできませんが、このエラーには、サービスが無効にする必要があります。 
    
MAPI_E_UNCONFIGURED: プロファイルへのログオンを完了するのに十分な情報がありません。 MAPI は、プロバイダーのメッセージ サービスのエントリ ポイント関数が呼び出されます。
    
MAPI_E_UNKNOWN_CPID: プロバイダーは、クライアントのコード ページをサポートすることはできません。
    
MAPI_E_UNKNOWN_LCID: プロバイダーは、クライアントのロケール情報をサポートすることはできません。
    
MAPI_E_USER_CANCEL: ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>備考

MAPI スプーラーでは、ユーザーのログオン セッションを確立するために**IXPProvider::TransportLogon**メソッドを呼び出します。 
  
ほとんどのトランスポート プロバイダーは、保存し、ユーザー識別情報、サーバーのアドレス、および資格情報を取得するための_lpMAPISup_パラメーターで指定されたサポート オブジェクトに用意されている[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを使用します。 **OpenProfileSection**を使用すると、トランスポート プロバイダーは任意の情報を保存し、特定のリソースへのログオンに関連付けることできます。 たとえば、プロバイダーは、アカウント名とパスワードが特定のセッションとすべてのサーバー名またはその他の必要な情報は、そのセッションでのリソースへのアクセスに必要な関連付けを保存するのには**OpenProfileSection**を使用できます。 MAPI には、外部アクセスからリソースに関連付けられている情報が非表示にします。 _LpMAPISup_を介して利用可能にするプロファイルのセクションは、このユーザーのコンテキストに関連するデータが他のコンテキストのデータから分離されているために、MAPI スプーラーによって管理されます。 
  
トランスポート プロバイダーは、サポート オブジェクトの**IUnknown::AddRef**メソッドを呼び出すし、プロバイダー ログオン オブジェクトの一部としてこのオブジェクトへのポインターのコピーを保持する必要があります。 
  
トランスポート プロバイダーを使用するとエラー メッセージまたはログオン] ダイアログ ボックスで使用できるように、 _lpszProfileName_でのプロファイルの表示名が用意されています。 プロバイダーは、この名前を保持している場合は、プロバイダーによって割り当てられた記憶域にコピーする必要があります。 
  
その他のサービス ・ プロバイダーと密に結合したトランスポート プロバイダーは、コンパニオン プロバイダー間での操作に必要な適切な資格情報を確立するのにはログオン時に追加の作業を行う必要があります。
  
通常、トランスポート プロバイダーは、ユーザーがプロファイルを最初にログオンしたときに開かれます。 最初のログオン プロファイルにそのためは、通常はログオンする前に、メッセージ ・ ストアにため、MAPI スプーラーは通常、 **TransportLogon**を LOGON_NO_INBOUND と LOGON_NO_OUTBOUND の両方のフラグを_lpulFlags_に設定して呼び出します。 以降では、適切なメッセージ ・ ストアがプロファイル セッションで使用できる場合は、MAPI スプーラーは、トランスポート プロバイダーの受信および送信の操作を開始するのには**TransportNotify**を呼び出します。 
  
トランスポート プロバイダーのオフライン操作は、 _lpulFlags_信号で LOGON_NO_CONNECT フラグを渡します。 このフラグを示します外部接続は行われません。トランスポート プロバイダーが外部接続を使用せず、セッションを確立できない場合は、ログオンのエラー値を返します。 
  
トランスポート プロバイダーする必要がありますフラグを設定 LOGON_SP_IDLE _lpulFlags_で初期化時にそれ以外のシステムが消費する時間を使用することが目的の場合アイドル。 このような時間は、ダウンロードすると、メッセージの自動タイムアウトのメッセージをダウンロードするメッセージの送信のタイムアウトなど、自動操作を処理するためによく使用されます。 このフラグが設定されている場合、MAPI スプーラーは、このような操作を開始するのにはシステムのアイドル時間が発生したとき**アイドル**を呼び出します。 MAPI スプーラーを無効に設定した間隔で**アイドル**を呼び出しません代わりに、真のアイドル時間中にのみ呼び出されます。 したがって、プロバイダーは必要があります、 **Idle**メソッドが呼び出される頻度について何らかの仮定では動作しません。 アイドル時の操作をサポートするプロバイダーを指定の構成のユーザー インターフェイスの [プロバイダー] プロパティ シートでは、します。 
  
トランスポート プロバイダーへのログオンが成功すると、プロバイダーする必要がありますポインターを返す_lppXPLogon_パラメーターでログオン オブジェクトにします。 MAPI スプーラーはその他のプロバイダーのアクセスをこのオブジェクトを使用します。 **TransportLogon**は、ログオン ダイアログ ボックスを表示し、ユーザー ログオン通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックすると、プロバイダーは MAPI_E_USER_CANCEL を返す必要があります。 
  
**TransportLogon**から返されるエラー値のほとんどを MAPI には、プロバイダーが所属するメッセージ サービスが無効になります。 MAPI 呼び出しの MAPI セッションの残りの部分には、そのサービスに属するすべてのプロバイダーは使用されません。 対照的に、そのログオンから**TransportLogon**が MAPI_E_FAILONEPROVIDER のエラー値を返すと、MAPI は無効メッセージ サービス プロバイダーが所属します。 セッションの残りの部分のサービスを無効にすることを保証しないというエラーが発生した場合、 **TransportLogon**は MAPI_E_FAILONEPROVIDER を返す必要があります。 
  
プロバイダーは、そのログオンから MAPI_E_UNCONFIGURED を返します、MAPI は、プロバイダーのメッセージ サービスのエントリ関数を呼び出し、ログオンを再試行してください。 MAPI では、サービス自体を設定する機会を提供するのには、コンテキストとして MSG_SERVICE_CONFIGURE を渡します。 ログオン時にユーザー インターフェイスを許可するクライアントを選択すると、構成情報を入力できるように、サービスは、[設定] プロパティ シートを表示できます。 
  
プロバイダーが検出された場合に必要な情報が、プロファイルに含まれないすべて、MAPI プロバイダーのメッセージ サービスのエントリ ポイント関数を呼び出すように、MAPI_E_UNCONFIGURED を返す必要があります。 
  
## <a name="see-also"></a>関連項目

- [IXPProvider: IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

