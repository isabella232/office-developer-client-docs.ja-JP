---
title: キャッシュ モードで同期を呼び出さずに OST でExchangeする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: C++ のコード サンプルを含み、IMsgStore::OpenEntry で IID_IMessageRaw を使用して、クライアントがキャッシュ Exchange モードのときにメッセージ全体をダウンロードすることなく、オフライン フォルダー ファイル (OST) 内のメッセージを管理する IMessage インターフェイスを取得する方法を示します。
ms.openlocfilehash: e78743e6e84293d6507762380ac9b1952e420dd7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614074"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>キャッシュ モードで同期を呼び出さずに OST でExchangeする

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、クライアントがキャッシュ Exchange モードのときにメッセージ全体をダウンロードせずに、オフライン フォルダー ファイル (OST) 内のメッセージを管理する IMessage インターフェイスを取得するために `IID_IMessageRaw` **[IMsgStore::OpenEntry](imsgstore-openentry.md)****[](imessageimapiprop.md)** で使用する方法を示す C++ のコード サンプルを示します。 
  
クライアントがキャッシュ モードExchange、OST 内のメッセージは次の 2 つの状態の 1 つになります。
  
- ヘッダーと本文を含むメッセージ全体がダウンロードされます。
    
- ヘッダーのみを含むメッセージがダウンロードされます。
    
OST で **メッセージの IMessage** インターフェイスを要求し、クライアントがキャッシュ モードの場合は、Exchangeを使用します `IID_IMessageRaw` 。 IMessage インターフェイスを要求するために使用し、メッセージのヘッダーだけが OST にダウンロードされている場合は、メッセージ全体をダウンロードしようとする同期 `IID_IMessage` を呼び出します。  
  
IMessage インターフェイスを使用または要求する場合、返されるインターフェイスは使用 `IID_IMessageRaw` `IID_IMessage` されているインターフェイスと同じです。  使用 **して要求された IMessage** インターフェイスは、OST に存在する電子メール メッセージを返し、同期  `IID_IMessageRaw` は強制されません。 
  
次の例は、 の代わりに **OpenEntry メソッドを呼** び出す  `IID_IMessageRaw` 方法を示しています  `IID_IMessage` 。
  
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

**OpenEntry** メソッドがエラー コードMAPI_E_INTERFACE_NOT_SUPPORTED返す場合、メッセージ ストアが生モードでメッセージへのアクセスをサポートしていないかどうかを示します。 この状況では、渡して **OpenEntry** メソッドを再度試してください  `IID_IMessage` 。

> [!IMPORTANT]
>  `IID_IMessageRaw` 現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。 この場合、次の定義を使用してコードに追加できます。 Windows Microsoft DEFINE_OLEGUID ソフトウェア開発キット (SDK) ヘッダー ファイル guiddef.h で定義されている DEFINE_OLEGUID マクロを使用して、GUID 記号名をその値に関連付ける。 >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>関連項目

- [MAPI の追加について](about-mapi-additions.md) 
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

