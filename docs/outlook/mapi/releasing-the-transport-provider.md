---
title: トランスポートプロバイダーを解放する
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
# <a name="releasing-the-transport-provider"></a>トランスポートプロバイダーを解放する

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi または mapi スプーラーがトランスポートログオンオブジェクトを使用して終了した場合:
  
1. mapi または mapi スプーラーは、トランスポートプロバイダーの[IXPLogon:: transportlogoff](ixplogon-transportlogoff.md)メソッドを呼び出します。 
    
2. トランスポートプロバイダーは、 [imapisupport:: makeinvalid](imapisupport-makeinvalid.md)メソッドを呼び出して、status オブジェクトを無効にします。 transport **logoff**呼び出しの時点で送受信されたメッセージオブジェクトがトランスポートプロバイダによって無効にされるかどうかは、 **transportlogoff**に渡されたフラグによって決まります。
    
3. トランスポートプロバイダーは、サポートオブジェクトの[IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出して、状態テーブルからトランスポートプロバイダーの行を削除し、imapisupport で設定された一意識別子 (uid) をすべて内部テーブルから削除します。 [setprovideruid](imapisupport-setprovideruid.md)メソッド。 このプロバイダーオブジェクトでアクティブになっている既知のログオンオブジェクトの数をデクリメントします。 数が0になると、MAPI は、プロバイダーオブジェクトで[ixpprovider:: Shutdown](ixpprovider-shutdown.md)メソッドと**Release**を呼び出します。 このプロセスでこの dll を使用する最後の既知のプロバイダーオブジェクトである場合、MAPI は dll の**FreeLibrary**関数を後で呼び出します。 MAPI サポートオブジェクトのメモリは解放され、support オブジェクトの**Release**メソッドは返されます。 
    
4. **transportlogoff**メソッドは S_OK を返します。 
    
5. mapi または mapi スプーラーは、トランスポートプロバイダーのログオンオブジェクトで**リリース**を呼び出します。 オブジェクトのメモリが解放されます。 
    
6. mapi または mapi スプーラーは、プロバイダー DLL で**FreeLibrary**を呼び出します。 
    
堅牢性を考慮して、ログオンおよびプロバイダーオブジェクトは、最初に**transportlogoff**または**Shutdown**メソッドを呼び出さずに、それ自体の最終**リリース**呼び出しを処理できる必要があります。 このような場合に**release**が呼び出された場合、トランスポートプロバイダーは、 **** 引数ゼロを**** 指定して**release**を呼び出した場合と同様に、呼び出しを処理する必要があります。
  

