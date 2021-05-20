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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438149"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI リソースまたはサービス プロバイダーで使用可能な外部状態情報を確認します。 このメソッドは、すべての状態オブジェクトでサポートされています。 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

_ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。
    
_ulFlags_
  
> [in]検証を制御するフラグのビットマスク。 次のフラグを設定できます。
    
ABORT_XP_HEADER_OPERATION
  
> ユーザーは、通常、対応するダイアログ ボックスの [ **キャンセル** ] ボタンをクリックして、操作をキャンセルしました。 status オブジェクトには、次の 2 つのオプションがあります。 
    
   - 操作の作業を続行します。
    
   - 操作を停止し、操作をMAPI_E_USER_CANCELED。
    
CONFIG_CHANGED 
  
> 1 つ以上の状態オブジェクトの構成プロパティが変更されました。 クライアントは、MAPI スプーラーが重大なトランスポート プロバイダーのエラーを動的に修正できるよう、このフラグを設定できます。 
    
FORCE_XP_CONNECT 
  
> status オブジェクトは接続を実行する必要があります。 このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHEと一緒に使用すると、接続はキャッシュなしで行われます。
    
FORCE_XP_DISCONNECT 
  
> status オブジェクトは切断操作を実行する必要があります。 このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHEと一緒に使用すると、切断はキャッシュなしで行われます。
    
PROCESS_XP_HEADER_CACHE 
  
> ヘッダー キャッシュ テーブル内のエントリを処理し、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたメッセージはすべてダウンロードし、MSGSTATUS_REMOTE_DELETE フラグでマークされたメッセージはすべて削除する必要があります。 設定されたメッセージとMSGSTATUS_REMOTE_DOWNLOAD設定MSGSTATUS_REMOTE_DELETEメッセージを移動する必要があります。
    
REFRESH_XP_HEADER_CACHE 
  
> リモート トランスポート プロバイダーの場合は、メッセージ ヘッダーの新しい一覧をダウンロードし、メッセージの状態を示すフラグはすべてクリアする必要があります。
    
SUPPRESS_UI 
  
> status オブジェクトが操作の一部としてユーザー インターフェイスを表示しなかします。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検証が成功しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中です。この操作を開始する前に、完了を許可するか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> **status** オブジェクトは、PR_RESOURCE_METHODS ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_VALIDATE_STATE フラグがない場合に示される検証メソッドをサポートしません。
    
MAPI_E_USER_CANCEL 
  
> ユーザーは、通常、ダイアログ ボックスの [キャンセル]ボタンをクリックして、検証操作をキャンセルしました。 この値は、リモート トランスポート プロバイダーによってのみ返されます。 
    
## <a name="remarks"></a>注釈

**IMAPIStatus::ValidateState** メソッドは、状態オブジェクトに関連付けられているリソースの状態をチェックします。 **ValidateState** は、すべての状態オブジェクトに必要な [IMAPIStatus](imapistatusimapiprop.md) インターフェイス内の唯一のメソッドです。 このメソッドの正確な動作は、実装によって異なります。 次の表では、さまざまな種類の状態オブジェクトの実装について説明します。 
  
|**Status オブジェクト**|ValidateState** の実装**|
|:-----|:-----|
|MAPI サブシステム  <br/> |現在アクティブなサービス プロバイダーとサブシステム自体が所有しているすべてのリソースの状態を検証します。  <br/> |
|MAPI スプーラー  <br/> |既にログオンしているかどうかに関係なく、すべてのトランスポート プロバイダーのログオンを実行します。  <br/> |
|MAPI アドレス帳  <br/> |プロファイル セクションのエントリを確認します。  <br/> |
|サービス プロバイダー  <br/> |実装は、プロバイダーの種類と  _ulFlags パラメーターで設定されたフラグによって異_ なります。  <br/> |
   
## <a name="notes-to-implementers"></a>実装に関するメモ

リモート クライアント アプリケーションは ValidateState メソッドを **呼び出** して、さまざまなアクションのリモート処理を開始します。 このメソッドは主に、MAPI スプーラーと通信するための状態ビットを設定するために存在します。実際に作業を行う代わりに。 通常、トランスポート プロバイダーは、クライアントの要求を完了するために開始する必要があるアクションを MAPI スプーラーに示すフラグを状態行に設定します。 

