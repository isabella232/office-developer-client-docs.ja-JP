---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: メッセージのプライマリ accountsendstamp を指定します。
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327707"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="bbb9a-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="bbb9a-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="bbb9a-104">メッセージのプライマリ アカウント "send" スタンプを指定します。</span><span class="sxs-lookup"><span data-stu-id="bbb9a-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bbb9a-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="bbb9a-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bbb9a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bbb9a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbb9a-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bbb9a-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="bbb9a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bbb9a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbb9a-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="bbb9a-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="bbb9a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bbb9a-110">Data type:</span></span>  <br/> |<span data-ttu-id="bbb9a-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bbb9a-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bbb9a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bbb9a-112">Area:</span></span>  <br/> |<span data-ttu-id="bbb9a-113">取引</span><span class="sxs-lookup"><span data-stu-id="bbb9a-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbb9a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bbb9a-114">Remarks</span></span>

<span data-ttu-id="bbb9a-115">このプロパティは、MAPI メッセージ オブジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="bbb9a-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="bbb9a-116">受信したメッセージの場合、プライマリ アカウントの "送信" スタンプは、転送するアカウントまたは返信を送信するアカウントを示します。</span><span class="sxs-lookup"><span data-stu-id="bbb9a-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="bbb9a-117">送信メッセージの場合、メッセージを送信するアカウントを決定します。</span><span class="sxs-lookup"><span data-stu-id="bbb9a-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="bbb9a-118">その値は [、PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) が送信されるアカウントの [IOlkAccount](iolkaccount.md) インターフェイスからの値です。</span><span class="sxs-lookup"><span data-stu-id="bbb9a-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bbb9a-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="bbb9a-119">See also</span></span>

- [<span data-ttu-id="bbb9a-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="bbb9a-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="bbb9a-121">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bbb9a-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="bbb9a-122">PidTagPrimarySendAccount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbb9a-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

