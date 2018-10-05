---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: メッセージの主要な accountsendstamp を指定します。
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394085"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="67574-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="67574-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="67574-104">メッセージをプライマリ アカウントの「送信」スタンプを指定します。</span><span class="sxs-lookup"><span data-stu-id="67574-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="67574-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="67574-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67574-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="67574-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67574-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="67574-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="67574-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="67574-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67574-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="67574-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="67574-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="67574-110">Data type:</span></span>  <br/> |<span data-ttu-id="67574-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="67574-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="67574-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="67574-112">Area:</span></span>  <br/> |<span data-ttu-id="67574-113">Account</span><span class="sxs-lookup"><span data-stu-id="67574-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67574-114">備考</span><span class="sxs-lookup"><span data-stu-id="67574-114">Remarks</span></span>

<span data-ttu-id="67574-115">このプロパティは、MAPI のメッセージ オブジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="67574-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="67574-116">受信したメッセージは、プライマリ アカウントの「送信」スタンプはアカウントには、転送または返信を送信するかを示します。</span><span class="sxs-lookup"><span data-stu-id="67574-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="67574-117">送信メッセージでは、メッセージを送信するアカウントを決定します。</span><span class="sxs-lookup"><span data-stu-id="67574-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="67574-118">その値が、 [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) 、 [IOlkAccount](iolkaccount.md)のインターフェイス、メッセージが送信されているアカウントからです。</span><span class="sxs-lookup"><span data-stu-id="67574-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67574-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="67574-119">See also</span></span>

- [<span data-ttu-id="67574-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="67574-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="67574-121">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="67574-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="67574-122">PidTagPrimarySendAccount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="67574-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

