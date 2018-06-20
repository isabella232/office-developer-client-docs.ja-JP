---
title: OST 内のメッセージを Exchange キャッシュ モードで同期を呼び出すことがなく管理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Exchange キャッシュ モードでは、クライアントと、メッセージ全体のダウンロードを強制することがなく IMsgStore::OpenEntry に IID_IMessageRaw を使用して、オフライン フォルダー ファイル (OST) でメッセージを管理している IMessage インターフェイスを取得する方法について説明する C++ のコード サンプルが含まれていますモードです。
ms.openlocfilehash: e32bf4f64bfb91979133ee983e45481b3d5b9732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800248"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>OST 内のメッセージを Exchange キャッシュ モードで同期を呼び出すことがなく管理します。

**適用されます**: Outlook 
  
このトピックには、c++ を使用する方法を示すコード サンプルが含まれています`IID_IMessageRaw`メッセージ全体のダウンロードを強制することがなく、オフライン フォルダー ファイル (OST) でメッセージを管理している**[IMessage](imessageimapiprop.md)** インターフェイスを取得するのには**[IMsgStore::OpenEntry](imsgstore-openentry.md)** で、クライアントExchange キャッシュ モードでは。 
  
クライアントは、Exchange キャッシュ モードでは、オフライン フォルダー ファイル内のメッセージは 2 つの状態のいずれかにできます。
  
- ヘッダーと本文を含むメッセージ全体がダウンロードされます。
    
- メッセージのヘッダーのみがダウンロードされます。
    
OST 内のメッセージの**IMessage**インターフェイスを要求すると、クライアントが Exchange キャッシュ モードを使用して、 `IID_IMessageRaw`。 使用する場合は、 `IID_IMessage` 、 **IMessage**インターフェイスを要求して、メッセージ全体をダウンロードしようとする同期を起動する場合は、OST にダウンロードされたヘッダーのみのメッセージには。 
  
使用する場合は、`IID_IMessageRaw`または`IID_IMessage` **IMessage**インターフェイスを要求するには返されたインターフェイスが使用中と同じです。 **IMessage**インターフェイスを使用して、要求された`IID_IMessageRaw`、オフライン フォルダー ファイル内に存在して、同期の必要はありません、電子メール メッセージが返されます。 
  
次の例は、 **OpenEntry**メソッドを呼び出す方法を示します`IID_IMessageRaw`の代わりに`IID_IMessage`。
  
```cpp
HRESULT HrOpenRawMessage ( 
    LPMDB lpMSB,  
    ULONG cbEntryID,  
    LPENTRYID lpEntryID,  
    ULONG ulFlags,  
    LPMESSAGE* lpMessage) 
{ 
    ULONG ulObjType = NULL; 
 
    HRESULT hRes = lpMDB->OpenEntry( 
        cbEntryID, 
        lpEntryID, 
        IID_IMessageRaw, 
        ulFlags, 
        &ulObjType, 
        (LPUNKNOWN*) lpMessage)); 
 
   return hRes; 
} 

```

**OpenEntry**メソッドでは、 **MAPI_E_INTERFACE_NOT_SUPPORTED**のエラー コードが返された場合は、メッセージ ・ ストアがサポートしていないこと、raw モードでメッセージにアクセスすることを示します。 このような場合は、再度実行してください**OpenEntry**メソッドを渡すことによって`IID_IMessage`。

> [!IMPORTANT]
>  `IID_IMessageRaw`現在あるダウンロード可能なヘッダー ファイルでない定義できます。 この例では、次の定義を使用してコードにそれを追加することができます。 GUID のシンボリック名をその値に関連付けるには、Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されている DEFINE_OLEGUID マクロを使用します。 >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>関連項目

- [MAPI の追加について](about-mapi-additions.md) 
- [Exchange キャッシュ モードでは、リモート サーバーと Outlook のストアのアクセス](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [ストアがリモート サーバーと Outlook の Exchange キャッシュ モードでは、開いています。](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

