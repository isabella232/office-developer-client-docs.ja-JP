---
title: IMAPIStatusFlushQueues
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d6c221ae307edb9d84cfcc0026660ea4bce7fadd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800713"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**適用対象**: Outlook 
  
送信またはアップロードまたはダウンロードをすぐに受信を待機しているすべてのメッセージを強制的にします。 MAPI スプーラーの状態のオブジェクトおよびトランスポート プロバイダーを実装する状態オブジェクトは、このメソッドをサポートします。
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。
    
 _cbTargetTransport_
  
> [in]_LpTargetTransport_パラメーターで指定されたエントリの識別子のバイト数です。 _CbTargetTransport_パラメーターは、MAPI スプーラーを無効の状態のオブジェクトへの呼び出しでのみ設定されています。 トランスポート プロバイダーへの呼び出し、 _cbTargetTransport_パラメーターが 0 に設定されます。 
    
 _lpTargetTransport_
  
> [in]そのメッセージ キューをフラッシュするのには、トランスポート プロバイダーのエントリの識別子へのポインター。 _LpTargetTransport_パラメーターは、MAPI スプーラーを無効の状態のオブジェクトへの呼び出しでのみ設定されています。 トランスポート プロバイダーへの呼び出し、 _lpTargetTransport_パラメーターは NULL に設定します。 
    
 _ulFlags_
  
> [in]フラッシュ操作を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
FLUSH_ASYNC_OK 
  
> フラッシュ操作が非同期的に発生することができます。 このフラグは、MAPI スプーラーを無効の状態のオブジェクトにのみ適用されます。 
    
FLUSH_DOWNLOAD 
  
> 受信メッセージ キューをフラッシュする必要があります。
    
FLUSH_FORCE 
  
> フラッシュ操作にする必要がありますパフォーマンスが低下する可能性も関係なく、発生します。 非同期型のトランスポート プロバイダーを対象としたとき、このフラグを設定する必要があります。
    
FLUSH_NO_UI 
  
> ステータス オブジェクトでは、進行状況のインジケーターが表示されない必要があります。
    
FLUSH_UPLOAD 
  
> 送信メッセージのキューをフラッシュする必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フラッシュ操作が正常に完了しました。
    
MAPI_E_BUSY 
  
> 別の操作が実行中です。完了するために許可するか、停止する、この操作を開始する前に。
    
MAPI_E_NO_SUPPORT 
  
> 状態オブジェクトは、この操作をサポートしていません状態オブジェクトの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティに STATUS_FLUSH_QUEUES フラグがない場合で示される。
    
## <a name="remarks"></a>注釈

**IMAPIStatus::FlushQueues**メソッドは、MAPI スプーラーを無効またはトランスポート プロバイダーすぐに発信キュー内のすべてのメッセージを送信または受信キューからすべてのメッセージを受信するを要求します。 **FlushQueues**は、MAPI スプーラーの状態のオブジェクトのみが、トランスポート プロバイダーの供給状態のオブジェクトによって実装されます。 
  
非同期要求のクライアントは、作業を続行できるように、MAPI_E_BUSY が返されます。 
  
既定では、 **FlushQueues**は、同期操作です。フラッシュが完了するまで、制御は呼び出し側に返されません。 のみ、フラッシュ操作 MAPI スプーラーが実行できる可能性があります。クライアントは、FLUSH_ASYNC_OK フラグを設定することによってこの動作を要求します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**FlushQueues**のリモート トランスポート プロバイダーの実装では、キューをフラッシュする方法を制御するため、ログオン オブジェクトの [状態] 行で、 **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) のプロパティのビットを設定します。 リモート ビューアーは、FLUSH_UPLOAD フラグに合格した場合、 **FlushQueues**メソッドは、STATUS_INBOUND_ENABLED と STATUS_INBOUND_ACTIVE のビットを設定します。 リモート ビューアーは、FLUSH_DOWNLOAD フラグに合格した場合、 **FlushQueues**メソッドは、STATUS_OUTBOUND_ENABLED と STATUS_OUTBOUND_ACTIVE のビットを設定します。 **FlushQueues**では、S_OK を返す必要がありますし。 MAPI スプーラーを無効にし、アップロードし、メッセージをダウンロードするには、適切なアクションが開始されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI スプーラーの状態のオブジェクトへの呼び出しは、するか、適切なトランスポート プロバイダーからすべてのメッセージを転送するディレクティブです。 個々 のトランスポート プロバイダーの状態のオブジェクトを呼び出すと、そのプロバイダーのメッセージだけが影響を受けます。
  
## <a name="see-also"></a>関連項目



[PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
  
[PidTagStatusCode 標準プロパティ](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

