---
title: メッセージ ストアのメッセージの作成と保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7c923a330c542dff8b1bbc476461ccd21680a5b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332901"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="4f695-103">メッセージ ストアのメッセージの作成と保存</span><span class="sxs-lookup"><span data-stu-id="4f695-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="4f695-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f695-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f695-p101">メッセージ ストア プロバイダーが基盤となるストレージ メカニズムでメッセージの作成と保存を行う方法は、基盤となるストレージ メカニズムそのものに大きく依存します。一般的には、メッセージとその値のプロパティを保存するためのコードを記述するだけです。</span><span class="sxs-lookup"><span data-stu-id="4f695-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="4f695-p102">メッセージ ストア プロバイダーが新しいメッセージを作成するときは、メッセージに必要なプロパティを付けてメッセージを作成する必要があります。これらのプロパティ一覧は、[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) インターフェイスの文書に記載されています。その後、クライアント アプリケーションが、[IMAPIProp](imapipropiunknown.md) メソッドを使ってすべての追加プロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f695-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="4f695-110">メッセージ ストア プロバイダーが基盤となるストレージ メカニズムにメッセージを保存するときは、メッセージのプロパティを繰り返し処理して、基盤となるストレージ メカニズムに保存する必要があります。そうすることで、後で開いたときにメッセージが完全な形で復元されます。</span><span class="sxs-lookup"><span data-stu-id="4f695-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="4f695-p103">MAPI は [IMessage](imessageimapiprop.md) インターフェイス上のプロパティのトランザクションを要求します。つまり、プロパティに加えられた変更は、[IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドがメッセージ オブジェクトに対して呼び出されるまでは永続的になりません。メッセージ ストア プロバイダーには、この動作を実装する責任があります。通常、これは難しくありません。つまり、プロパティが変更されている間、プロパティをメモリに保持し、**SaveChanges** が呼び出されたときに、基盤となるストレージ メカニズムにコミットすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="4f695-p103">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="4f695-114">メッセージ オブジェクトのプロパティの中には、次に示すとおり、**SaveChanges** メソッドに関して、クライアント アプリケーションに対する特別なセマンティクスを持つものがあります。</span><span class="sxs-lookup"><span data-stu-id="4f695-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="4f695-115">一部のプロパティは、**SaveChanges** が呼び出される前に読み取り/書き込みが行われる必要がありますが、その後は読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="4f695-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="4f695-116">たとえば、メッセージを作成する (つまり読み取り/書き込みである) クライアント アプリケーションによって、当初、**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) が設定されていても、いったん **SaveChanges** の呼び出しがあってからは変更できません。</span><span class="sxs-lookup"><span data-stu-id="4f695-116">For example, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="4f695-p105">一部のプロパティは、自らの属するフォルダーのプロパティ、または **IMAPIFolder** メソッドとの間で特別な関係を持っています。たとえば、**PR_MESSAGE_FLAGS** プロパティは、[IMAPIFolder::CreateMessage](imapifolder-createmessage.md) の呼び出しに使用されるフラグと関連があります。</span><span class="sxs-lookup"><span data-stu-id="4f695-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="4f695-119">一部のプロパティは、**SaveChanges** が初めて呼び出されるまで使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="4f695-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="4f695-120">たとえば、**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティは **SaveChanges** が初めて呼び出されるまで使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="4f695-120">For example, the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="4f695-121">一部のプロパティは、メッセージ オブジェクトのその他のプロパティと特別な関係を持っています。</span><span class="sxs-lookup"><span data-stu-id="4f695-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="4f695-122">たとえば、**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティは、通常、リッチ テキスト形式のメッセージをサポートするメッセージ ストア プロバイダーの **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティから派生します。</span><span class="sxs-lookup"><span data-stu-id="4f695-122">For example, the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="4f695-123">一部のプロパティは、メッセージ ストアに関連する複数のオブジェクト型で使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f695-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="4f695-124">たとえば、**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティは、フォルダーでも、メッセージ オブジェクトでも、さらにはメッセージ ストア オブジェクトでも必要です。</span><span class="sxs-lookup"><span data-stu-id="4f695-124">For example, the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="4f695-125">メッセージ ストア プロバイダーには、このようなプロパティに対する適切なセマンティクスを実装する責任があります。</span><span class="sxs-lookup"><span data-stu-id="4f695-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4f695-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f695-126">See also</span></span>



[<span data-ttu-id="4f695-127">メッセージ ストアのメッセージの実装</span><span class="sxs-lookup"><span data-stu-id="4f695-127">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

