---
title: Exchange キャッシュモードで同期を呼び出すことなく OST でメッセージを管理する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: 'IMsgStore:: openentry で IID_IMessageRaw を使用して、クライアントが Exchange にキャッシュされているときに、メッセージ全体を強制的にダウンロードすることなく、オフラインフォルダーファイル (OST) 内のメッセージを管理する IMessage インターフェイスを取得する方法を示す C++ のコードサンプルが含まれています。荷.'
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418758"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="67c02-103">Exchange キャッシュモードで同期を呼び出すことなく OST でメッセージを管理する</span><span class="sxs-lookup"><span data-stu-id="67c02-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="67c02-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67c02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67c02-105">このトピックには、 **[IMsgStore:: openentry](imsgstore-openentry.md)** での使用`IID_IMessageRaw`方法を示す C++ のコードサンプルが含まれています。これは、オフラインフォルダーファイル (OST) 内のメッセージを管理する**[IMessage](imessageimapiprop.md)** インターフェイスを取得するために、クライアントでのメッセージ全体のダウンロードを強制しません。Exchange キャッシュモードになっています。</span><span class="sxs-lookup"><span data-stu-id="67c02-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="67c02-106">クライアントが Exchange キャッシュモードの場合、OST 内のメッセージは次の2つの状態のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="67c02-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="67c02-107">ヘッダーと本文を含むメッセージ全体がダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="67c02-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="67c02-108">ヘッダーのみが含まれるメッセージがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="67c02-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="67c02-109">OST でメッセージの**IMessage**インターフェイスを要求し、クライアントが Exchange キャッシュモードの場合は、を使用`IID_IMessageRaw`します。</span><span class="sxs-lookup"><span data-stu-id="67c02-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="67c02-110">を使用`IID_IMessage`して**IMessage**インターフェイスを要求し、メッセージのヘッダーが OST にダウンロードされている場合は、メッセージ全体をダウンロードしようとする同期を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="67c02-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="67c02-111">または`IID_IMessage`を`IID_IMessageRaw`使用して**IMessage**インターフェイスを要求すると、返されるインターフェイスは同じように使用されます。</span><span class="sxs-lookup"><span data-stu-id="67c02-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="67c02-112">を\*\*\*\* 使用`IID_IMessageRaw`して要求した IMessage インターフェイスは、OST に存在する電子メールメッセージを返します。同期は強制されません。</span><span class="sxs-lookup"><span data-stu-id="67c02-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="67c02-113">次の`IID_IMessage`例は、 **openentry**メソッドを呼び出す方法を示し`IID_IMessageRaw`ています。このメソッドは、ではなく渡されます。</span><span class="sxs-lookup"><span data-stu-id="67c02-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="67c02-114">**openentry**メソッドが**MAPI_E_INTERFACE_NOT_SUPPORTED**のエラーコードを返す場合は、メッセージストアが raw モードでのメッセージへのアクセスをサポートしていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="67c02-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="67c02-115">このような場合は、を渡し`IID_IMessage`て**openentry**メソッドをもう一度試してください。</span><span class="sxs-lookup"><span data-stu-id="67c02-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="67c02-116">`IID_IMessageRaw`現在、ダウンロード可能なヘッダーファイルで定義されていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="67c02-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="67c02-117">この場合は、次の定義を使用してコードに追加できます。</span><span class="sxs-lookup"><span data-stu-id="67c02-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="67c02-118">Microsoft Windows Software Development Kit (SDK) ヘッダーファイル guiddef で定義されている DEFINE_OLEGUID マクロを使用して、GUID シンボリック名とその値を関連付けます。</span><span class="sxs-lookup"><span data-stu-id="67c02-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="67c02-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="67c02-119">See also</span></span>

- [<span data-ttu-id="67c02-120">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="67c02-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="67c02-121">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする</span><span class="sxs-lookup"><span data-stu-id="67c02-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="67c02-122">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く</span><span class="sxs-lookup"><span data-stu-id="67c02-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

