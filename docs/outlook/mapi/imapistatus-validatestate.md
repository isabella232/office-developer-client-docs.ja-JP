---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3ff29ac7e7f9b7876bb678930390ca556351ecf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800741"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**適用されます**: Outlook 
  
MAPI リソースまたはサービス プロバイダーの使用可能な外部のステータス情報を確認します。 ステータスのすべてのオブジェクトでこのメソッドがサポートされています。 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

_ulUIParam_
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。
    
_ulFlags_
  
> [in]検証を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
ABORT_XP_HEADER_OPERATION
  
> ユーザー操作がキャンセルされました、通常、対応するダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 状態オブジェクトには、2 つのオプションがあります。 
    
   - 工程の作業を続行します。
    
   - 操作を停止し、MAPI_E_USER_CANCELED を返します。
    
CONFIG_CHANGED 
  
> 1 つ以上の状態のオブジェクトの構成のプロパティを変更します。 クライアントは、動的に重要なトランスポート プロバイダーのエラーを修正するのには MAPI スプーラーを許可するには、このフラグを設定できます。 
    
FORCE_XP_CONNECT 
  
> 状態オブジェクトは、接続を実行します。 REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグを指定してこのフラグを使用する場合は、キャッシュを使用しない接続が発生します。
    
FORCE_XP_DISCONNECT 
  
> 状態オブジェクトは、切断操作を実行する必要があります。 REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグを指定してこのフラグを使用する場合は、キャッシュを使用しない切断が発生します。
    
PROCESS_XP_HEADER_CACHE 
  
> ヘッダー キャッシュ テーブル内のエントリを処理する必要があります、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたすべてのメッセージをダウンロードするか、および、MSGSTATUS_REMOTE_DELETE フラグでマークされたすべてのメッセージを削除する必要があります。 MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE の設定の両方を持つメッセージを移動する必要があります。
    
REFRESH_XP_HEADER_CACHE 
  
> リモート トランスポート プロバイダーでは、メッセージ ヘッダーの新しいリストをダウンロードする必要があり、メッセージの状態をマークするすべてのフラグをクリアする必要があります。
    
SUPPRESS_UI 
  
> 状態オブジェクトが操作の一部としてユーザー インターフェイスを表示するを防ぎます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 検証に成功しました。
    
MAPI_E_BUSY 
  
> 別の操作が実行中です。完了するために許可するか、停止する、この操作を開始する前に。
    
MAPI_E_NO_SUPPORT 
  
> 状態オブジェクトは、検証メソッドをサポートしていません**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティに STATUS_VALIDATE_STATE フラグがない場合で示される。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました検証、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 リモート トランスポート プロバイダーによってのみ、この値が返されます。 
    
## <a name="remarks"></a>備考

**IMAPIStatus::ValidateState**メソッドは、状態オブジェクトに関連付けられているリソースの状態をチェックします。 [IMAPIStatus](imapistatusimapiprop.md)インターフェイスの状態のすべてのオブジェクトに必要な唯一の方法は、 **ValidateState**です。 このメソッドの実際の動作は実装によって異なります。 次の表では、状態オブジェクトのさまざまな種類のそれぞれの実装について説明します。 
  
|**ステータス オブジェクト**|* ValidateState * 実装 * *|
|:-----|:-----|
|MAPI サブシステム  <br/> |現在アクティブなサービス ・ プロバイダー、サブシステム自身が所有しているすべてのリソースの状態を検証します。  <br/> |
|MAPI スプーラー  <br/> |ログオン用に既にログオンしているかどうかに関係なくすべてのトランスポート プロバイダーを実行します。  <br/> |
|MAPI アドレス帳  <br/> |プロファイル セクション内のエントリをチェックします。  <br/> |
|サービス プロバイダー  <br/> |実装は、プロバイダーと、 _ulFlags_パラメーターで設定されているフラグの種類によって異なります。  <br/> |
   
## <a name="notes-to-implementers"></a>実装者へのメモ

リモート クライアント アプリケーションは、リモートのさまざまなアクションの処理を開始する**ValidateState**メソッドを呼び出します。 このメソッドは、実際に作業を行うための代わりに、MAPI スプーラーと通信するためにステータス ビットを設定するのには、主に存在します。 通常、トランスポート プロバイダーは、MAPI スプーラーにクライアントの要求を完了するのには開始する必要があるアクションを示すステータス行のフラグを設定します。 

