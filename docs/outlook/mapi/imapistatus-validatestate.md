---
title: imapistatusvalidatestate
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
  
MAPI リソースまたはサービスプロバイダーに対して使用可能な外部状態情報を確認します。 このメソッドは、すべての status オブジェクトでサポートされています。 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

_uluiparam_
  
> 順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。
    
_ulFlags_
  
> 順番検証を制御するフラグのビットマスク。 次のフラグを設定できます。
    
ABORT_XP_HEADER_OPERATION
  
> ユーザーが操作をキャンセルしました。通常は、対応するダイアログボックスの **[キャンセル**] ボタンをクリックします。 status オブジェクトには、次の2つのオプションがあります。 
    
   - 操作を続行します。
    
   - 操作を停止し、MAPI_E_USER_CANCELED を返します。
    
CONFIG_CHANGED 
  
> 1つ以上の状態オブジェクトの構成プロパティが変更されました。 クライアントはこのフラグを設定して、MAPI スプーラーが重要なトランスポートプロバイダーのエラーを動的に修正できるようにすることができます。 
    
FORCE_XP_CONNECT 
  
> status オブジェクトは、接続を実行する必要があります。 このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグと共に使用すると、接続はキャッシュなしで行われます。
    
FORCE_XP_DISCONNECT 
  
> status オブジェクトは、切断操作を実行する必要があります。 このフラグが REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグと共に使用されている場合、切断はキャッシュなしで行われます。
    
PROCESS_XP_HEADER_CACHE 
  
> ヘッダーキャッシュテーブル内のエントリを処理する必要があり、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたすべてのメッセージをダウンロードして、MSGSTATUS_REMOTE_DELETE フラグでマークされたすべてのメッセージを削除する必要があります。 MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE の両方が設定されたメッセージは移動する必要があります。
    
REFRESH_XP_HEADER_CACHE 
  
> リモートトランスポートプロバイダーの場合は、メッセージヘッダーの新しいリストがダウンロードされ、メッセージの状態をマークするすべてのフラグがクリアされる必要があります。
    
SUPPRESS_UI 
  
> status オブジェクトが操作の一部としてユーザーインターフェイスを表示できないようにします。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検証に成功しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中です。この操作を開始する前に、これを完了させるか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> status オブジェクトは、 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティの STATUS_VALIDATE_STATE フラグが指定されていない場合に、検証方法をサポートしていません。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが検証操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 この値は、リモートトランスポートプロバイダーによってのみ返されます。 
    
## <a name="remarks"></a>注釈

**imapistatus:: validatestate**メソッドは、status オブジェクトに関連付けられているリソースの状態をチェックします。 **validatestate**は、すべての状態オブジェクトに必要な[imapistatus](imapistatusimapiprop.md)インターフェイスの唯一のメソッドです。 このメソッドの正確な動作は、実装によって異なります。 次の表では、さまざまな種類の状態オブジェクトの実装について説明します。 
  
|**Status オブジェクト**|validatestate * * 実装 * *|
|:-----|:-----|
|MAPI サブシステム  <br/> |現在アクティブなサービスプロバイダとサブシステム自体が所有しているすべてのリソースの状態を検証します。  <br/> |
|MAPI スプーラー  <br/> |既にログオンしているかどうかにかかわらず、すべてのトランスポートプロバイダーのログオンを実行します。  <br/> |
|MAPI アドレス帳  <br/> |[プロファイル] セクションのエントリを確認します。  <br/> |
|サービスプロバイダー  <br/> |実装は、プロバイダーの種類と_ulflags_パラメーターで設定されたフラグによって異なります。  <br/> |
   
## <a name="notes-to-implementers"></a>実装に関するメモ

リモートクライアントアプリケーションは、 **validatestate**メソッドを呼び出して、さまざまなアクションのリモート処理を開始します。 このメソッドは、主に、実際に作業を行うのではなく、MAPI スプーラーと通信するようにステータスビットを設定することによって発生します。 通常、トランスポートプロバイダーは、MAPI スプーラーに対して、クライアントの要求を完了するために開始する必要のあるアクションを示す状態行にフラグを設定します。 

