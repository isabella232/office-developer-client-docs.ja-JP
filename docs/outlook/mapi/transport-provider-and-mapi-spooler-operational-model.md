---
title: トランスポートプロバイダーと MAPI スプーラー運用モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426626"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>トランスポートプロバイダーと MAPI スプーラー運用モデル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーの初期化、スタートアップ、処理、シャットダウン、および deinitialization は、MAPI スプーラーからトランスポートプロバイダーへの一連の呼び出しによって実行されます。 呼び出しは次のように順序付けられます。
  
1. mapi スプーラーは、 [xps の init](xpproviderinit.md)関数を呼び出し、サポートオブジェクトを渡して、プロバイダーオブジェクトを取得します。また、トランスポートプロバイダーと mapi スプーラーが、互換性のある mapi バージョン番号の範囲をサポートしているかどうかを確認します。 
    
2. MAPI スプーラーは、 [ixpprovider: IUnknown](ixpprovideriunknown.md)インターフェイスの[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)メソッドを呼び出します。 プロファイルの現在のセクションの資格情報を使用して、MAPI スプーラーとトランスポートプロバイダーの間にセッションが確立されます。 トランスポートプロバイダーがログオンオブジェクトを返します。 
    
3. MAPI スプーラーは、 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出します。 トランスポートプロバイダーは、受け付ける一意識別子 (uid) と電子メールアドレスの種類の一覧を返します。 
    
4. トランスポートプロバイダーは、MAPI 状態テーブルに行を作成する[imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを呼び出します。 
    
5. MAPI スプーラーは、 [IXPLogon:: transportnotify](ixplogon-transportnotify.md)メソッドを呼び出して、メッセージの送信と受信を有効にします。 
    
6. トランスポートプロバイダーによって、 **transportlogon**呼び出しに対して戻り値が要求されると、MAPI スプーラーは[IXPLogon:: Idle](ixplogon-idle.md)メソッドを定期的に呼び出します。 アイドル処理は、トランスポートプロバイダーが、新しいメッセージの基礎となるメッセージングシステムをポーリングしたり、優先度の低いタスクを実行したりする必要がある場合に便利です。 
    
7. MAPI スプーラーとトランスポートプロバイダーは、メッセージを送受信します。 詳細については、「[メッセージ送信モデル](message-submission-model.md)および[メッセージ受信モデル](message-reception-model.md)」を参照してください。 MAPI スプーラーサービスは、サポート、メッセージ、および添付ファイルオブジェクトのトランスポート要求と呼び出しを行います。
    
8. MAPI スプーラーは、メッセージの送信と受信を無効にするために、 **transportnotify**メソッドを呼び出します。 
    
9. MAPI スプーラーは、ログオンおよびプロバイダーオブジェクトを解放します。 詳細については、 [ixpprovider:: Shutdown](ixpprovider-shutdown.md)メソッドを参照してください。 
    

