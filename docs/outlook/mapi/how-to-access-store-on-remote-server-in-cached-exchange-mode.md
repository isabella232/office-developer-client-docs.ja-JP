---
title: Outlook が Exchange キャッシュ モードではリモート サーバー上のストアにアクセスします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 8f1afd31f017b73fa5270d8fbf4c2a1c8fa08880
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800233"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Outlook が Exchange キャッシュ モードではリモート サーバー上のストアにアクセスします。
 
**適用対象**: Outlook 
  
このトピックには、 **MAPI_NO_CACHE**フラグを使用して Microsoft Office Outlook が Exchange キャッシュ モードではときに、フォルダーまたはリモート サーバー上のメッセージ ストアにメッセージを開く方法を示している C++ でのコード サンプルが含まれています。 
  
Exchange キャッシュ モードでは、Outlook ユーザーのメールボックスをリモートの Exchange サーバー上のリモート ・ コピーへのオンライン接続を維持するときに、ユーザーのメールボックスのローカル コピーを使用するように Outlook を許可します。 Outlook が既定では、Exchange キャッシュ モードで実行されている場合、同じセッションにログオンしている MAPI ソリューションでは、キャッシュされたメッセージ ストアに接続されています。 アクセスされているすべてのデータと加えられた変更は、メールボックスのローカル コピーに対して行われます。
  
クライアントまたはサービス プロバイダーは、ローカル メッセージ ストアへの接続をオーバーライドし、 **[IMsgStore::OpenEntry](imsgstore-openentry.md)** を呼び出すときは、 *ulFlags*パラメーターで**MAPI_NO_CACHE**のビットを設定することにより、メッセージまたはリモート ストア上のフォルダーを開きます。 
  
次のコード サンプルは、リモート メッセージ ストアのルート フォルダーを開く、 *ulFlags*パラメーターの設定**MAPI_NO_CACHE**フラグを使用して**IMsgStore::OpenEntry**を呼び出す方法を示しています。 
  
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

リモート サーバー上で**MDB_ONLINE**フラグを使用してメッセージ ・ ストアを開いた場合、 **MAPI_NO_CACHE**フラグを使用する必要はありません。 
  
## <a name="see-also"></a>関連項目

- [MAPI の追加について](about-mapi-additions.md)
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