このクライアントトランスポートスプーラー相互作用モデルでは、クライアントによって要求されたアクションは、要求された操作が完了する前にその**validatestate**が戻ることによって返されます。 ただし、基になるメッセージングシステムを必要としないアクションや、トランスポート固有のインターフェイスを必要とするアクションは、同期することができます。 クライアントアプリケーションは、リモートトランスポートプロバイダーが実行するアクションを指定するために、次のフラグのビットマスクを渡します。 
  
ABORT_XP_HEADER_OPERATION 
  
> 可能であれば、リモートトランスポートプロバイダーは、ヘッダーのダウンロードに関連する操作をすべて取り消す必要があります。 これを行うには、トランスポートプロバイダーは、ログオンオブジェクトの状態の行に次のプロパティ値を設定する必要があります。
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの STATUS_INBOUND_ENABLED および STATUS_INBOUND_ACTIVE ビットをクリアして、このトランスポートプロバイダーの着信フラッシュプロセスを停止するように MAPI スプーラーに通知します。
    
   - **PR_STATUS_CODE**プロパティの STATUS_OFFLINE ビットを設定します。 
    
   - **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) プロパティを TRUE に設定します。
    
   - **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) プロパティを、トランスポートプロバイダーのユーザーに対する状態を示す文字列に設定します。
    
   - S_OK ��Ԃ��܂��B ただし、処理中の操作を取り消すことができない場合、 **validatestate**は MAPI_E_BUSY を返す必要があります。 
    
FORCE_XP_CONNECT 
  
> リモートトランスポートプロバイダーは、 [IXPLogon:: flushqueues](ixplogon-flushqueues.md)メソッドに含まれる MAPI スプーラートランスポート相互作用のコンテキストの外部にある共有リソース (モデム、COM ポートなど) への接続を確立することはできません。 このフラグを使用して**validatestate**を呼び出す場合、トランスポートプロバイダーは次の操作を実行する必要があります。 
    
   - **IXPLogon:: flushqueues**メソッドが呼び出されたときにリモート接続を確立する必要があることを示す内部状態フラグを設定します。 
    
   - 状態テーブルの正しい値を設定して、MAPI スプーラーがキューのフラッシュプロセスを開始するようにします。
    
   - キューのフラッシュが完了したら、共有リソースを解放します。
    
   - **PR_STATUS_CODE**プロパティの STATUS_OFFLINE ビットをオフにします。 
    
   - S_OK ��Ԃ��܂��B
    
FORCE_XP_DISCONNECT 
  
> リモートトランスポートプロバイダーは、メッセージングシステムのリソースへの接続を解放する必要があります。 この操作を行った後、 **PR_STATUS_CODE**プロパティの STATUS_OFFLINE ビットを設定し、S_OK を返す必要があります。 
    
PROCESS_XP_HEADER_CACHE 
  
> リモートトランスポートプロバイダーは、リモートメッセージを処理し、延期されたメッセージをすべてアップロードする必要があります。 これを行うには、トランスポートプロバイダーは、ログオンオブジェクトの状態の行に次のプロパティ値を設定する必要があります。
    
   - **PR_STATUS_STRING**プロパティを、トランスポートプロバイダーのユーザーに対する状態を示す文字列に設定します。 
    
   - **PR_STATUS_CODE**プロパティに STATUS_OUTBOUND_ENABLED および STATUS_OUTBOUND_ACTIVE ビットを設定します。 
    
   - トランスポートプロバイダーの状態行の**PR_REMOTE_VALIDATE_OK**プロパティを FALSE に設定します。 
    
   - **validatestate**が呼び出されたときに別の操作 (ヘッダーのダウンロードなど) が進行中の場合、 **validatestate**は MAPI_E_BUSY を返します。 
    
   - REFRESH_XP_HEADER_CACHE フラグを処理するコードを実行して、Microsoft Exchange クライアントの要件を満たすようにします。
    
REFRESH_XP_HEADER_CACHE 
  
> リモートトランスポートプロバイダーは、メッセージングシステムからすべての新しいメッセージヘッダーを取得する必要があります。 これを行うには、トランスポートプロバイダーは次のことを行う必要があります。
    
   - **PR_STATUS_STRING**プロパティを、トランスポートプロバイダーのユーザーに対する状態を示す文字列に設定します。 
    
   - **PR_STATUS_CODE**プロパティに STATUS_INBOUND_ENABLED および STATUS_INBOUND_ACTIVE ビットを設定します。 
    
   - **PR_STATUS_CODE**プロパティの STATUS_OFFLINE ビットをオフにします。 
    
   - **PR_STATUS_CODE**プロパティの STATUS_ONLINE ビットを設定します。 
    
   - トランスポートプロバイダーの状態行の**PR_REMOTE_VALIDATE_OK**プロパティを FALSE に設定します。 
    
