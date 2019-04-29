---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: アカウントの電子メールアドレスを指定します。
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436777"
---
# <a name="propacctuseremailaddr"></a><span data-ttu-id="1ae08-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="1ae08-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="1ae08-104">アカウントの電子メールアドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="1ae08-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1ae08-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1ae08-105">Quick info</span></span>

<span data-ttu-id="1ae08-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ae08-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ae08-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="1ae08-107">Identifier:</span></span>  <br/> |<span data-ttu-id="1ae08-108">0x000c</span><span class="sxs-lookup"><span data-stu-id="1ae08-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="1ae08-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="1ae08-109">Property type:</span></span>  <br/> |<span data-ttu-id="1ae08-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1ae08-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1ae08-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="1ae08-111">Property tag:</span></span>  <br/> |<span data-ttu-id="1ae08-112">0x000c001f</span><span class="sxs-lookup"><span data-stu-id="1ae08-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="1ae08-113">接続</span><span class="sxs-lookup"><span data-stu-id="1ae08-113">Access:</span></span>  <br/> |<span data-ttu-id="1ae08-114">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="1ae08-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ae08-115">注釈</span><span class="sxs-lookup"><span data-stu-id="1ae08-115">Remarks</span></span>

 <span data-ttu-id="1ae08-116">**PROP_ACCT_USER_EMAIL_ADDR**は、すべてのアカウントに存在するとは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="1ae08-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="1ae08-117">たとえば、Exchange アカウントは[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)を持つことはできますが、 **PROP_ACCT_USER_EMAIL_ADDR**はできませんが、SMTP/POP3 アカウントの場合は、状況を逆にします。</span><span class="sxs-lookup"><span data-stu-id="1ae08-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1ae08-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ae08-118">See also</span></span>

- [<span data-ttu-id="1ae08-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="1ae08-119">About the Account Management API</span></span>](about-the-account-management-api.md)

