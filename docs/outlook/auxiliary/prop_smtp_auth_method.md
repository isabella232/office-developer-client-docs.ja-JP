---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: SMTP アカウントに使用する認証方法を指定します。
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326503"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="813f8-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="813f8-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="813f8-104">SMTP アカウントに使用する認証方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="813f8-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="813f8-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="813f8-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="813f8-106">識別子:</span><span class="sxs-lookup"><span data-stu-id="813f8-106">Identifier:</span></span>  <br/> |<span data-ttu-id="813f8-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="813f8-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="813f8-108">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="813f8-108">Property type:</span></span>  <br/> |<span data-ttu-id="813f8-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="813f8-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="813f8-110">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="813f8-110">Property tag:</span></span>  <br/> |<span data-ttu-id="813f8-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="813f8-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="813f8-112">接続</span><span class="sxs-lookup"><span data-stu-id="813f8-112">Access:</span></span>  <br/> |<span data-ttu-id="813f8-113">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="813f8-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="813f8-114">解説</span><span class="sxs-lookup"><span data-stu-id="813f8-114">Remarks</span></span>

<span data-ttu-id="813f8-115">値は、次の定数のビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="813f8-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="813f8-116">値については、「 [Constants (Account management API)](constants-account-management-api.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="813f8-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="813f8-117">**SMTP_AUTH_SAME_AS_POP**は、 [PROP_INET_USER](prop_inet_user.md)と[PROP_INET_PASSWORD](prop_inet_password.md)で提供されるように、受信メールサーバーと同じ資格情報を使用することを意味します。</span><span class="sxs-lookup"><span data-stu-id="813f8-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="813f8-118">**SMTP_AUTH_USER_PASS**は、 [PROP_SMTP_USER](prop_smtp_user.md)および[PROP_SMTP_PASSWORD](prop_smtp_password.md)によって提供される資格情報を使用することを意味します。</span><span class="sxs-lookup"><span data-stu-id="813f8-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="813f8-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND**は、メールを送信する前に、受信メールサーバーにログオンするようにユーザーに要求することを意味します。</span><span class="sxs-lookup"><span data-stu-id="813f8-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="813f8-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="813f8-120">See also</span></span>

- [<span data-ttu-id="813f8-121">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="813f8-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="813f8-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="813f8-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

