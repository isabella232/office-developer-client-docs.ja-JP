---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: SMTP アカウントに使用する認証方法を指定します。
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799583"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="6f6da-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="6f6da-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="6f6da-104">SMTP アカウントに使用する認証方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="6f6da-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6f6da-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="6f6da-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f6da-106">識別子:</span><span class="sxs-lookup"><span data-stu-id="6f6da-106">Identifier:</span></span>  <br/> |<span data-ttu-id="6f6da-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="6f6da-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="6f6da-108">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="6f6da-108">Property type:</span></span>  <br/> |<span data-ttu-id="6f6da-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="6f6da-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="6f6da-110">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="6f6da-110">Property tag:</span></span>  <br/> |<span data-ttu-id="6f6da-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="6f6da-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="6f6da-112">アクセス:</span><span class="sxs-lookup"><span data-stu-id="6f6da-112">Access:</span></span>  <br/> |<span data-ttu-id="6f6da-113">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6f6da-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f6da-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6f6da-114">Remarks</span></span>

<span data-ttu-id="6f6da-115">値は、以下の定数のビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="6f6da-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="6f6da-116">その値の[定数 (アカウント管理 API)](constants-account-management-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f6da-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="6f6da-117">**SMTP_AUTH_SAME_AS_POP**は、 [PROP_INET_USER](prop_inet_user.md)と[PROP_INET_PASSWORD](prop_inet_password.md)によって提供されるように、受信メール サーバーと同じ資格情報を使用してを意味します。</span><span class="sxs-lookup"><span data-stu-id="6f6da-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="6f6da-118">**SMTP_AUTH_USER_PASS**は、 [PROP_SMTP_USER](prop_smtp_user.md)と[PROP_SMTP_PASSWORD](prop_smtp_password.md)によって提供された資格情報を使用することを意味します。</span><span class="sxs-lookup"><span data-stu-id="6f6da-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="6f6da-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND**では、メールを送信する前に受信メール サーバーにログオンするユーザーを要求することを意味します。</span><span class="sxs-lookup"><span data-stu-id="6f6da-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6f6da-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f6da-120">See also</span></span>

- [<span data-ttu-id="6f6da-121">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="6f6da-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="6f6da-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="6f6da-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

