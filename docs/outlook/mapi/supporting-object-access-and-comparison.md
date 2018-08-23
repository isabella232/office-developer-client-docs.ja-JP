---
title: オブジェクトのアクセスと比較のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f33dcedae5ffe30b85a58d5248d239be81c8efc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575282"
---
# <a name="supporting-object-access-and-comparison"></a><span data-ttu-id="c31c9-103">オブジェクトのアクセスと比較のサポート</span><span class="sxs-lookup"><span data-stu-id="c31c9-103">Supporting Object Access and Comparison</span></span>

  
  
<span data-ttu-id="c31c9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c31c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c31c9-105">サービス プロバイダーでは、開くし、プロバイダーやその他のプロバイダーに属しているオブジェクトを比較する、 [IMAPISupport::OpenEntry](imapisupport-openentry.md)メソッドと[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c31c9-105">Service providers can use the [IMAPISupport::OpenEntry](imapisupport-openentry.md) and [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) methods to open and compare objects that belong to their provider or to other providers:</span></span> 
  
<span data-ttu-id="c31c9-106">クライアントの[IMAPISession::OpenEntry](imapisession-openentry.md)をのようなプロバイダーは、オブジェクトのエントリ id を知っている、長い間の任意のオブジェクトにアクセスするためのサポート オブジェクトの**OpenEntry**メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c31c9-106">Like [IMAPISession::OpenEntry](imapisession-openentry.md) for clients, providers can use their support object's **OpenEntry** method to access any object as long they know the object's entry identifier.</span></span> <span data-ttu-id="c31c9-107">サポート メソッドでは、セッション メソッドとは異なり、 _lpEntryID_パラメーターに有効なエントリの識別子を指定することが必要です。</span><span class="sxs-lookup"><span data-stu-id="c31c9-107">Unlike the session method, the support method requires that you specify a valid entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="c31c9-108">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c31c9-108">It cannot be NULL.</span></span> 
  
<span data-ttu-id="c31c9-109">トランスポート プロバイダーが**IMAPISupport::OpenEntry**を使用する方法を示すためには、次のシナリオを検討します。</span><span class="sxs-lookup"><span data-stu-id="c31c9-109">To illustrate how a transport provider might use **IMAPISupport::OpenEntry**, consider the following scenario.</span></span> <span data-ttu-id="c31c9-110">トランスポート プロバイダーは、リッチ テキスト形式で書式設定されたメッセージを受信しましたが、対象の受信者がこの形式を処理できるかどうかがわからない</span><span class="sxs-lookup"><span data-stu-id="c31c9-110">The transport provider has received a message formatted in Rich Text Format and does not know whether the target recipient can handle this format.</span></span> <span data-ttu-id="c31c9-111">メッセージを配信する前にトランスポート プロバイダーは、次の操作を必要があります。</span><span class="sxs-lookup"><span data-stu-id="c31c9-111">Before delivering the message, the transport provider needs to do the following:</span></span>
  
1. <span data-ttu-id="c31c9-112">受信者と受信者のエントリの識別子、その**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティにアクセスするためのメッセージの[IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c31c9-112">Call the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method to access the recipient table and the recipient's entry identifier, its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="c31c9-113">開くには、受信者は、通常、 **IMAPISupport::OpenEntry**にメッセージのユーザーまたは配布リストに対応するエントリの識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="c31c9-113">Pass the entry identifier to **IMAPISupport::OpenEntry** to open the recipient, typically either a messaging user or distribution list.</span></span> <span data-ttu-id="c31c9-114">プロバイダーできませんを事前に確認、受信者のオブジェクト タイプであるために、 _lpInterface_パラメーターを NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c31c9-114">The  _lpInterface_ parameter should be set to NULL because the provider cannot know ahead of time the object type of the recipient.</span></span> <span data-ttu-id="c31c9-115">サポート オブジェクトの**OpenEntry**メソッドでは、受信者のアドレス帳プロバイダーを確認するのには[IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c31c9-115">The support object's **OpenEntry** method calls [IMAPISession::OpenEntry](imapisession-openentry.md) to determine the address book provider responsible for the recipient.</span></span> <span data-ttu-id="c31c9-116">セッション オブジェクト、メソッドを呼び出して適切なアドレス帳プロバイダーの**OpenEntry**受信者を開き、トランスポート プロバイダーへのインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="c31c9-116">The session object then calls the appropriate address book provider's **OpenEntry** method to open the recipient and return an interface pointer to the transport provider.</span></span> 
    
3. <span data-ttu-id="c31c9-117">**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティを取得するために、受信者の[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c31c9-117">Call the recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="c31c9-118">**PR_SEND_RICH_INFO**を TRUE に設定すると、受信者が書式設定されたテキストを処理できます。</span><span class="sxs-lookup"><span data-stu-id="c31c9-118">If **PR_SEND_RICH_INFO** is set to TRUE, the recipient can handle formatted text.</span></span> 
    
<span data-ttu-id="c31c9-119">他のプロバイダーから複数のオブジェクトを開いた場合は、2 つのエントリ id が同じオブジェクトを参照するかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c31c9-119">If you have opened several objects from other providers, you may need to find out whether two entry identifiers refer to the same object.</span></span> <span data-ttu-id="c31c9-120">などの短期的なエントリ id がある場合があり、長期のエントリ id とこれらの識別子は、同じオブジェクトを識別しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="c31c9-120">For example, you may have a short-term entry identifier and a long-term entry identifier and these identifiers may or may not identify the same object.</span></span> <span data-ttu-id="c31c9-121">冗長な処理を避けるためには、これらのエントリ id を比較する[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c31c9-121">To avoid redundant processing, call the [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) method to compare these entry identifiers.</span></span> <span data-ttu-id="c31c9-122">エントリ id を直接比較できないためには、エントリの識別子の比較のためこのメソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c31c9-122">You must use this method for entry identifier comparison because entry identifiers cannot be compared directly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c31c9-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c31c9-123">See also</span></span>



[<span data-ttu-id="c31c9-124">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c31c9-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

