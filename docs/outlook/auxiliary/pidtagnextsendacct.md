---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: メッセージのセカンダリ アカウントendstampを指定します。
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327714"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="cd35a-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="cd35a-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="cd35a-104">メッセージのセカンダリ アカウント "send" スタンプを指定します。</span><span class="sxs-lookup"><span data-stu-id="cd35a-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cd35a-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="cd35a-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd35a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cd35a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd35a-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="cd35a-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="cd35a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cd35a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd35a-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="cd35a-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="cd35a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cd35a-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd35a-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cd35a-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cd35a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="cd35a-112">Area:</span></span>  <br/> |<span data-ttu-id="cd35a-113">Outlookアプリケーション</span><span class="sxs-lookup"><span data-stu-id="cd35a-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd35a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="cd35a-114">Remarks</span></span>

<span data-ttu-id="cd35a-115">このプロパティは、MAPI メッセージ オブジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="cd35a-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="cd35a-116">受信したメッセージの場合、セカンダリ アカウントの "送信" スタンプは、転送または返信をプライマリ アカウントで送信できない場合に、転送または返信を送信するアカウントを示します。</span><span class="sxs-lookup"><span data-stu-id="cd35a-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="cd35a-117">送信メッセージの場合、セカンダリ アカウント "send" スタンプは、メッセージをプライマリ アカウントと一緒に送信できない場合に、メッセージを送信するアカウントを決定します。</span><span class="sxs-lookup"><span data-stu-id="cd35a-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="cd35a-118">その値は [、PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) が送信されるアカウントの [IOlkAccount](iolkaccount.md) インターフェイスからの値です。</span><span class="sxs-lookup"><span data-stu-id="cd35a-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd35a-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd35a-119">See also</span></span>

- [<span data-ttu-id="cd35a-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="cd35a-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="cd35a-121">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="cd35a-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="cd35a-122">PidTagNextSendAcct 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cd35a-122">PidTagNextSendAcct Canonical Property</span></span>](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

