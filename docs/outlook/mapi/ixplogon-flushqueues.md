---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 116e3cfaace9c0965001021575b76ec371667877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801254"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**適用対象**: Outlook 
  
要求がトランスポート プロバイダーは、すべての保留の受信または送信メッセージを即座に配信します。
  
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
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpTargetTransport_
  
> [in]予約されています。NULL である必要があります。
    
 _ulFlags_
  
> [in]メッセージ キューのフラッシュを実現する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
FLUSH_DOWNLOAD 
  
> 受信メッセージのキューをフラッシュする必要があります。
    
FLUSH_FORCE 
  
> トランスポート プロバイダーは、これは時間がかかる場合でもこの要求を可能であれば、処理されます。 
    
FLUSH_NO_UI 
  
> トランスポート プロバイダーは、ユーザー インターフェイスを表示しない必要があります。
    
FLUSH_UPLOAD 
  
> 送信メッセージのキューをフラッシュする必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、MAPI スプーラーがメッセージの処理を開始しようとしていますが、トランスポート プロバイダーに通知する**IXPLogon::FlushQueues**メソッドを呼び出します。 トランスポート プロバイダーは、 **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) のプロパティの [状態] 行で、適切なビットの状態を設定するのには[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドを呼び出す必要があります。 その [状態] 行を更新した後には、トランスポート プロバイダーは、必要があります、 **FlushQueues**の呼び出しに、S_OK を返します。 MAPI スプーラーは、MAPI スプーラーを無効に同期されている操作をメッセージの送信を開始します。 
  
[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドの実装をサポートするためには、MAPI スプーラーは、ログオン オブジェクトのすべてのプロファイル セッションで実行されているアクティブなトランスポート プロバイダーの**IXPLogon::FlushQueues**を呼び出します。 **IMAPIStatus::FlushQueues**クライアント アプリケーションの呼び出しによって、トランスポート プロバイダーの**FlushQueues**メソッドを呼び出すと、クライアントにメッセージの処理が非同期に発生します。
  
## <a name="see-also"></a>関連項目



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

