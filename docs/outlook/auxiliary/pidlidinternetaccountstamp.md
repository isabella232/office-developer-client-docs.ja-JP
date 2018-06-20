---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: メッセージを配信するアカウントのアカウントのタイムスタンプを返します。
ms.openlocfilehash: ba54bffb60a05a3b4a1ff30519960740af93ebd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799552"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="40ab2-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="40ab2-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="40ab2-104">メッセージを配信するアカウントのアカウントのタイムスタンプを返します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="40ab2-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="40ab2-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40ab2-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="40ab2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="40ab2-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="40ab2-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="40ab2-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-108">Property set:</span></span>  <br/> |<span data-ttu-id="40ab2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="40ab2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="40ab2-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="40ab2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="40ab2-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="40ab2-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="40ab2-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-112">Data type:</span></span>  <br/> |<span data-ttu-id="40ab2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40ab2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="40ab2-114">領域:</span><span class="sxs-lookup"><span data-stu-id="40ab2-114">Area:</span></span>  <br/> |<span data-ttu-id="40ab2-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="40ab2-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40ab2-116">備考</span><span class="sxs-lookup"><span data-stu-id="40ab2-116">Remarks</span></span>

<span data-ttu-id="40ab2-117">このプロパティは、メッセージを配信しているアカウントについては、アカウント管理 API プロパティの[PROP_ACCT_STAMP](prop_acct_stamp.md)から返される値と同じ値を格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40ab2-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="40ab2-118">メッセージ ストア プロバイダーは、次のアクションが発生しないように、この名前付きプロパティと[PidLidInternetAccountName](pidlidinternetaccountname.md)を公開します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="40ab2-119">ユーザーをクリックしたとき **[全員へ返信**電子メール メッセージ、Outlook は、アカウントに関連付けられており、返信の受信者のリストからのメッセージにスタンプがあるメール アドレスを削除します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="40ab2-120">この現象は、この e メール アドレスが元のメッセージの送信者ではない場合、発生します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="40ab2-121">既定では、Outlook は、返信を送信し、元のメッセージの文字が印字されているアカウントを経由してメッセージを転送します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="40ab2-122">通常、Outlook プロトコル マネージャーが、メッセージを提供し、Outlook がメッセージを配信しているアカウントを示すために**PidLidInternetAccountName**と**PidLidInternetAccountStamp**のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="40ab2-123">ただし、メッセージ ストアは、トランスポートと密接に関連では、Outlook プロトコル マネージャーがメッセージを配信しませんし、Outlook は、これらのプロパティを設定できません。</span><span class="sxs-lookup"><span data-stu-id="40ab2-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="40ab2-124">このシナリオでは、Outlook は、 [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="40ab2-125">メッセージ ストア プロバイダーは、これらの名前付きプロパティを公開する必要がある場合は**IMAPIProp::GetIDsFromNames**を実装する必要があります、出力パラメーター *lppPropTags*をプロパティ タグを取得します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="40ab2-126">Outlook は、これらのプロパティ タグを使用して、 [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)メソッドを呼び出して、メッセージ ストア プロバイダーは、アカウント名と目的のアカウントのタイムスタンプを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="40ab2-126">Outlook can then call the [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="40ab2-127">ストア プロバイダーでは、これらの名前のプロパティをサポートするには、 **IMAPIProp::GetIDsFromNames**を使用して、このプロパティのプロパティ タグを取得するように Outlook が予想されます。</span><span class="sxs-lookup"><span data-stu-id="40ab2-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="40ab2-128">Outlook では、 **IMAPIProp::GetIDsFromNames**の入力パラメーター *lppPropNames*が指す配列の一部として渡されるこの名前のプロパティに対応する[MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="40ab2-128">Outlook specifies the following values for the [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40ab2-129">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="40ab2-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="40ab2-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="40ab2-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="40ab2-131">ulKind。</span><span class="sxs-lookup"><span data-stu-id="40ab2-131">ulKind:</span></span>  <br/> |<span data-ttu-id="40ab2-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="40ab2-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="40ab2-133">Kind.lID。</span><span class="sxs-lookup"><span data-stu-id="40ab2-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="40ab2-134">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="40ab2-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40ab2-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="40ab2-135">See also</span></span>

- [<span data-ttu-id="40ab2-136">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="40ab2-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="40ab2-137">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="40ab2-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="40ab2-138">PidLidInternetAccountStamp の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="40ab2-138">PidLidInternetAccountStamp Canonical Property</span></span>](http://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

