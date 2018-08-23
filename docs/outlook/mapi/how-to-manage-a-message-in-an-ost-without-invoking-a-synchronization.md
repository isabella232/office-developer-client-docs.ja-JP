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
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="b92d2-103">OST 内のメッセージを Exchange キャッシュ モードで同期を呼び出すことがなく管理します。</span><span class="sxs-lookup"><span data-stu-id="b92d2-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="b92d2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b92d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b92d2-105">このトピックには、c++ を使用する方法を示すコード サンプルが含まれています`IID_IMessageRaw`メッセージ全体のダウンロードを強制することがなく、オフライン フォルダー ファイル (OST) でメッセージを管理している**[IMessage](imessageimapiprop.md)** インターフェイスを取得するのには**[IMsgStore::OpenEntry](imsgstore-openentry.md)** で、クライアントExchange キャッシュ モードでは。</span><span class="sxs-lookup"><span data-stu-id="b92d2-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="b92d2-106">クライアントは、Exchange キャッシュ モードでは、オフライン フォルダー ファイル内のメッセージは 2 つの状態のいずれかにできます。</span><span class="sxs-lookup"><span data-stu-id="b92d2-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="b92d2-107">ヘッダーと本文を含むメッセージ全体がダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="b92d2-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="b92d2-108">メッセージのヘッダーのみがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="b92d2-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="b92d2-109">OST 内のメッセージの**IMessage**インターフェイスを要求すると、クライアントが Exchange キャッシュ モードを使用して、 `IID_IMessageRaw`。</span><span class="sxs-lookup"><span data-stu-id="b92d2-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="b92d2-110">使用する場合は、 `IID_IMessage` 、 **IMessage**インターフェイスを要求して、メッセージ全体をダウンロードしようとする同期を起動する場合は、OST にダウンロードされたヘッダーのみのメッセージには。</span><span class="sxs-lookup"><span data-stu-id="b92d2-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="b92d2-111">使用する場合は、`IID_IMessageRaw`または`IID_IMessage` **IMessage**インターフェイスを要求するには返されたインターフェイスが使用中と同じです。</span><span class="sxs-lookup"><span data-stu-id="b92d2-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="b92d2-112">**IMessage**インターフェイスを使用して、要求された`IID_IMessageRaw`、オフライン フォルダー ファイル内に存在して、同期の必要はありません、電子メール メッセージが返されます。</span><span class="sxs-lookup"><span data-stu-id="b92d2-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="b92d2-113">次の例は、 **OpenEntry**メソッドを呼び出す方法を示します`IID_IMessageRaw`の代わりに`IID_IMessage`。</span><span class="sxs-lookup"><span data-stu-id="b92d2-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="b92d2-114">**OpenEntry**メソッドでは、 **MAPI_E_INTERFACE_NOT_SUPPORTED**のエラー コードが返された場合は、メッセージ ・ ストアがサポートしていないこと、raw モードでメッセージにアクセスすることを示します。</span><span class="sxs-lookup"><span data-stu-id="b92d2-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="b92d2-115">このような場合は、再度実行してください**OpenEntry**メソッドを渡すことによって`IID_IMessage`。</span><span class="sxs-lookup"><span data-stu-id="b92d2-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="b92d2-116">`IID_IMessageRaw`現在あるダウンロード可能なヘッダー ファイルでない定義できます。</span><span class="sxs-lookup"><span data-stu-id="b92d2-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="b92d2-117">この例では、次の定義を使用してコードにそれを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b92d2-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="b92d2-118">GUID のシンボリック名をその値に関連付けるには、Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されている DEFINE_OLEGUID マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="b92d2-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="b92d2-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="b92d2-119">See also</span></span>

- [<span data-ttu-id="b92d2-120">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="b92d2-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="b92d2-121">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする</span><span class="sxs-lookup"><span data-stu-id="b92d2-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="b92d2-122">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く</span><span class="sxs-lookup"><span data-stu-id="b92d2-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

