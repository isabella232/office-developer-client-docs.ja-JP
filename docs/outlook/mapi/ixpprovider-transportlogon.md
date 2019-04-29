---
title: ixpprovidertransportlogon
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 53b2733dbf38d680027dc00ecf5513f384e46660
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417309"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションがトランスポートプロバイダーにログオンするセッションを確立します。 
  
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

_lpMAPISup_: [in] このセッションの MAPI 内のコールバック関数に対するトランスポートプロバイダーのサポートオブジェクトへのポインター。 このオブジェクトは、トランスポートプロバイダーによって解放されるまで有効です。
    
_uluiparam_: [in] このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドルです。 _uluiparam_パラメーターには、LOGON_SETUP フラグが_l flags_パラメーターで設定されている場合など、null 以外の値を指定できます。 
    
_lpszprofilename_: [in] ユーザーのプロファイル名へのポインター。 _lpszprofilename_パラメーターは、ダイアログボックスを表示する必要があるときに主に使用されます。 
    
_lpulflags_: ログオンセッションの確立方法を制御するフラグのビットマスクです。 次のフラグは、MAPI スプーラーによる入力に対して設定できます。
    
  - LOGON_NO_CONNECT: ユーザーアカウントは、メッセージの送信と受信以外の目的でこのトランスポートプロバイダーにログオンしています。 トランスポートプロバイダーは、他のメッセージングシステムへの接続を試みることはできません。
        
  - LOGON_NO_DIALOG: 現在保存されているユーザーの資格情報が無効であるか、ログオンに必要な資格情報が不足している場合でも、ダイアログボックスを表示しません。
        
  - LOGON_NO_INBOUND: トランスポートプロバイダーは、メッセージの受信を初期化する必要がなく、受信メッセージを受け付けないようにする必要があります。 MAPI スプーラーは、後で[IXPLogon:: transportnotify](ixplogon-transportnotify.md)メソッドを使用して、トランスポートプロバイダーに通知し、受信メッセージ処理を有効にすることができます。 
        
  - LOGON_NO_OUTBOUND: MAPI スプーラーでは何も提供されていないため、トランスポートプロバイダーはメッセージを送信するために初期化する必要はありません。 クライアントアプリケーションで、 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッド呼び出しを行うことができるように、メッセージの構成時にリモートプロバイダーへの接続が必要な場合は、トランスポートプロバイダーが接続を確立する必要があります。 MAPI スプーラーは、送信操作を開始できるときにトランスポートプロバイダーに通知するために、 **transportnotify**を使用できます。 
      
  - MAPI_UNICODE: プロファイル名の渡された文字列は、UNICODE 形式です。 MAPI\_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
      
    次のフラグは、トランスポートプロバイダーによって出力されるように設定できます。
      
  - LOGON_SP_IDLE: MAPI スプーラーが、アイドル時間処理のためにトランスポートプロバイダーの[IXPLogon:: idle](ixplogon-idle.md)メソッドを頻繁に呼び出すように要求します。 
      
  - LOGON_SP_POLL: MAPI スプーラーが、返された logon オブジェクトの[IXPLogon::P oll](ixplogon-poll.md)メソッドを頻繁に呼び出して、新しいメッセージをチェックするように要求します。 このフラグが設定されていない場合、MAPI スプーラーは、トランスポートプロバイダーが[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドを使用して、処理する新しいメッセージがあることをスプーラーに通知する場合にのみ、新しいメッセージをチェックします。 トランスポートプロバイダーは、このフラグを設定していない、またはメッセージ受信の MAPI スプーラーに通知しないことで、実際に送信のみになります。 
      
  - LOGON_SP_RESOLVE: MAPI スプーラーが完全に解決する要求このトランスポートプロバイダーによってサポートされていない受信者のすべてのメッセージアドレス。 そのため、トランスポートプロバイダーは、すべての受信者に対する応答パスを作成できます。
      
  - MAPI_UNICODE: [MAPIERROR](mapierror.md)構造体に返される文字列 (存在する場合) は、UNICODE 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
_lppMAPIError_: [out] 返される**MAPIERROR**構造体へのポインターへのポインター (存在する場合)。これには、そのエラーに関するバージョン、コンポーネント、およびコンテキスト情報が含まれています。 返す**MAPIERROR**構造体がない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
_lppXPLogon_: [out] 返されたトランスポートプロバイダログオンオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK: 呼び出しが成功し、必要な値が返されました。
    
MAPI_E_FAILONEPROVIDER: このプロバイダーはログオンできませんが、このエラーによってサービスが無効にならないようにしてください。 
    
MAPI_E_UNCONFIGURED: プロファイルには、ログオンが完了するのに十分な情報が含まれていません。 MAPI は、プロバイダーのメッセージサービスのエントリポイント関数を呼び出します。
    
MAPI_E_UNKNOWN_CPID: プロバイダーはクライアントのコードページをサポートしていません。
    
MAPI_E_UNKNOWN_LCID: プロバイダーはクライアントのロケール情報をサポートできません。
    
MAPI_E_USER_CANCEL: ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーは**ixpprovider:: transportlogon**メソッドを呼び出して、ユーザーのログオンセッションを確立します。 
  
ほとんどのトランスポートプロバイダーでは、ユーザー id 情報、サーバーアドレス、および資格情報を保存および取得するために、 _lpMAPISup_パラメーターで指定された support オブジェクトで提供される[imapisupport:: openprofilesection](imapisupport-openprofilesection.md)メソッドを使用します。 **openプロファイル**を使用することで、トランスポートプロバイダーは任意の情報を保存して、それを特定のリソースにログオンと関連付けることができます。 たとえば、プロバイダーは**openプロファイル**を使用して、特定のセッションに関連付けられているアカウント名とパスワード、およびそのセッションのリソースにアクセスするために必要なその他の必要な情報を保存することができます。 MAPI は、外部アクセスから、リソースに関連付けられている情報を非表示にします。 _lpMAPISup_で使用できるプロファイルセクションは、MAPI スプーラーによって管理されるため、このユーザーコンテキストに関連するデータは他のコンテキストのデータから分離されます。 
  
トランスポートプロバイダーは、サポートオブジェクトに対して**IUnknown:: AddRef**メソッドを呼び出し、プロバイダーのログオンオブジェクトの一部としてこのオブジェクトへのポインターのコピーを保持する必要があります。 
  
_lpszprofilename_のプロファイル表示名は、トランスポートプロバイダーがエラーメッセージまたはログオンダイアログボックスで使用できるように提供されています。 プロバイダーがこの名前を保持している場合は、プロバイダーによって割り当てられたストレージにコピーする必要があります。 
  
他のサービスプロバイダーと密に結合されているトランスポートプロバイダーは、コンパニオンプロバイダー間の操作に必要な資格情報を確立するために、ログオン時に追加の作業を行う必要がある場合があります。
  
通常、トランスポートプロバイダーは、ユーザーが最初にプロファイルにログオンしたときに開かれます。 通常、プロファイルへの最初のログオンは、メッセージストアにログオンする前に送信されるため、MAPI スプーラーは通常、 _lpulflags_に設定されている LOGON_NO_INBOUND と LOGON_NO_OUTBOUND の両方のフラグを使用して**transportlogon**を呼び出します。 後で、適切なメッセージストアがプロファイルセッションで利用可能になると、MAPI スプーラーはトランスポートプロバイダーの着信および発信操作を開始するために、 **transportnotify**を呼び出します。 
  
LOGON_NO_CONNECT フラグを lな_フラグ_で渡すと、トランスポートプロバイダーのオフライン操作を通知します。 このフラグは、外部接続を行わないことを示します。トランスポートプロバイダーが外部接続のないセッションを確立できない場合は、ログオンに対してエラー値が返されます。 
  
トランスポートプロバイダーは、システムがアイドル状態に__ なっている時間を使用するように設計されている場合は、初期化時に lLOGON_SP_IDLE フラグの先頭にフラグを設定する必要があります。 このような時間は、自動メッセージダウンロード、定刻メッセージのダウンロード、定刻メッセージ送信などの自動操作を処理するためによく使用されます。 このフラグが設定されている場合、MAPI スプーラーは、システムのアイドル時間が発生してこのような操作を開始すると、**アイドル状態**になります。 MAPI スプーラーは、設定された間隔で**アイドル状態**を呼び出しません。その代わりに、実際のアイドル時間中にのみ呼び出されます。 そのため、プロバイダーは、**アイドル状態**のメソッドが呼び出される頻度に関する前提条件に対応していません。 アイドル時間の操作をサポートするプロバイダーは、プロバイダーのプロパティシートで、そのための構成ユーザーインターフェイスを提供する必要があります。 
  
トランスポートプロバイダーのログオンが成功した場合、プロバイダーはログオンオブジェクトへのポインターを_lppXPLogon_パラメーターに返します。 MAPI スプーラーは、追加のプロバイダーアクセスにこのオブジェクトを使用します。 **transportlogon**がログオンダイアログボックスを表示し、ユーザーがログオンをキャンセルした場合、通常、ダイアログボックスの **[キャンセル**] ボタンをクリックすると、プロバイダーは MAPI_E_USER_CANCEL を返します。 
  
**transportlogon**から返されるエラー値のほとんどに対して、MAPI はプロバイダーが属しているメッセージサービスを無効にします。 mapi は、そのサービスに属しているプロバイダーを mapi セッションの残りの部分に対して呼び出しません。 一方、 **transportlogon**がログオンから MAPI_E_FAILONEPROVIDER エラー値を返す場合、MAPI はプロバイダーが属しているメッセージサービスを無効にしません。 セッションの残りの部分でサービスを無効にすることを保証しないエラーが発生した場合、 **transportlogon**は MAPI_E_FAILONEPROVIDER を返す必要があります。 
  
プロバイダーがログオンから MAPI_E_UNCONFIGURED を返した場合、MAPI はプロバイダーのメッセージサービスのエントリ関数を呼び出して、ログオンを再試行します。 MAPI は MSG_SERVICE_CONFIGURE をコンテキストとして渡して、サービスにそれ自体を構成する機会を与えます。 クライアントがログオンのユーザーインターフェイスを許可することを選択した場合、サービスはその構成プロパティシートを表示して、ユーザーが構成情報を入力できるようにすることができます。 
  
必要なすべての情報がプロファイルに含まれていないことがプロバイダーによって検出された場合、MAPI がプロバイダーのメッセージサービスのエントリポイント関数を呼び出すように、MAPI_E_UNCONFIGURED を返します。 
  
## <a name="see-also"></a>関連項目

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

