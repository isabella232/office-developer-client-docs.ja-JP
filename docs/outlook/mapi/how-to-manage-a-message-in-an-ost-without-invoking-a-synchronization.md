---
title: Exchange キャッシュ モードで同期を呼び出さずに OST でメッセージを管理する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: クライアントが Exchange キャッシュ モードのときにメッセージ全体をダウンロードせずに、オフライン フォルダー ファイル (OST) 内のメッセージを管理する IMessage インターフェイスを取得するために IMsgStore::OpenEntry で IID_IMessageRaw を使用する方法を示す C++ のコード サンプルが含まれています。
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418758"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Exchange キャッシュ モードで同期を呼び出さずに OST でメッセージを管理する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、クライアントが Exchange キャッシュ モードのときにメッセージ全体をダウンロードせずに、オフライン フォルダー ファイル (OST) 内のメッセージを管理する IMessage インターフェイスを取得するために `IID_IMessageRaw` **[IMsgStore::OpenEntry](imsgstore-openentry.md)****[](imessageimapiprop.md)** で使用する方法を示す C++ のコード サンプルを示します。 
  
クライアントが Exchange キャッシュ モードの場合、OST のメッセージは次の 2 つの状態の 1 つになります。
  
- ヘッダーと本文を含むメッセージ全体がダウンロードされます。
    
- ヘッダーのみを含むメッセージがダウンロードされます。
    
OST で **メッセージの IMessage** インターフェイスを要求し、クライアントが Exchange キャッシュ モードの場合は、 を使用します  `IID_IMessageRaw` 。 IMessage インターフェイスを要求するために使用し、メッセージのヘッダーだけが OST にダウンロードされている場合は、メッセージ全体をダウンロードしようとする同期 `IID_IMessage` を呼び出します。  
  
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
>  `IID_IMessageRaw` 現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。 この場合、次の定義を使用してコードに追加できます。 GUID 記号名DEFINE_OLEGUID関連付けるには、Microsoft Windows ソフトウェア開発キット (SDK) ヘッダー ファイル guiddef.h で定義されているコマンド マクロを使用します。 >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>関連項目

- [MAPI の追加について](about-mapi-additions.md) 
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