このクライアント トランスポート スプーラー操作のモデルでは、要求されたアクションが完了する前に **ValidateState** が返されるという、クライアントによって要求されたアクションは非同期です。 ただし、基になるメッセージング システムを必ずしも必要としないアクション、またはトランスポート固有のインターフェイスを含むアクションは同期可能です。 クライアント アプリケーションは、次のフラグのビットマスクを渡して、リモート トランスポート プロバイダーが実行するアクションを指定します。 
  
ABORT_XP_HEADER_OPERATION 
  
> 可能であれば、リモート トランスポート プロバイダーは、ヘッダーのダウンロードに関連する操作を取り消す必要があります。 これを行うには、トランスポート プロバイダーはログオン オブジェクトの状態行に次のプロパティ値を設定する必要があります。
    
   - PR_STATUS_CODE ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの **STATUS_INBOUND_ENABLED** ビットと STATUS_INBOUND_ACTIVE ビットをクリアして、このトランスポート プロバイダーの受信フラッシュ プロセスを停止する MAPI スプーラーに通知します。
    
   - プロパティでSTATUS_OFFLINEビットを **PR_STATUS_CODE** します。 
    
   - [プロパティ] **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) プロパティを TRUE に設定します。
    
   - ユーザーに **PR_STATUS_STRING** を示す文字列にプロパティ [(PidTagStatusString)](pidtagstatusstring-canonical-property.md)プロパティを設定します。
    
   - S_OK ��Ԃ��܂��B ただし、進行中の操作を取り消しできない場合は **、ValidateState** はデータをMAPI_E_BUSY。 
    
FORCE_XP_CONNECT 
  
> リモート トランスポート プロバイダーは [、IXPLogon::FlushQueues](ixplogon-flushqueues.md) メソッドに関係する MAPI スプーラー トランスポートの相互作用のコンテキスト外で共有リソース (モデムや COM ポートなど) への接続を確立しなけれ。 ValidateState **をこの** フラグで呼び出す場合、トランスポート プロバイダーは次の操作を行う必要があります。 
    
   - **IXPLogon::FlushQueues** メソッドの呼び出し時にリモート接続を確立する必要がある場合は、内部状態フラグを設定します。 
    
   - MAPI スプーラーがキューのフラッシュ プロセスを開始する状態テーブルの正しい値を設定します。
    
   - キューのフラッシュが完了したら、共有リソースを解放します。
    
   - プロパティのSTATUS_OFFLINEビットを **PR_STATUS_CODE** します。 
    
   - S_OK ��Ԃ��܂��B
    
FORCE_XP_DISCONNECT 
  
> リモート トランスポート プロバイダーは、メッセージング システム リソースへの接続を解放する必要があります。 これを行った後、STATUS_OFFLINE プロパティで STATUS_OFFLINE ビットを設定し、PR_STATUS_CODEを返S_OK。 
    
PROCESS_XP_HEADER_CACHE 
  
> リモート トランスポート プロバイダーは、リモート メッセージを処理し、延期されたメッセージをアップロードする必要があります。 これを行うには、トランスポート プロバイダーはログオン オブジェクトの状態行に次のプロパティ値を設定する必要があります。
    
   - トランスポート プロバイダー **PR_STATUS_STRING** をユーザーに示す文字列に、PR_STATUS_STRING プロパティを設定します。 
    
   - プロパティでSTATUS_OUTBOUND_ENABLEDビットSTATUS_OUTBOUND_ACTIVEビットを **PR_STATUS_CODE** します。 
    
   - トランスポート プロバイダー **のPR_REMOTE_VALIDATE_OK** のプロパティを FALSE に設定します。 
    
   - **ValidateState** が呼び出された場合に別の操作 (ヘッダーのダウンロードなど) が進行中の場合は **、ValidateState** はヘッダーを返MAPI_E_BUSY。 
    
   - Microsoft クライアントの要件を満たすために、REFRESH_XP_HEADER_CACHE フラグを処理するコードExchangeします。
    
REFRESH_XP_HEADER_CACHE 
  
> リモート トランスポート プロバイダーは、メッセージング システムから新しいメッセージ ヘッダーを取得する必要があります。 これを行うには、トランスポート プロバイダーは次の操作を行う必要があります。
    
   - トランスポート プロバイダー **PR_STATUS_STRING** をユーザーに示す文字列に、PR_STATUS_STRING プロパティを設定します。 
    
   - プロパティでSTATUS_INBOUND_ENABLEDビットSTATUS_INBOUND_ACTIVEビットを **設定** PR_STATUS_CODEします。 
    
   - プロパティのSTATUS_OFFLINEビットを **PR_STATUS_CODE** します。 
    
   - プロパティでSTATUS_ONLINEビットを **PR_STATUS_CODE** します。 
    
   - トランスポート プロバイダー **のPR_REMOTE_VALIDATE_OK** のプロパティを FALSE に設定します。 
    
