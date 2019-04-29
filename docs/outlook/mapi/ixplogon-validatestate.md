---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439486"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーの外部の状態を確認します。 
  
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
  
> 順番状態チェックの実行方法と状態チェックの結果を制御するフラグのビットマスク。 次のフラグを設定できます。
    
ABORT_XP_HEADER_OPERATION 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 トランスポートプロバイダーは、操作を続行するか、操作を中止して MAPI_E_USER_CANCELED を返すかを選択できます。 
    
CONFIG_CHANGED 
  
> MAPI スプーラーに[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すことによって、現在読み込まれているトランスポートプロバイダーの状態を検証します。 また、このフラグを使用すると、MAPI スプーラーは、クライアントアプリケーションがログオフしてから再度ログオンすることなく、重要なトランスポートプロバイダーのエラーを修正する機会を得ることができます。 
    
FORCE_XP_CONNECT 
  
> ユーザーが接続操作を選択しました。 このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグと共に使用すると、接続アクションはキャッシュなしで行われます。
    
FORCE_XP_DISCONNECT 
  
> ユーザーが切断操作を選択しました。 このフラグが REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE で使用されている場合、disconnect 操作はキャッシュなしで行われます。
    
PROCESS_XP_HEADER_CACHE 
  
> ヘッダーキャッシュテーブル内のエントリを処理する必要があり、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたすべてのメッセージをダウンロードして、MSGSTATUS_REMOTE_DELETE フラグでマークされたすべてのメッセージを削除する必要があります。 MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE の両方が設定されたメッセージは移動する必要があります。
    
REFRESH_XP_HEADER_CACHE 
  
> メッセージヘッダーの新しいリストがダウンロードされ、すべてのメッセージ状態マーキングフラグがクリアされる必要があります。
    
SUPPRESS_UI 
  
> トランスポートプロバイダーがユーザーインターフェイスを表示できないようにします。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中です。完了することが許可されているか、この操作を実行する前に停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> 関係するリモートトランスポートプロバイダーはユーザーインターフェイスをサポートしておらず、クライアントアプリケーション自体にダイアログボックスを表示する必要があります。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、 **IXPLogon:: validatestate**メソッドを呼び出して、ステータスオブジェクトの[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドへの呼び出しをサポートします。 トランスポートプロバイダーは、 **IXPLogon:: validatestate**呼び出しに応答する必要があります。これは、MAPI スプーラーが現在のログオンセッションの状態オブジェクトを開いており、そのオブジェクトに対して**imapistatus:: validatestate**を呼び出した場合と同じです。 
  
**imapistatus:: validatestate**の実装をサポートするために、MAPI スプーラーは、プロファイルセッションで実行されているすべてのアクティブなトランスポートプロバイダーのすべてのログオンオブジェクトに対して**IXPLogon:: validatestate**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

