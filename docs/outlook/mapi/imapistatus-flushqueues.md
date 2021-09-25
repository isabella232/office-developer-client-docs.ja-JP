---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5f85765a2440be83a5aafa900b686b2f6de84aa6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584403"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信または受信を待機しているすべてのメッセージを、すぐにアップロードまたはダウンロードする必要があります。 トランスポート プロバイダーが実装する MAPI スプーラー状態オブジェクトと状態オブジェクトは、このメソッドをサポートします。
  
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
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。
    
 _cbTargetTransport_
  
> [in]  _lpTargetTransport_ パラメーターが指すエントリ識別子のバイト 数。 _cbTargetTransport_ パラメーターは、MAPI スプーラーの状態オブジェクトへの呼び出しでのみ設定されます。 トランスポート プロバイダーへの呼び出しの場合  _、cbTargetTransport_ パラメーターは 0 に設定されます。 
    
 _lpTargetTransport_
  
> [in]メッセージ キューをフラッシュするトランスポート プロバイダーのエントリ識別子へのポインター。 _lpTargetTransport パラメーター_ は、MAPI スプーラーの状態オブジェクトの呼び出しでのみ設定されます。 トランスポート プロバイダーへの呼び出しの場合  _、lpTargetTransport_ パラメーターは NULL に設定されます。 
    
 _ulFlags_
  
> [in]フラッシュ操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
FLUSH_ASYNC_OK 
  
> フラッシュ操作は非同期的に行われます。 このフラグは、MAPI スプーラーの状態オブジェクトにのみ適用されます。 
    
FLUSH_DOWNLOAD 
  
> 受信メッセージ キューはフラッシュする必要があります。
    
FLUSH_FORCE 
  
> フラッシュ操作は、パフォーマンスが低下する可能性があるにもかかわらず、関係なく発生する必要があります。 このフラグは、非同期トランスポート プロバイダーを対象とする場合に設定する必要があります。
    
FLUSH_NO_UI 
  
> status オブジェクトは進行状況インジケーターを表示しない必要があります。
    
FLUSH_UPLOAD 
  
> 送信メッセージ キューはフラッシュする必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フラッシュ操作が成功しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中です。この操作を開始する前に、完了を許可するか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> status オブジェクトは、status オブジェクトの PR_RESOURCE_METHODS **(** [PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_FLUSH_QUEUES フラグがない場合に示されるこの操作をサポートします。
    
## <a name="remarks"></a>注釈

**IMAPIStatus::FlushQueues** メソッドは、MAPI スプーラーまたはトランスポート プロバイダーが送信キュー内のすべてのメッセージを直ちに送信するか、受信キューからすべてのメッセージを受信する要求を行います。 **FlushQueues は** 、MAPI スプーラーの状態オブジェクトとトランスポート プロバイダーが提供する状態オブジェクトによってのみ実装されます。 
  
MAPI_E_BUSYを続行できるよう、非同期要求に対して返す必要があります。 
  
既定では **、FlushQueues は** 同期操作です。フラッシュが完了するまで、コントロールは呼び出し元に戻しません。 MAPI スプーラーによって実行されるフラッシュ操作のみを非同期にできます。クライアントは、この動作を要求するには、FLUSH_ASYNC_OKフラグを設定します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

リモート トランスポート プロバイダーによる **FlushQueues** の実装では、ログオン オブジェクトの状態行の **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティのビットを設定して、キューのフラッシュ方法を制御します。 リモート ビューアーが FLUSH_UPLOAD フラグを渡す場合 **、FlushQueues** メソッドは、STATUS_INBOUND_ENABLEDビットとSTATUS_INBOUND_ACTIVEする必要があります。 リモート ビューアーが FLUSH_DOWNLOAD フラグを渡す場合 **、FlushQueues** メソッドは、STATUS_OUTBOUND_ENABLEDビットSTATUS_OUTBOUND_ACTIVEする必要があります。 **FlushQueues は、** 次にデータをS_OK。 MAPI スプーラーは、メッセージをアップロードおよびダウンロードするための適切なアクションを開始します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI スプーラー状態オブジェクトへの呼び出しは、すべてのメッセージを適切なトランスポート プロバイダーと転送するディレクティブです。 個々のトランスポート プロバイダーの状態オブジェクトを呼び出す場合、そのプロバイダーのメッセージだけが影響を受ける。
  
## <a name="see-also"></a>関連項目



[PidTagResourceMethods 標準プロパティ](pidtagresourcemethods-canonical-property.md)
  
[PidTagStatusCode 標準プロパティ](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