SHOW_XP_SESSION_UI 
  
> トランスポート プロバイダーにメッセージ ヘッダーを処理するためのユーザー インターフェイス (メッセージのダウンロードを確認するダイアログ ボックスなど) がある場合は、そのダイアログ ボックスが表示されます。 それ以外の場合 **、ValidateState** は、MAPI_E_NO_SUPPORT。 
    
これらのフラグ以外のフラグが渡された場合は **、ValidateState** は値を返MAPI_E_UNKNOWN_FLAGS。 
  
トランスポート プロバイダーへのクライアントの呼び出しは、多くの場合 **、IMAPIStatus::ValidateState メソッドに対して行** います。 **ValidateState** の処理中に、トランスポート プロバイダーは、モデムや COM ポートなど、不足しているシステム リソースを割り当てるアクションを実行しなけい。 これは、MAPI スプーラーが複数のトランスポート プロバイダーでキューをフラッシュする必要がある場合があるためです。 ただし、クライアントは、任意のトランスポート プロバイダーの **ValidateState** メソッドをいつでも呼び出できます。 **ValidateState** の処理中にトランスポート プロバイダーが不足しているリソースを割り当てしようとすると、MAPI スプーラーがキューをフラッシュするように指示した別のトランスポート プロバイダーとの競合が原因でエラーが発生する可能性があります。 MAPI スプーラーの指示に従って、すべての不足しているリソース割り当てを許可する場合は、このような競合を回避できます。 トランスポート プロバイダーは、トランスポート **プロバイダーがビジー状態または** MAPI スプーラーがアクションを開始するのを待っているときにクライアント アプリケーションが検出できるよう、PR_REMOTE_VALIDATE_OK プロパティをサポートする必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

このメソッドは、他の潜在的に長い呼び出しを行う原因となる可能性があるため **、ValidateState** は MAPI_E_BUSY を返して、このメソッドが別の操作の完了を待機しているという通知を受け取る場合があります。 別のタスクを試みる前に、保留中の操作が完了するまで待つ必要があります。 
  
トランスポート プロバイダーの状態オブジェクトへの呼び出しを最も制御できます。 1 つ以上のフラグを **ValidateState** に渡して、トランスポート プロバイダーの操作に影響を与えます。 たとえば、ABORT_XP_HEADER_OPERATIONフラグは、ユーザーが検証を取り消したと示します。 トランスポート プロバイダーは、中止、返す、または続行MAPI_E_USER_CANCELED決定できます。 
  
呼び出しの CONFIG_CHANGEDフラグをサービス プロバイダーの status オブジェクトまたは MAPI スプーラーに設定して、構成オプションが変更されたかどうかを示します。 トランスポート プロバイダーを動的CONFIG_CHANGED再構成するには、次の情報を使用します。 サービス プロバイダーの状態オブジェクトへの呼び出しで CONFIG_CHANGED を設定すると、プロバイダーは [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) への呼び出しで応答し、MAPI スプーラーに変更を通知します。 MAPI スプーラー CONFIG_CHANGED呼び出し時に、スプーラーはアクティブなトランスポート プロバイダーごとに [IXPLogon::AddressTypes](ixplogon-addresstypes.md) を呼び出します。 **AddressTypes は** 、トランスポートでサポートされているアドレスの種類を MAPI スプーラーに通知します。 一部のサービス プロバイダーは、検証に時間がかかると予想される場合は進行状況インジケーターも表示します。 進行状況インジケーターの表示は役に立ちますが、必須ではありません。 
  
このフラグSUPPRESS_UI設定すると、構成プロパティ シートや進行状況ダイアログ ボックスを表示できません。 
  
## <a name="see-also"></a>関連項目

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [PidTagRemoteValidateOk 標準プロパティ](pidtagremotevalidateok-canonical-property.md)
- [PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
- [PidTagStatusCode 標準プロパティ](pidtagstatuscode-canonical-property.md)
- [PidTagStatusString 標準プロパティ](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

