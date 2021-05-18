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
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328386"
---
# <a name="releasing-the-transport-provider"></a>トランスポート プロバイダーの解放

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI または MAPI スプーラーがトランスポート ログオン オブジェクトの使用を終了すると、次の処理が完了します。
  
1. MAPI または MAPI スプーラーは、トランスポート プロバイダーの [IXPLogon::TransportLogoff メソッドを呼び出](ixplogon-transportlogoff.md) します。 
    
2. トランスポート プロバイダーは [、IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) メソッドを呼び出して、status オブジェクトを無効にします。 トランスポート プロバイダーが **TransportLogoff** 呼び出し時に送信または受信されるメッセージ オブジェクトを無効にするかどうかは **、TransportLogoff** に渡されたフラグによって異なります。
    
3. トランスポート プロバイダーは、サポート オブジェクトの [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) メソッドを呼び出して、トランスポート プロバイダーの行を状態テーブルから削除し [、IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) メソッドで設定された一意の識別子 (UID) を内部テーブルから削除します。 このプロバイダー オブジェクトでアクティブな既知のログオン オブジェクトの数をデクレメントします。 カウントが 0 に達すると、MAPI は [IXPProvider::Shutdown](ixpprovider-shutdown.md) メソッドと **Release** をプロバイダー オブジェクトで呼び出します。 このプロセスでこの DLL を使用する最後の既知のプロバイダー オブジェクトである場合、MAPI は後で DLL の **FreeLibrary** 関数を呼び出します。 MAPI サポート オブジェクトのメモリが解放され、サポート オブジェクト **Release** メソッドが返されます。 
    
4. **TransportLogoff メソッドは**、次のS_OK。 
    
5. MAPI または MAPI スプーラーは、トランスポート **プロバイダー** のログオン オブジェクトで Release を呼び出します。 オブジェクトのメモリが解放されます。 
    
6. MAPI または MAPI スプーラーは、プロバイダー DLL **で FreeLibrary** を呼び出します。 
    
堅牢性を高めるには、ログオン オブジェクトとプロバイダー オブジェクトは、最初に **TransportLogoff** メソッドまたは **Shutdown** メソッドを呼び出さずに、自身で最終的なリリース呼び出しを処理できる必要があります。 このような **場合に** Release が呼び出された場合、トランスポート プロバイダーは、引数が 0 の **TransportLogoff** または **Shutdown** が呼び出された場合と同様に呼び出しを処理し、その後に Release を指定 **します**。
  

