---
title: トランスポート プロバイダーの解放
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: ea9656f9571777478d3db9a2613fbff5ddef0ee6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592291"
---
# <a name="releasing-the-transport-provider"></a>トランスポート プロバイダーの解放

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI、または MAPI スプーラーが終了したときトランスポート ログオン オブジェクトを使用します。
  
1. MAPI、または MAPI スプーラーは、トランスポート プロバイダーの[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)メソッドを呼び出します。 
    
2. トランスポート プロバイダーは、 [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md)メソッドを呼び出して、状態オブジェクトを無効にします。 トランスポート プロバイダーは、メッセージ オブジェクトを無効にするかどうか送信または**TransportLogoff**の呼び出し時に受信されるが**TransportLogoff**に渡されたフラグに依存します。
    
3. トランスポート プロバイダーは、状態テーブルから、トランスポート プロバイダーの行を削除して、一意の識別子 (Uid) [IMAPISupport で設定された内部テーブルからを削除するサポート オブジェクトの[リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)のメソッドを呼び出して、:。SetProviderUID](imapisupport-setprovideruid.md)メソッドです。 それをデクリメントこのプロバイダー オブジェクトのアクティブなログオンが正常のオブジェクトの数です。 カウントが 0 になった場合、MAPI はプロバイダー オブジェクトの**リリース**、 [IXPProvider::Shutdown](ixpprovider-shutdown.md)メソッドを呼び出します。 最後の既知のプロバイダー オブジェクトがこのプロセスでこの DLL を使用する場合、MAPI は、後で、DLL の**終わった**関数を呼び出します。 MAPI サポート オブジェクトのメモリは解放され、 **Release**メソッドのサポート オブジェクトを返します。 
    
4. **TransportLogoff**メソッドは S_OK を返します。 
    
5. MAPI、または MAPI スプーラーは、トランスポート プロバイダーのログオン オブジェクトの**リリース**を呼び出します。 オブジェクトのメモリを解放するとします。 
    
6. MAPI、または MAPI スプーラーは、プロバイダーの DLL に**終わった**を呼び出します。 
    
堅牢性、ログオンし、プロバイダーのオブジェクトは、 **TransportLogoff**または**シャット ダウン**の方法と呼ばれることがなく自身の最終の**解放**呼び出しを処理することにあります。 **リリース**はこのような場合に呼び出されると、トランスポート プロバイダーは、 **TransportLogoff**または**シャット ダウン****のリリース**の後に 0 個の引数を指定して呼び出された場合と同様に呼び出しを扱う必要があります。
  

