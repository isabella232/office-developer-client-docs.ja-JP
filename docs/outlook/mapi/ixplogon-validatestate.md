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
  
トランスポート プロバイダーの外部状態を確認します。 
  
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
  
> [in]状態チェックの実行方法と状態チェックの結果を制御するフラグのビットマスク。 次のフラグを設定できます。
    
ABORT_XP_HEADER_OPERATION 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 トランスポート プロバイダーは、操作の作業を続行するか、操作を中止し、操作を返MAPI_E_USER_CANCELED。 
    
CONFIG_CHANGED 
  
> MAPI スプーラーが [IXPLogon::AddressTypes](ixplogon-addresstypes.md) メソッドを呼び出して、現在読み込まれているトランスポート プロバイダーの状態を検証します。 また、このフラグを使用すると、MAPI スプーラーは、クライアント アプリケーションにログオフしてから再度ログオンすることなく、重大なトランスポート プロバイダーのエラーを修正できます。 
    
FORCE_XP_CONNECT 
  
> ユーザーが接続操作を選択しました。 このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHEと一緒に使用すると、接続アクションはキャッシュなしで実行されます。
    
FORCE_XP_DISCONNECT 
  
> ユーザーが切断操作を選択しました。 このフラグを使用して、REFRESH_XP_HEADER_CACHEまたはPROCESS_XP_HEADER_CACHEキャッシュせずに切断アクションが実行されます。
    
PROCESS_XP_HEADER_CACHE 
  
> ヘッダー キャッシュ テーブル内のエントリを処理し、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたメッセージはすべてダウンロードし、MSGSTATUS_REMOTE_DELETE フラグでマークされたメッセージはすべて削除する必要があります。 設定されたメッセージとMSGSTATUS_REMOTE_DOWNLOAD設定MSGSTATUS_REMOTE_DELETEメッセージを移動する必要があります。
    
REFRESH_XP_HEADER_CACHE 
  
> メッセージ ヘッダーの新しい一覧をダウンロードし、すべてのメッセージ状態マーキング フラグをクリアする必要があります。
    
SUPPRESS_UI 
  
> トランスポート プロバイダーがユーザー インターフェイスを表示しなかします。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中です。完了を許可するか、この操作を試みる前に停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> 関連するリモート トランスポート プロバイダーはユーザー インターフェイスをサポートしていないので、クライアント アプリケーション自体がダイアログ ボックスを表示する必要があります。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーは **、IXPLogon::ValidateState** メソッドを呼び出して、STATUS オブジェクトの [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドの呼び出しをサポートします。 トランスポート プロバイダーは、MAPI スプーラーが現在のログオン セッションの状態オブジェクトを開き、そのオブジェクトで **IMAPIStatus::ValidateState** を呼び出した場合とまったく同じ **IXPLogon::ValidateState** 呼び出しに応答する必要があります。 
  
**IMAPIStatus::ValidateState** の実装をサポートするために、MAPI スプーラーは、プロファイル セッションで実行中のすべてのアクティブなトランスポート プロバイダーのすべてのログオン オブジェクトで **IXPLogon::ValidateState** を呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

