---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: メッセージの第 2 の accountsendstamp を指定します。
ms.openlocfilehash: 63d98382ff8a5a545cdb015c089c7b0a38926138
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799560"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="d8fce-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="d8fce-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="d8fce-104">メッセージのサブ アカウントの「送信」スタンプを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8fce-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d8fce-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d8fce-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8fce-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d8fce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8fce-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="d8fce-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="d8fce-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d8fce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d8fce-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="d8fce-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="d8fce-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d8fce-110">Data type:</span></span>  <br/> |<span data-ttu-id="d8fce-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d8fce-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d8fce-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d8fce-112">Area:</span></span>  <br/> |<span data-ttu-id="d8fce-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d8fce-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8fce-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d8fce-114">Remarks</span></span>

<span data-ttu-id="d8fce-115">このプロパティは、MAPI のメッセージ オブジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d8fce-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="d8fce-116">受信したメッセージは、サブ アカウントの「送信」タイムスタンプは、プライマリ アカウントを使用して転送、または返信を送信できない場合、転送または返信を送信するアカウントを示します。</span><span class="sxs-lookup"><span data-stu-id="d8fce-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="d8fce-117">、送信メッセージのスタンプを「送信」サブ アカウントをプライマリ アカウントでメッセージを送信できない場合にメッセージを送信するアカウントを決定します。</span><span class="sxs-lookup"><span data-stu-id="d8fce-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="d8fce-118">その値が、 [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) 、 [IOlkAccount](iolkaccount.md)のインターフェイス、メッセージが送信されているアカウントからです。</span><span class="sxs-lookup"><span data-stu-id="d8fce-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8fce-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8fce-119">See also</span></span>

- [<span data-ttu-id="d8fce-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="d8fce-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="d8fce-121">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d8fce-121">MAPI Properties</span></span>](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="d8fce-122">PidTagNextSendAcct 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d8fce-122">PidTagNextSendAcct Canonical Property</span></span>](http://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

