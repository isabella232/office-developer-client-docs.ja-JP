---
title: キャッシュ モードの場合、リモート サーバー OutlookストアにExchangeする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: cfc20c1a9ca4510ffec86bf16666f1fc50822321
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433865"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>キャッシュ モードの場合、リモート サーバー OutlookストアにExchangeする
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは **、MAPI_NO_CACHE** フラグを使用して、Microsoft Office Outlook がキャッシュ Exchange モードのときにリモート サーバー上のメッセージ ストアでフォルダーまたはメッセージを開く方法を示す C++ のコード サンプルを示します。 
  
キャッシュ Exchange モードでは、Outlook はユーザーのメールボックスのローカル コピーを使用し、Outlook はリモート Exchange サーバー上のユーザーのメールボックスのリモート コピーへのオンライン接続を維持します。 キャッシュ Outlook Exchangeモードで実行されている場合、既定では、同じセッションにログオンする MAPI ソリューションもキャッシュされたメッセージ ストアに接続されます。 アクセスされるデータおよび変更は、メールボックスのローカル コピーに対して行います。
  
クライアントまたはサービス プロバイダーは **[、IMsgStore::OpenEntry](imsgstore-openentry.md)** を呼び出す際に *ulFlags* パラメーターで **MAPI_NO_CACHE** のビットを設定することにより、ローカル メッセージ ストアへの接続を上書きし、メッセージまたはリモート ストア上のフォルダーを開きます。 
  
次のコード サンプルは *、ulFlags* パラメーターで MAPI_NO_CACHE フラグが設定された **IMsgStore::OpenEntry** を呼び出して、リモート メッセージ ストアのルート フォルダーを開く方法を示しています。  
  
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

リモート サーバーで MDB_ONLINE フラグを **指定** してメッセージ ストアを開いた場合は、MAPI_NO_CACHEフラグ **を使用する必要** があります。 
  
## <a name="see-also"></a>関連項目

- [MAPI の追加について](about-mapi-additions.md) 
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

