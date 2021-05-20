---
title: サポート オブジェクトのアクセスと比較
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2b62f92325fcebf8cd3f0c86d28d98e7ff511ee2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429034"
---
# <a name="supporting-object-access-and-comparison"></a><span data-ttu-id="3b577-103">サポート オブジェクトのアクセスと比較</span><span class="sxs-lookup"><span data-stu-id="3b577-103">Supporting Object Access and Comparison</span></span>

  
  
<span data-ttu-id="3b577-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b577-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b577-105">サービス プロバイダーは [、IMAPISupport::OpenEntry](imapisupport-openentry.md) メソッドと [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) メソッドを使用して、プロバイダーまたは他のプロバイダーに属するオブジェクトを開いて比較できます。</span><span class="sxs-lookup"><span data-stu-id="3b577-105">Service providers can use the [IMAPISupport::OpenEntry](imapisupport-openentry.md) and [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) methods to open and compare objects that belong to their provider or to other providers:</span></span> 
  
<span data-ttu-id="3b577-106">[クライアントの IMAPISession::OpenEntry](imapisession-openentry.md)と同様に、プロバイダーはサポート オブジェクトの **OpenEntry** メソッドを使用して、オブジェクトのエントリ識別子を知っている限り、任意のオブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3b577-106">Like [IMAPISession::OpenEntry](imapisession-openentry.md) for clients, providers can use their support object's **OpenEntry** method to access any object as long they know the object's entry identifier.</span></span> <span data-ttu-id="3b577-107">セッション メソッドとは異なり、サポート メソッドでは  _、lpEntryID_ パラメーターに有効なエントリ識別子を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b577-107">Unlike the session method, the support method requires that you specify a valid entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="3b577-108">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="3b577-108">It cannot be NULL.</span></span> 
  
<span data-ttu-id="3b577-109">トランスポート プロバイダーが **IMAPISupport::OpenEntry** を使用する方法を説明するには、次のシナリオを検討してください。</span><span class="sxs-lookup"><span data-stu-id="3b577-109">To illustrate how a transport provider might use **IMAPISupport::OpenEntry**, consider the following scenario.</span></span> <span data-ttu-id="3b577-110">トランスポート プロバイダーはリッチ テキスト形式で書式設定されたメッセージを受信し、ターゲット受信者がこの形式を処理できるかどうかを知りません。</span><span class="sxs-lookup"><span data-stu-id="3b577-110">The transport provider has received a message formatted in Rich Text Format and does not know whether the target recipient can handle this format.</span></span> <span data-ttu-id="3b577-111">メッセージを配信する前に、トランスポート プロバイダーは次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b577-111">Before delivering the message, the transport provider needs to do the following:</span></span>
  
1. <span data-ttu-id="3b577-112">**メッセージ** の [IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出して、受信者テーブルと受信者のエントリ識別子 、その PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3b577-112">Call the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method to access the recipient table and the recipient's entry identifier, its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="3b577-113">エントリ識別子を **IMAPISupport::OpenEntry** に渡して、受信者 (通常はメッセージング ユーザーまたは配布リスト) を開きます。</span><span class="sxs-lookup"><span data-stu-id="3b577-113">Pass the entry identifier to **IMAPISupport::OpenEntry** to open the recipient, typically either a messaging user or distribution list.</span></span> <span data-ttu-id="3b577-114">プロバイダーが受信者のオブジェクトの種類を前もって知らないので  _、lpInterface_ パラメーターを NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b577-114">The  _lpInterface_ parameter should be set to NULL because the provider cannot know ahead of time the object type of the recipient.</span></span> <span data-ttu-id="3b577-115">サポート オブジェクトの **OpenEntry** メソッドは [IMAPISession::OpenEntry](imapisession-openentry.md) を呼び出して、受信者を担当するアドレス帳プロバイダーを決定します。</span><span class="sxs-lookup"><span data-stu-id="3b577-115">The support object's **OpenEntry** method calls [IMAPISession::OpenEntry](imapisession-openentry.md) to determine the address book provider responsible for the recipient.</span></span> <span data-ttu-id="3b577-116">セッション オブジェクトは、適切なアドレス帳プロバイダーの **OpenEntry** メソッドを呼び出して、受信者を開き、トランスポート プロバイダーへのインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="3b577-116">The session object then calls the appropriate address book provider's **OpenEntry** method to open the recipient and return an interface pointer to the transport provider.</span></span> 
    
3. <span data-ttu-id="3b577-117">受信者の [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_SEND_RICH_INFO **(** [PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="3b577-117">Call the recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="3b577-118">この **PR_SEND_RICH_INFO** TRUE に設定されている場合、受信者は書式設定されたテキストを処理できます。</span><span class="sxs-lookup"><span data-stu-id="3b577-118">If **PR_SEND_RICH_INFO** is set to TRUE, the recipient can handle formatted text.</span></span> 
    
<span data-ttu-id="3b577-119">他のプロバイダーから複数のオブジェクトを開いている場合は、2 つのエントリ識別子が同じオブジェクトを参照するかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b577-119">If you have opened several objects from other providers, you may need to find out whether two entry identifiers refer to the same object.</span></span> <span data-ttu-id="3b577-120">たとえば、短期エントリ識別子と長期エントリ識別子を持つ場合、これらの識別子は同じオブジェクトを識別する場合と識別できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="3b577-120">For example, you may have a short-term entry identifier and a long-term entry identifier and these identifiers may or may not identify the same object.</span></span> <span data-ttu-id="3b577-121">冗長処理を回避するには [、IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) メソッドを呼び出して、これらのエントリ識別子を比較します。</span><span class="sxs-lookup"><span data-stu-id="3b577-121">To avoid redundant processing, call the [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) method to compare these entry identifiers.</span></span> <span data-ttu-id="3b577-122">エントリ識別子を直接比較できないので、エントリ識別子の比較にはこのメソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b577-122">You must use this method for entry identifier comparison because entry identifiers cannot be compared directly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b577-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b577-123">See also</span></span>



[<span data-ttu-id="3b577-124">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3b577-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

