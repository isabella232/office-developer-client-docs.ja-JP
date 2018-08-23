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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4fd0dd02c5cf6f6a49b782d06c02e373dcfc3327
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577486"
---
# <a name="ixplogonvalidatestate"></a>IXPLogon::ValidateState

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート プロバイダーの外部の状況をチェックします。 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]状態チェックの実行方法を制御するフラグのビットマスクと状態の結果を確認します。 次のフラグを設定することができます。
    
ABORT_XP_HEADER_OPERATION 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 トランスポート プロバイダーは、操作の操作を続行するオプションか、操作を中止して MAPI_E_USER_CANCELED を返します。 
    
CONFIG_CHANGED 
  
> MAPI スプーラーを無効に、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すことで、現在読み込まれているトランスポート プロバイダーの状態を検証します。 このフラグでは、いったんログオフして再度ログオンするクライアント アプリケーションを強制することのないトランスポート プロバイダーの重要なエラーを修正すること、MAPI スプーラーも提供します。 
    
FORCE_XP_CONNECT 
  
> ユーザーは、接続操作を選択します。 REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグを指定してこのフラグを使用する場合は、キャッシュを使用しない接続の動作が発生します。
    
FORCE_XP_DISCONNECT 
  
> ユーザーは、切断操作を選択します。 このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE を使用する場合は、キャッシュを使用しない切断操作が発生します。
    
PROCESS_XP_HEADER_CACHE 
  
> ヘッダー キャッシュ テーブル内のエントリを処理する必要があります、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたすべてのメッセージをダウンロードするか、および、MSGSTATUS_REMOTE_DELETE フラグでマークされたすべてのメッセージを削除する必要があります。 MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE の設定の両方を持つメッセージを移動する必要があります。
    
REFRESH_XP_HEADER_CACHE 
  
> メッセージ ヘッダーの新しいリストをダウンロードするか、およびフラグをマークするすべてのメッセージの状態をクリアする必要があります。
    
SUPPRESS_UI 
  
> トランスポート プロバイダーが、ユーザー インターフェイスを表示するを防ぎます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
MAPI_E_BUSY 
  
> 別の操作が実行中です。完了するために許可するか、この操作を実行しようとする前に停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> リモート トランスポート プロバイダーの関連するが、ユーザー インターフェイスをサポートしていませんし、クライアント アプリケーションでは、ダイアログ ボックスを表示する必要があります。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、状態オブジェクトの[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドの呼び出しをサポートするために**IXPLogon::ValidateState**メソッドを呼び出します。 トランスポート プロバイダーは、正確に場合と、MAPI スプーラーが現在のログオン セッションの状態のオブジェクトを開くし、そのオブジェクトに**IMAPIStatus::ValidateState**と呼ばれる**IXPLogon::ValidateState**の呼び出しに応答します。 
  
**IMAPIStatus::ValidateState**の実装をサポートするには、MAPI スプーラーは、ログオン オブジェクトのすべてのプロファイル セッションで実行されているすべてのアクティブなトランスポート プロバイダーの**IXPLogon::ValidateState**を呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