クライアント トランスポートがスプーラーの相互作用のこのモデルでは、クライアントによって要求された操作は、非同期で要求された操作が完了する前に、 **ValidateState**が返されます。 ただしが必ずしも含まれず、基になるメッセージング システムまたはトランスポートに固有のインターフェイスでは、関連するアクションは、同期があります。 リモート トランスポート プロバイダーが実行するアクションを指定するのには、次のフラグのビットマスクで、クライアント アプリケーションに渡されます。 
  
ABORT_XP_HEADER_OPERATION 
  
> 可能であれば、リモート トランスポート プロバイダーでは、ヘッダーのダウンロードに関連するすべての操作を取り消す必要があります。 これを行うには、トランスポート プロバイダーは、ログオン オブジェクトの [状態] 行に次のプロパティ値を設定する必要があります。
    
   - このトランスポート プロバイダーの受信のフラッシュ処理を停止するのには MAPI スプーラーに指示するのには**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) のプロパティで STATUS_INBOUND_ENABLED と STATUS_INBOUND_ACTIVE のビットをオフにします。
    
   - STATUS_OFFLINE の**PR_STATUS_CODE**プロパティ内のビットを設定します。 
    
   - **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) プロパティを TRUE に設定します。
    
   - ユーザーに、トランスポート プロバイダーの状態を示す文字列を**PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) のプロパティを設定します。
    
   - S_OK ��Ԃ��܂��B ただし、実行中の操作をキャンセルすることはできません、 **ValidateState**は MAPI_E_BUSY を返す必要があります。 
    
FORCE_XP_CONNECT 
  
> リモート トランスポート プロバイダーは、 [IXPLogon::FlushQueues](ixplogon-flushqueues.md)メソッドに関連する MAPI スプーラー トランスポートの操作のコンテキストの外部からの共有リソース (たとえば、モデムまたは COM ポート) への接続を確立する必要があることはありません。 **ValidateState**はこのフラグを使って呼び出されると、トランスポート プロバイダーが次の操作にする必要があります。 
    
   - **IXPLogon::FlushQueues**メソッドが呼び出されたときに、リモート接続を確立する必要があることを示す内部フラグを設定します。 
    
   - MAPI スプーラー キュー プロセスのフラッシュを開始するのには、状態テーブルに正しい値を設定します。
    
   - キューのフラッシュが完了すると、共有リソースを解放します。
    
   - STATUS_OFFLINE の**PR_STATUS_CODE**プロパティ内のビットをオフにします。 
    
   - S_OK ��Ԃ��܂��B
    
FORCE_XP_DISCONNECT 
  
> リモート トランスポート プロバイダーは、メッセージング システムのリソースへの接続を解放する必要があります。 その後で、 **PR_STATUS_CODE**プロパティに STATUS_OFFLINE ビットを設定する必要があります、S_OK を返します。 
    
PROCESS_XP_HEADER_CACHE 
  
> リモート トランスポート プロバイダーは、必要がありますリモートのメッセージを処理し、保留されているすべてのメッセージをアップロードします。 これを行うには、トランスポート プロバイダーは、ログオン オブジェクトの [状態] 行に次のプロパティ値を設定する必要があります。
    
   - ユーザーに、トランスポート プロバイダーの状態を示す文字列を**PR_STATUS_STRING**プロパティを設定します。 
    
   - [ **PR_STATUS_CODE** ] プロパティには、STATUS_OUTBOUND_ENABLED と STATUS_OUTBOUND_ACTIVE のビットを設定します。 
    
   - False を指定するトランスポート プロバイダーの状態の行の**PR_REMOTE_VALIDATE_OK**プロパティを設定します。 
    
   - (ヘッダーをダウンロードするには) などの進行中の別の操作の場合**ValidateState**が呼び出されると、 **ValidateState**は MAPI_E_BUSY を返す必要があります。 
    
   - Microsoft Exchange クライアントの要件を満たすために、同様に、REFRESH_XP_HEADER_CACHE フラグを処理するためのコードを実行します。
    
REFRESH_XP_HEADER_CACHE 
  
> リモート トランスポート プロバイダーは、メッセージング システムから新しいメッセージ ヘッダーを取得する必要があります。 これを行うには、トランスポート プロバイダーは次の操作を行う必要があります。
    
   - ユーザーに、トランスポート プロバイダーの状態を示す文字列を**PR_STATUS_STRING**プロパティを設定します。 
    
   - [ **PR_STATUS_CODE** ] プロパティには、STATUS_INBOUND_ENABLED と STATUS_INBOUND_ACTIVE のビットを設定します。 
    
   - STATUS_OFFLINE の**PR_STATUS_CODE**プロパティ内のビットをオフにします。 
    
   - STATUS_ONLINE の**PR_STATUS_CODE**プロパティ内のビットを設定します。 
    
   - False を指定するトランスポート プロバイダーの状態の行の**PR_REMOTE_VALIDATE_OK**プロパティを設定します。 
    
