---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: メッセージを配信しているアカウントの表示名を返します。
ms.openlocfilehash: 2bd27cc7f868fb3f255a002ed70d0cb9b79516e3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393538"
---
# <a name="pidlidinternetaccountname"></a><span data-ttu-id="e7693-103">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="e7693-103">PidLidInternetAccountName</span></span>

<span data-ttu-id="e7693-104">メッセージを配信しているアカウントの表示名を返します。</span><span class="sxs-lookup"><span data-stu-id="e7693-104">Returns the display name of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e7693-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e7693-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7693-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e7693-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7693-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="e7693-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="e7693-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e7693-108">Property set:</span></span>  <br/> |<span data-ttu-id="e7693-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e7693-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e7693-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e7693-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e7693-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="e7693-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="e7693-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e7693-112">Data type:</span></span>  <br/> |<span data-ttu-id="e7693-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e7693-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e7693-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e7693-114">Area:</span></span>  <br/> |<span data-ttu-id="e7693-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="e7693-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7693-116">備考</span><span class="sxs-lookup"><span data-stu-id="e7693-116">Remarks</span></span>

<span data-ttu-id="e7693-117">このプロパティは、メッセージを配信しているアカウントについては、アカウント管理 API プロパティの[PROP_ACCT_NAME](prop_acct_name.md)から返される値と同じ値を格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7693-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_NAME](prop_acct_name.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="e7693-118">メッセージ ストア プロバイダーは、次のアクションが発生しないように、この名前付きプロパティと[PidLidInternetAccountStamp](pidlidinternetaccountstamp.md)を公開します。</span><span class="sxs-lookup"><span data-stu-id="e7693-118">Message store providers expose this named property and [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="e7693-119">ユーザーをクリックしたとき **[全員へ返信**電子メール メッセージ、Outlook は、アカウントに関連付けられており、返信の受信者のリストからのメッセージにスタンプがあるメール アドレスを削除します。</span><span class="sxs-lookup"><span data-stu-id="e7693-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="e7693-120">この現象は、この e メール アドレスが元のメッセージの送信者ではない場合、発生します。</span><span class="sxs-lookup"><span data-stu-id="e7693-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="e7693-121">既定では、Outlook は、返信を送信し、元のメッセージの文字が印字されているアカウントを経由してメッセージを転送します。</span><span class="sxs-lookup"><span data-stu-id="e7693-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="e7693-122">通常、Outlook プロトコル マネージャーが、メッセージを提供し、Outlook がメッセージを配信しているアカウントを示すために**PidLidInternetAccountName**と**PidLidInternetAccountStamp**のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e7693-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="e7693-123">ただし、メッセージ ストアは、トランスポートと密接に関連では、Outlook プロトコル マネージャーがメッセージを配信しませんし、Outlook は、これらのプロパティを設定できません。</span><span class="sxs-lookup"><span data-stu-id="e7693-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="e7693-124">このシナリオでは、Outlook は、 [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e7693-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="e7693-125">メッセージ ストア プロバイダーは、これらの名前付きプロパティを公開する必要がある場合は**IMAPIProp::GetIDsFromNames**を実装する必要があります、出力パラメーター *lppPropTags*をプロパティ タグを取得します。</span><span class="sxs-lookup"><span data-stu-id="e7693-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="e7693-126">Outlook は、これらのプロパティ タグを使用して、 [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)メソッドを呼び出して、メッセージ ストア プロバイダーは、アカウント名と目的のアカウントのタイムスタンプを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="e7693-126">Outlook can then call the [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="e7693-127">ストア プロバイダーでは、これらの名前のプロパティをサポートするには、 **IMAPIProp::GetIDsFromNames**を使用して、このプロパティのプロパティ タグを取得するように Outlook が予想されます。</span><span class="sxs-lookup"><span data-stu-id="e7693-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="e7693-128">Outlook では、 **IMAPIProp::GetIDsFromNames**の入力パラメーター *lppPropNames*が指す配列の一部として渡されるこの名前のプロパティに対応する[MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7693-128">Outlook specifies the following values for the [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7693-129">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="e7693-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="e7693-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e7693-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e7693-131">ulKind。</span><span class="sxs-lookup"><span data-stu-id="e7693-131">ulKind:</span></span>  <br/> |<span data-ttu-id="e7693-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="e7693-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="e7693-133">Kind.lID。</span><span class="sxs-lookup"><span data-stu-id="e7693-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="e7693-134">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="e7693-134">dispidInetAcctName</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7693-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7693-135">See also</span></span>

- [<span data-ttu-id="e7693-136">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="e7693-136">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="e7693-137">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="e7693-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="e7693-138">PidLidInternetAccountName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7693-138">PidLidInternetAccountName Canonical Property</span></span>](https://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

