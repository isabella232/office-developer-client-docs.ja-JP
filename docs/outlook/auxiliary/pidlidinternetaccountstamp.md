---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: メッセージを配信したアカウントのアカウント スタンプを返します。
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327728"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="cb2c8-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="cb2c8-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="cb2c8-104">メッセージを配信したアカウントのアカウント スタンプを返します。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cb2c8-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="cb2c8-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb2c8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cb2c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb2c8-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="cb2c8-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="cb2c8-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="cb2c8-108">Property set:</span></span>  <br/> |<span data-ttu-id="cb2c8-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="cb2c8-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="cb2c8-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="cb2c8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cb2c8-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="cb2c8-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="cb2c8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cb2c8-112">Data type:</span></span>  <br/> |<span data-ttu-id="cb2c8-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cb2c8-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cb2c8-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="cb2c8-114">Area:</span></span>  <br/> |<span data-ttu-id="cb2c8-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="cb2c8-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb2c8-116">注釈</span><span class="sxs-lookup"><span data-stu-id="cb2c8-116">Remarks</span></span>

<span data-ttu-id="cb2c8-117">このプロパティには、メッセージを配信したアカウントの Account Management API プロパティ [PROP_ACCT_STAMP同じ](prop_acct_stamp.md) 値を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="cb2c8-118">メッセージ ストア プロバイダーは、この名前付きプロパティと [PidLidInternetAccountName](pidlidinternetaccountname.md) を公開して、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="cb2c8-119">ユーザーが電子メールメッセージで [全員に返信] をクリックすると、Outlook はアカウントに関連付けられている電子メール アドレスを削除し、返信の受信者リストからメッセージにスタンプされます。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="cb2c8-120">この動作は、この電子メール アドレスが元のメッセージの送信者である場合を使用しない限り発生します。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="cb2c8-121">既定では、Outlookメッセージにスタンプされたアカウントを通じて返信メッセージと転送メッセージが送信されます。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="cb2c8-122">通常、Outlook プロトコル マネージャーはメッセージを配信し、Outlook は **PidLidInternetAccountName** プロパティと **PidLidInternetAccountStamp** プロパティを設定して、メッセージを配信したアカウントを示します。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="cb2c8-123">ただし、メッセージ ストアがトランスポートと緊密に結合されている場合、Outlook プロトコル マネージャーはメッセージを配信し、Outlookプロパティを設定できません。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="cb2c8-124">このシナリオでは、Outlook [IMAPIProp::GetIDsFromNames 関数を呼び出](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)します。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="cb2c8-125">メッセージ ストア プロバイダーがこれらの名前付きプロパティを公開する場合は **、IMAPIProp::GetIDsFromNames** を実装し、出力パラメーター  *lppPropTags*  を使用してプロパティ タグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="cb2c8-126">Outlookこれらのプロパティ タグを使用して[IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)メソッドを呼び出し、メッセージ ストア プロバイダーは目的のアカウントのアカウント名とスタンプを返します。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="cb2c8-127">これらの名前付きプロパティをサポートするために、ストア プロバイダーは、Outlook プロパティのプロパティ タグを取得するために **IMAPIProp::GetIDsFromNames** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="cb2c8-128">Outlookは **、IMAPIProp::GetIDsFromNames** の入力パラメーター *lppPropNames* によって示される配列の一部として渡される、この名前付きプロパティに対応する [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb2c8-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb2c8-129">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="cb2c8-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="cb2c8-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="cb2c8-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="cb2c8-131">ulKind:</span><span class="sxs-lookup"><span data-stu-id="cb2c8-131">ulKind:</span></span>  <br/> |<span data-ttu-id="cb2c8-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="cb2c8-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="cb2c8-133">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="cb2c8-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="cb2c8-134">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="cb2c8-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb2c8-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="cb2c8-135">See also</span></span>

- [<span data-ttu-id="cb2c8-136">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="cb2c8-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="cb2c8-137">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="cb2c8-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="cb2c8-138">PidLidInternetAccountStamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cb2c8-138">PidLidInternetAccountStamp Canonical Property</span></span>](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