SHOW_XP_SESSION_UI 
  
> メッセージヘッダー (メッセージのダウンロードを確認するダイアログボックスなど) を処理するためのユーザーインターフェイスがトランスポートプロバイダーにある場合は、そのダイアログボックスが表示されます。 それ以外の場合、 **validatestate**は MAPI_E_NO_SUPPORT を返すことができます。 
    
これら以外のフラグが渡された場合、 **validatestate**は MAPI_E_UNKNOWN_FLAGS を返さなければなりません。 
  
多くの場合、トランスポートプロバイダーに対するクライアントの呼び出しは、 **imapistatus:: validatestate**メソッドになります。 **validatestate**の処理中は、トランスポートプロバイダーは、モデムや COM ポートなどの不足しているシステムリソースを割り当てるアクションを実行してはなりません。 これは、MAPI スプーラーが複数のトランスポートプロバイダーのキューをフラッシュする必要がある場合があるためです。 ただし、クライアントは任意のトランスポートプロバイダーの**validatestate**メソッドをいつでも呼び出すことができます。 トランスポートプロバイダーが、 **validatestate**の処理中に希少でないリソースを割り当てようとした場合、MAPI スプーラーがキューをフラッシュするように指示した別のトランスポートプロバイダーとの競合が原因で、エラーが発生する可能性があります。 すべての希少なリソース割り当てを MAPI スプーラーの方向で実行できるようにする場合は、このような競合を避けることができます。 トランスポートプロバイダーは**PR_REMOTE_VALIDATE_OK**プロパティをサポートしている必要があります。これにより、クライアントアプリケーションは、トランスポートプロバイダーがビジー状態になったとき、または MAPI スプーラーがアクションを開始するのを待っていることを検出できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

このメソッドを使用すると、その他の長い呼び出しが発生する可能性があるため、 **validatestate**は MAPI_E_BUSY を返して、このメソッドが別の操作の完了を待機していることを通知します。 別のタスクを試行する前に、保留中の操作が完了するまで待機する必要があります。 
  
トランスポートプロバイダーの状態オブジェクトに対する呼び出しを最も細かく制御できます。 1つ以上のフラグを**validatestate**に渡して、トランスポートプロバイダーの操作に影響を与えることができます。 たとえば、ABORT_XP_HEADER_OPERATION フラグは、ユーザーが入力規則を取り消したことを示します。 トランスポートプロバイダーは、中止、MAPI_E_USER_CANCELED を返す、または続行することを決定できます。 
  
CONFIG_CHANGED フラグは、サービスプロバイダーまたは MAPI スプーラーの状態オブジェクトへの呼び出しに設定して、構成オプションが変更されたことを示すことができます。 CONFIG_CHANGED を使用して、トランスポートプロバイダーを動的に再構成することができます。 サービスプロバイダーの status オブジェクトへの呼び出しで CONFIG_CHANGED を設定すると、プロバイダーは[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)を呼び出して応答し、変更の MAPI スプーラーに通知します。 MAPI スプーラーの状態オブジェクトへの呼び出しで CONFIG_CHANGED を設定すると、スプーラーは各アクティブトランスポートプロバイダーに対して[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)を呼び出します。 **AddressTypes**は、トランスポートのサポートされているアドレスの種類の MAPI スプーラーに通知します。 一部のサービスプロバイダーでは、検証に長い時間がかかることが予想される場合にも、進行状況のインジケーターが表示されます。 進行状況インジケーターを表示することは便利ですが、必須ではありません。 
  
SUPPRESS_UI フラグが設定されている場合は、構成プロパティのシートまたは進行状況のダイアログボックスを表示できません。 
  
## <a name="see-also"></a>関連項目

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [PidTagRemoteValidateOk 標準プロパティ](pidtagremotevalidateok-canonical-property.md)
- [PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
- [PidTagStatusCode 標準プロパティ](pidtagstatuscode-canonical-property.md)
- [PidTagStatusString 標準プロパティ](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

