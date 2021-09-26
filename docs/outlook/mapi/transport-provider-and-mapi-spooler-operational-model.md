---
title: トランスポート プロバイダーと MAPI スプーラー運用モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9613c46ee105d24317c6c902f8d5f122cf4689cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619597"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>トランスポート プロバイダーと MAPI スプーラー運用モデル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーの初期化、起動、処理、シャットダウン、および初期化解除は、MAPI スプーラーからトランスポート プロバイダーへの一連の呼び出しによって実行されます。 呼び出しは次のように順序付けされます。
  
1. MAPI スプーラーは [、XPProviderInit](xpproviderinit.md) 関数を呼び出し、サポート オブジェクトを渡し、プロバイダー オブジェクトを取得し、トランスポート プロバイダーと MAPI スプーラーが互換性のある MAPI バージョン番号の範囲をサポートしているのを確認します。 
    
2. MAPI スプーラーは、IXPProvider: IUnknown インターフェイスの [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) メソッド [を呼び出](ixpprovideriunknown.md) します。 MAPI スプーラーとトランスポート プロバイダーの間で、プロファイルの現在のセクションの資格情報を使用してセッションが確立されます。 トランスポート プロバイダーは、ログオン オブジェクトを返します。 
    
3. MAPI スプーラーは [、IXPLogon::AddressTypes メソッドを呼び出](ixplogon-addresstypes.md) します。 トランスポート プロバイダーは、受け入れる一意の識別子 (UID) と電子メール アドレスの種類の一覧を返します。 
    
4. トランスポート プロバイダーは [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを呼び出して、MAPI 状態テーブルに行を作成します。 
    
5. MAPI スプーラーは [、IXPLogon::TransportNotify](ixplogon-transportnotify.md) メソッドを呼び出して、メッセージの送受信を有効にします。 
    
6. **TransportLogon** 呼び出しの戻り値としてトランスポート プロバイダーから要求された場合、MAPI スプーラーは定期的に [IXPLogon::Idle メソッドを呼び出](ixplogon-idle.md)します。 アイドル処理は、トランスポート プロバイダーが基になるメッセージング システムに新しいメッセージをポーリングする必要がある場合、または他の優先度の低いタスクを実行する必要がある場合に便利です。 
    
7. MAPI スプーラーとトランスポート プロバイダーは、メッセージの送受信を行います。 詳細については、「Message [Submission Model and Message Reception](message-submission-model.md) [Model」を参照してください](message-reception-model.md)。 MAPI スプーラー は、サポート、メッセージ、および添付ファイル オブジェクトの要求と呼び出しを転送します。
    
8. MAPI スプーラーは **、TransportNotify** メソッドを呼び出して、メッセージの送受信を無効にします。 
    
9. MAPI スプーラーは、ログオン オブジェクトとプロバイダー オブジェクトを解放します。 詳細については [、「IXPProvider::Shutdown メソッド」を参照](ixpprovider-shutdown.md) してください。 
    

