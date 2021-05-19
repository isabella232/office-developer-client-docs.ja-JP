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
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="264d2-103">Exchange キャッシュ モードで同期を呼び出さずに OST でメッセージを管理する</span><span class="sxs-lookup"><span data-stu-id="264d2-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="264d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="264d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="264d2-105">このトピックでは、クライアントが Exchange キャッシュ モードのときにメッセージ全体をダウンロードせずに、オフライン フォルダー ファイル (OST) 内のメッセージを管理する IMessage インターフェイスを取得するために `IID_IMessageRaw` **[IMsgStore::OpenEntry](imsgstore-openentry.md)\*\*\*\*[](imessageimapiprop.md)** で使用する方法を示す C++ のコード サンプルを示します。</span><span class="sxs-lookup"><span data-stu-id="264d2-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="264d2-106">クライアントが Exchange キャッシュ モードの場合、OST のメッセージは次の 2 つの状態の 1 つになります。</span><span class="sxs-lookup"><span data-stu-id="264d2-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="264d2-107">ヘッダーと本文を含むメッセージ全体がダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="264d2-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="264d2-108">ヘッダーのみを含むメッセージがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="264d2-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="264d2-109">OST で **メッセージの IMessage** インターフェイスを要求し、クライアントが Exchange キャッシュ モードの場合は、 を使用します  `IID_IMessageRaw` 。</span><span class="sxs-lookup"><span data-stu-id="264d2-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="264d2-110">IMessage インターフェイスを要求するために使用し、メッセージのヘッダーだけが OST にダウンロードされている場合は、メッセージ全体をダウンロードしようとする同期 `IID_IMessage` を呼び出します。 </span><span class="sxs-lookup"><span data-stu-id="264d2-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="264d2-111">IMessage インターフェイスを使用または要求する場合、返されるインターフェイスは使用 `IID_IMessageRaw` `IID_IMessage` されているインターフェイスと同じです。 </span><span class="sxs-lookup"><span data-stu-id="264d2-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="264d2-112">使用 **して要求された IMessage** インターフェイスは、OST に存在する電子メール メッセージを返し、同期  `IID_IMessageRaw` は強制されません。</span><span class="sxs-lookup"><span data-stu-id="264d2-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="264d2-113">次の例は、 の代わりに **OpenEntry メソッドを呼** び出す  `IID_IMessageRaw` 方法を示しています  `IID_IMessage` 。</span><span class="sxs-lookup"><span data-stu-id="264d2-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="264d2-114">**OpenEntry** メソッドがエラー コードMAPI_E_INTERFACE_NOT_SUPPORTED返す場合、メッセージ ストアが生モードでメッセージへのアクセスをサポートしていないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="264d2-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="264d2-115">この状況では、渡して **OpenEntry** メソッドを再度試してください  `IID_IMessage` 。</span><span class="sxs-lookup"><span data-stu-id="264d2-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="264d2-116">`IID_IMessageRaw` 現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="264d2-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="264d2-117">この場合、次の定義を使用してコードに追加できます。</span><span class="sxs-lookup"><span data-stu-id="264d2-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="264d2-118">GUID 記号名DEFINE_OLEGUID関連付けるには、Microsoft Windows ソフトウェア開発キット (SDK) ヘッダー ファイル guiddef.h で定義されているコマンド マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="264d2-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="264d2-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="264d2-119">See also</span></span>

- [<span data-ttu-id="264d2-120">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="264d2-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="264d2-121">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする</span><span class="sxs-lookup"><span data-stu-id="264d2-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="264d2-122">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く</span><span class="sxs-lookup"><span data-stu-id="264d2-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

