---
title: Outlook が Exchange キャッシュモードの場合にリモートサーバー上のストアにアクセスする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: '最終更新日: 2012 年7月2日'
ms.openlocfilehash: cfc20c1a9ca4510ffec86bf16666f1fc50822321
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433865"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Outlook が Exchange キャッシュモードの場合にリモートサーバー上のストアにアクセスする
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、Microsoft Office Outlook が Exchange キャッシュモードの場合に、 **MAPI_NO_CACHE**フラグを使用してリモートサーバー上のメッセージストアでフォルダーまたはメッセージを開く方法を示す、C++ のコードサンプルを示します。 
  
Exchange キャッシュモードでは、outlook はユーザーのメールボックスのローカルコピーを使用して、リモート Exchange サーバー上のユーザーのメールボックスのリモートコピーへのオンライン接続を保持することができます。 Outlook が Exchange キャッシュモードで実行されている場合、既定では、同じセッションにログオンする MAPI ソリューションは、キャッシュされたメッセージストアにも接続されます。 アクセスされるデータと、変更が行われた場合は、メールボックスのローカルコピーに対して行われます。
  
クライアントまたはサービスプロバイダーは、ローカルメッセージストアへの接続を上書きし、 **[IMsgStore:: openentry](imsgstore-openentry.md)** を呼び出すときに*ulflags*パラメーターで**MAPI_NO_CACHE**のビットを設定することによって、リモートストア上のメッセージまたはフォルダーを開くことができます。 
  
次のコードサンプルは、 *ulflags*パラメーターに**MAPI_NO_CACHE**フラグを設定して**IMsgStore:: openentry**を呼び出して、リモートメッセージストアのルートフォルダーを開く方法を示しています。 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

リモートサーバーの**MDB_ONLINE**フラグを使用してメッセージストアを開いた場合、 **MAPI_NO_CACHE**フラグを使用する必要はありません。 
  
## <a name="see-also"></a>関連項目

- [MAPI の追加について](about-mapi-additions.md) 
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

