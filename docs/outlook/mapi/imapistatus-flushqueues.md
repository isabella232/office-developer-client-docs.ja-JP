---
title: imapistatusflushqueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328195"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信または受信を待機しているすべてのメッセージを直ちにアップロードまたはダウンロードすることを強制します。 トランスポートプロバイダーが実装する MAPI スプーラー状態オブジェクトと状態オブジェクトは、このメソッドをサポートしています。
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _cbtargettransport_
  
> 順番_lptargettransport_パラメーターで指定されたエントリ識別子のバイト数。 _cbtargettransport_パラメーターは、MAPI スプーラーの status オブジェクトへの呼び出しに対してのみ設定されます。 トランスポートプロバイダーの呼び出しの場合、 _cbtargettransport_パラメーターは0に設定されます。 
    
 _lptargettransport_
  
> 順番メッセージキューをフラッシュするトランスポートプロバイダーのエントリ識別子へのポインター。 _lptargettransport_パラメーターは、MAPI スプーラーの status オブジェクトへの呼び出しに対してのみ設定されます。 トランスポートプロバイダーの呼び出しの場合、 _lptargettransport_パラメーターは NULL に設定されます。 
    
 _ulFlags_
  
> 順番フラッシュ操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
FLUSH_ASYNC_OK 
  
> フラッシュ操作は非同期的に発生する可能性があります。 このフラグは、MAPI スプーラーの状態オブジェクトにのみ適用されます。 
    
FLUSH_DOWNLOAD 
  
> 受信メッセージキューをフラッシュする必要があります。
    
FLUSH_FORCE 
  
> フラッシュ操作は、パフォーマンスが低下する可能性があるにもかかわらず、発生します。 このフラグは、非同期トランスポートプロバイダーを対象とする場合に設定する必要があります。
    
FLUSH_NO_UI 
  
> status オブジェクトは、進行状況インジケーターを表示しません。
    
FLUSH_UPLOAD 
  
> 送信メッセージキューをフラッシュする必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フラッシュ操作が正常に終了しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中です。この操作を開始するには、これを完了させるか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> status オブジェクトの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_FLUSH_QUEUES フラグが設定されていない場合、status オブジェクトはこの操作をサポートしていません。
    
## <a name="remarks"></a>解説

**imapistatus:: flushqueues**メソッドは、MAPI スプーラーまたはトランスポートプロバイダーが、送信キュー内のすべてのメッセージを直ちに送信するか、または受信キューからすべてのメッセージを受信することを要求します。 **flushqueues**は、トランスポートプロバイダーが提供する MAPI スプーラー状態オブジェクトと状態オブジェクトによってのみ実装されます。 
  
クライアントが処理を続行できるように、非同期要求に対して MAPI_E_BUSY を返す必要があります。 
  
既定では、 **flushqueues**は同期操作です。コントロールは、フラッシュが完了するまで呼び出し元に戻りません。 MAPI スプーラーによって実行されるフラッシュ操作だけが非同期になることができます。クライアントは、FLUSH_ASYNC_OK フラグを設定してこの動作を要求します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

リモートトランスポートプロバイダーの**flushqueues**の実装は、キューのフラッシュ方法を制御するために、ログオンオブジェクトの状態行の**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティにビットを設定します。 リモートビューアーが FLUSH_UPLOAD フラグを渡す場合、 **flushqueues**メソッドは STATUS_INBOUND_ENABLED と STATUS_INBOUND_ACTIVE ビットを設定する必要があります。 リモートビューアーが FLUSH_DOWNLOAD フラグを渡す場合、 **flushqueues**メソッドは STATUS_OUTBOUND_ENABLED と STATUS_OUTBOUND_ACTIVE ビットを設定する必要があります。 **flushqueues**は S_OK を返す必要があります。 その後、MAPI スプーラーは、メッセージをアップロードしてダウンロードするための適切なアクションを開始します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI スプーラー状態オブジェクトの呼び出しは、適切なトランスポートプロバイダーとの間のすべてのメッセージを転送するためのディレクティブです。 個別のトランスポートプロバイダーの status オブジェクトを呼び出すと、そのプロバイダーのメッセージのみが影響を受けます。
  
## <a name="see-also"></a>関連項目



[PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
  
[PidTagStatusCode 標準プロパティ](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

