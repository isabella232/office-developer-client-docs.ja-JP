---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: メッセージを配信したアカウントのアカウントスタンプを返します。
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327728"
---
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="37643-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="37643-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="37643-104">メッセージを配信したアカウントのアカウントスタンプを返します。</span><span class="sxs-lookup"><span data-stu-id="37643-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="37643-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="37643-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37643-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="37643-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37643-107">dispidinetacctstamp</span><span class="sxs-lookup"><span data-stu-id="37643-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="37643-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="37643-108">Property set:</span></span>  <br/> |<span data-ttu-id="37643-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="37643-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="37643-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="37643-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="37643-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="37643-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="37643-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="37643-112">Data type:</span></span>  <br/> |<span data-ttu-id="37643-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="37643-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="37643-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="37643-114">Area:</span></span>  <br/> |<span data-ttu-id="37643-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="37643-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37643-116">解説</span><span class="sxs-lookup"><span data-stu-id="37643-116">Remarks</span></span>

<span data-ttu-id="37643-117">このプロパティには、メッセージを配信したアカウントのアカウント管理 API プロパティ[PROP_ACCT_STAMP](prop_acct_stamp.md)から返されるものと同じ値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37643-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="37643-118">メッセージストアプロバイダーは、この名前付きプロパティと[PidLidInternetAccountName](pidlidinternetaccountname.md)を公開して、次のアクションが実行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="37643-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="37643-119">ユーザーが電子メールメッセージで [**全員へ返信**] をクリックすると、Outlook はそのアカウントに関連付けられている電子メールアドレスを削除し、返信の受信者リストからメッセージにスタンプされます。</span><span class="sxs-lookup"><span data-stu-id="37643-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="37643-120">この動作は、この電子メールアドレスが元のメッセージの送信者ではない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="37643-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="37643-121">既定では、Outlook は、元のメッセージにスタンプされているアカウントを使用して、返信メッセージと転送メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="37643-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="37643-122">通常、outlook プロトコルマネージャーはメッセージを配信し、outlook は**PidLidInternetAccountName**および**PidLidInternetAccountStamp**プロパティを設定して、メッセージを配信したアカウントを示します。</span><span class="sxs-lookup"><span data-stu-id="37643-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="37643-123">ただし、メッセージストアがトランスポートと密に結合されている場合、outlook プロトコルマネージャーはメッセージを配信しないため、outlook はこれらのプロパティを設定できません。</span><span class="sxs-lookup"><span data-stu-id="37643-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="37643-124">このシナリオでは、Outlook は[imapiprop:: getidsfromnames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="37643-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="37643-125">メッセージストアプロバイダーがこれらの名前付きプロパティを公開する場合は、出力パラメーター *lppproptags*を使用して**imapiprop:: getidsfromnames**を実装し、プロパティタグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="37643-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="37643-126">その後、Outlook は、これらのプロパティタグを使用して[imapiprop:: GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)メソッドを呼び出すことができ、メッセージストアプロバイダーは必要なアカウントのアカウント名とスタンプを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="37643-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="37643-127">このような名前付きプロパティをサポートするには、ストアプロバイダーが**imapiprop:: getidsfromnames**を使用して、このプロパティのプロパティタグを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37643-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="37643-128">Outlook では、この名前付きプロパティに対応する[mapinameid](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx)構造体の次の値が指定されています。この名前は、入力パラメーター *lpppropnames の名前*によって示される配列の一部として渡されます。 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="37643-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37643-129">lpguid:</span><span class="sxs-lookup"><span data-stu-id="37643-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="37643-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="37643-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="37643-131">ulkind:</span><span class="sxs-lookup"><span data-stu-id="37643-131">ulKind:</span></span>  <br/> |<span data-ttu-id="37643-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="37643-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="37643-133">ふたの種類:</span><span class="sxs-lookup"><span data-stu-id="37643-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="37643-134">dispidinetacctstamp</span><span class="sxs-lookup"><span data-stu-id="37643-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37643-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="37643-135">See also</span></span>

- [<span data-ttu-id="37643-136">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="37643-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="37643-137">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="37643-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="37643-138">PidLidInternetAccountStamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="37643-138">PidLidInternetAccountStamp Canonical Property</span></span>](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

