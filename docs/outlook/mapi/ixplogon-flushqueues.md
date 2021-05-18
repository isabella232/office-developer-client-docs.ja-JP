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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421971"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーが保留中のすべての受信メッセージまたは送信メッセージを直ちに配信する要求。
  
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
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpTargetTransport_
  
> [in]予約済み。NULL である必要があります。
    
 _ulFlags_
  
> [in]メッセージ キューのフラッシュの実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
FLUSH_DOWNLOAD 
  
> 受信メッセージ キューまたはキューをフラッシュする必要があります。
    
FLUSH_FORCE 
  
> トランスポート プロバイダーは、可能な場合は、時間がかかる場合でも、この要求を処理する必要があります。 
    
FLUSH_NO_UI 
  
> トランスポート プロバイダーは、ユーザー インターフェイスを表示しない必要があります。
    
FLUSH_UPLOAD 
  
> 送信メッセージ キューまたはキューをフラッシュする必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは **、IXPLogon::FlushQueues** メソッドを呼び出して、MAPI スプーラーがメッセージの処理を開始する予定であるトランスポート プロバイダーに通知します。 トランスポート プロバイダーは [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを呼び出して、状態行の **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの状態に適切なビットを設定する必要があります。 状態行を更新した後、トランスポート プロバイダーは **FlushQueues** 呼び出しS_OKを返す必要があります。 その後、MAPI スプーラーはメッセージの送信を開始し、操作は MAPI スプーラーと同期します。 
  
[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドの実装をサポートするために、MAPI スプーラーは、プロファイル セッションで実行されているアクティブ なトランスポート プロバイダーのすべてのログオン オブジェクトに対して **IXPLogon::FlushQueues** を呼び出します。 **IMAPIStatus::FlushQueues** へのクライアント アプリケーション呼び出しの結果としてトランスポート プロバイダーの **FlushQueues** メソッドが呼び出された場合、メッセージ処理はクライアントに対して非同期的に行われます。
  
## <a name="see-also"></a>関連項目



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