SHOW_XP_SESSION_UI 
  
> トランスポート プロバイダーは、メッセージのダウンロードを確認するダイアログ ボックス) など、メッセージのヘッダーを処理するためのユーザー インターフェイスの任意の部分には、そのダイアログ ボックスが表示されます。 それ以外の場合、 **ValidateState**は、MAPI_E_NO_SUPPORT を返すことができます。 
    
これら以外のすべてのフラグが渡されると、 **ValidateState**は MAPI_E_UNKNOWN_FLAGS を返す必要があります。 
  
トランスポート プロバイダーは、クライアントの呼び出しは、 **IMAPIStatus::ValidateState**メソッドになります。 **ValidateState**の処理中にトランスポート プロバイダーは、モデムまたは COM ポートなど、限られたシステム リソースの割り当てすべてのアクションを行わないでください。 これは、MAPI スプーラーは、トランスポート プロバイダーを 1 つ以上のキューをフラッシュする必要がありますので。 ただし、クライアントは、いつでも任意のトランスポート プロバイダーの**ValidateState**メソッドを呼び出すことができます。 トランスポート プロバイダーは、 **ValidateState**の処理中に貴重なリソースを割り当てるしようとする場合、エラーは発生する MAPI スプーラーのキューをフラッシュするように指示する別のトランスポート プロバイダーとの競合が発生したためです。 MAPI スプーラーの指示の下で発生するすべての貴重なリソースの割り当てを許可する場合は、このような競合を回避できます。 トランスポート プロバイダーは、クライアント アプリケーションは、トランスポート プロバイダーは、ビジー状態または待機操作を実行するのには、MAPI スプーラーを無効にするときを検出できるように**PR_REMOTE_VALIDATE_OK**プロパティをサポートする必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

なる可能性がある時間のかかる他の呼び出しはこのメソッドが原因で発生するため、 **ValidateState**は、このメソッドが別の操作が完了するの待っていることを通知するために MAPI_E_BUSY を返すことができます。 別のタスクを実行する前に保留中の操作が完了するまでを待機する必要があります。 
  
プロバイダーの状態のオブジェクトを転送するのには、呼び出しを細かく制御があります。 **ValidateState**トランスポート プロバイダーの操作に影響を与えるには、1 つまたは複数のフラグを渡すことができます。 たとえば、ABORT_XP_HEADER_OPERATION フラグは、ユーザーが検証をキャンセルすることを示します。 トランスポート プロバイダーは、MAPI_E_USER_CANCELED を返すことを中止するには決定できますか、続けることができます。 
  
構成オプションが変更されたことを示すためにサービス ・ プロバイダーの状態オブジェクト、または MAPI スプーラーへの呼び出しには、CONFIG_CHANGED フラグを設定できます。 トランスポート プロバイダーを動的に再構成するのに CONFIG_CHANGED を使用することができます。 サービス プロバイダーの状態のオブジェクトへの呼び出しに CONFIG_CHANGED を設定すると、プロバイダーは、MAPI スプーラーを無効に変更を通知する[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)への呼び出しに応答します。 MAPI スプーラーを無効の状態のオブジェクトへの呼び出しに CONFIG_CHANGED を設定すると、スプーラーは、アクティブなトランスポート プロバイダーごとに[IXPLogon::AddressTypes](ixplogon-addresstypes.md)を呼び出します。 **AddressTypes**は、トランスポートのサポートされているアドレスの種類の MAPI スプーラーに通知します。 サービス プロバイダーによっては、検証の時間がかかるが予想される場合にも、進行状況インジケーターを表示します。 進行状況のインジケーターを表示するが役に立つ、必須ではありません。 
  
SUPPRESS_UI フラグを設定すると、プロパティ シートの構成や進行状況ダイアログ ボックスを表示できます。 
  
## <a name="see-also"></a>関連項目

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [PidTagRemoteValidateOk の標準的なプロパティ](pidtagremotevalidateok-canonical-property.md)
- [PidTagResourceMethods の標準的なプロパティ](pidtagresourcemethods-canonical-property.md)
- [PidTagStatusCode の標準的なプロパティ](pidtagstatuscode-canonical-property.md)
- [PidTagStatusString の標準的なプロパティ](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)

