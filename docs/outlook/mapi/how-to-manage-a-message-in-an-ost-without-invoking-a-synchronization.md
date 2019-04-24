---
title: Exchange キャッシュモードで同期を呼び出すことなく OST でメッセージを管理する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: 'IMsgStore:: openentry で IID_IMessageRaw を使用して、クライアントが Exchange にキャッシュされているときに、メッセージ全体を強制的にダウンロードすることなく、オフラインフォルダーファイル (OST) 内のメッセージを管理する IMessage インターフェイスを取得する方法を示す C++ のコードサンプルが含まれています。荷.'
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316395"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Exchange キャッシュモードで同期を呼び出すことなく OST でメッセージを管理する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックには、 **[IMsgStore:: openentry](imsgstore-openentry.md)** での使用`IID_IMessageRaw`方法を示す C++ のコードサンプルが含まれています。これは、オフラインフォルダーファイル (OST) 内のメッセージを管理する**[IMessage](imessageimapiprop.md)** インターフェイスを取得するために、クライアントでのメッセージ全体のダウンロードを強制しません。Exchange キャッシュモードになっています。 
  
クライアントが Exchange キャッシュモードの場合、OST 内のメッセージは次の2つの状態のいずれかになります。
  
- ヘッダーと本文を含むメッセージ全体がダウンロードされます。
    
- ヘッダーのみが含まれるメッセージがダウンロードされます。
    
OST でメッセージの**IMessage**インターフェイスを要求し、クライアントが Exchange キャッシュモードの場合は、を使用`IID_IMessageRaw`します。 を使用`IID_IMessage`して**IMessage**インターフェイスを要求し、メッセージのヘッダーが OST にダウンロードされている場合は、メッセージ全体をダウンロードしようとする同期を呼び出します。 
  
または`IID_IMessage`を`IID_IMessageRaw`使用して**IMessage**インターフェイスを要求すると、返されるインターフェイスは同じように使用されます。 を**** 使用`IID_IMessageRaw`して要求した IMessage インターフェイスは、OST に存在する電子メールメッセージを返します。同期は強制されません。 
  
次の`IID_IMessage`例は、 **openentry**メソッドを呼び出す方法を示し`IID_IMessageRaw`ています。このメソッドは、ではなく渡されます。
  
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

**openentry**メソッドが**MAPI_E_INTERFACE_NOT_SUPPORTED**のエラーコードを返す場合は、メッセージストアが raw モードでのメッセージへのアクセスをサポートしていないことを示します。 このような場合は、を渡し`IID_IMessage`て**openentry**メソッドをもう一度試してください。

> [!IMPORTANT]
>  `IID_IMessageRaw`現在、ダウンロード可能なヘッダーファイルで定義されていない場合があります。 この場合は、次の定義を使用してコードに追加できます。 Microsoft Windows Software Development Kit (SDK) ヘッダーファイル guiddef で定義されている DEFINE_OLEGUID マクロを使用して、GUID シンボリック名とその値を関連付けます。 >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>関連項目

- [MAPI の追加について](about-mapi-additions.md) 
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

