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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282832"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
保留中の受信または送信メッセージをすべてトランスポートプロバイダーが直ちに配信するよう要求します。
  
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
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lptargettransport_
  
> 順番予約語NULL である必要があります。
    
 _ulFlags_
  
> 順番メッセージキューのフラッシュがどのように行われるかを制御するフラグのビットマスク。 次のフラグを設定できます。
    
FLUSH_DOWNLOAD 
  
> 受信メッセージキューまたはキューをフラッシュする必要があります。
    
FLUSH_FORCE 
  
> 可能であれば、トランスポートプロバイダーはこの要求を処理する必要があります (これを実行すると時間がかかる場合もあります)。 
    
FLUSH_NO_UI 
  
> トランスポートプロバイダーは、ユーザーインターフェイスを表示しません。
    
FLUSH_UPLOAD 
  
> 送信メッセージキューまたはキューをフラッシュする必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>解説

mapi スプーラーは**IXPLogon:: flushqueues**メソッドを呼び出して、mapi スプーラーがメッセージの処理を開始しようとしていることをトランスポートプロバイダーに通知します。 トランスポートプロバイダーは、 [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを呼び出して、ステータス行の**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティでその状態に適したビットを設定する必要があります。 状態行を更新した後、トランスポートプロバイダーは**flushqueues**呼び出しに対して S_OK を返す必要があります。 その後、mapi スプーラーは、mapi スプーラーと同期された操作で、メッセージの送信を開始します。 
  
[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドの実装をサポートするために、MAPI スプーラーはプロファイルセッションで実行されているアクティブなトランスポートプロバイダーのすべてのログオンオブジェクトに対して**IXPLogon:: flushqueues**を呼び出します。 **imapistatus:: flushqueues**へのクライアントアプリケーション呼び出しの結果として、トランスポートプロバイダーの**flushqueues**メソッドが呼び出されると、メッセージ処理はクライアントに非同期で行われます。
  
## <a name="see-also"></a>関連項目



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

