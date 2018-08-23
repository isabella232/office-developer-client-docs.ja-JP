---
title: トランスポート プロバイダーと MAPI スプーラー運用モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 26d9982248fde015a584eb79cc248bafc5afc6bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594034"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>トランスポート プロバイダーと MAPI スプーラー運用モデル

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート プロバイダーの初期化、起動、処理、シャット ダウン、二つの後処理は、一連の MAPI スプーラーからトランスポート プロバイダーへの呼び出しによって実行されます。 呼び出しは次のように順序付けられました。
  
1. MAPI スプーラー [XPProviderInit](xpproviderinit.md)関数を呼び出し、オブジェクトがサポート、プロバイダー オブジェクトを取得、トランスポート プロバイダーが、MAPI スプーラーが互換性のある範囲の MAPI のバージョン番号をサポートすることを確認します。 
    
2. MAPI スプーラーは、の[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)メソッドを呼び出して、 [IXPProvider: IUnknown](ixpprovideriunknown.md)インタ フェースです。 MAPI スプーラーとプロファイルの現在のセクション内の資格情報を使用してトランスポート プロバイダーの間でセッションが確立されます。 トランスポート プロバイダーでは、ログオン オブジェクトを返します。 
    
3. MAPI スプーラーは、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出します。 トランスポート プロバイダーは、受け入れることは、一意識別子 (Uid) と電子メール アドレスの種類の一覧を返します。 
    
4. トランスポート プロバイダーでは、MAPI の状態テーブル内の行を作成する[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドを呼び出します。 
    
5. MAPI スプーラーでは、メッセージの送信と受信を有効にする[IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッドを呼び出します。 
    
6. **TransportLogon**呼び出し、その戻り値のトランスポート プロバイダーによって要求されると、MAPI スプーラーは定期的に[IXPLogon::Idle](ixplogon-idle.md)メソッドを呼び出します。 アイドル処理では、トランスポート プロバイダーが新しいメッセージの基になるメッセージング システムをポーリングまたはその他の優先度の低いタスクを実行する必要がある場合に便利です。 
    
7. MAPI スプーラーとトランスポート プロバイダー メッセージを送信します。 詳細については、[メッセージの送信のモデル](message-submission-model.md)と[メッセージの受信のモデル](message-reception-model.md)を参照してください。 MAPI スプーラーは、トランスポートの要求を処理し、サポート、メッセージ、および添付ファイルのオブジェクトを呼び出します。
    
8. MAPI スプーラーでは、メッセージの送受信を無効にする**TransportNotify**メソッドを呼び出します。 
    
9. MAPI スプーラーは、ログオン、およびプロバイダーのオブジェクトを解放します。 詳細については、 [IXPProvider::Shutdown](ixpprovider-shutdown.md)メソッドを参照してください。 
    

