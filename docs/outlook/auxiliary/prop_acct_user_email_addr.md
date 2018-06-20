---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: アカウントの電子メール アドレスを指定します。
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799571"
---
# <a name="propacctuseremailaddr"></a><span data-ttu-id="70762-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="70762-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="70762-104">アカウントの電子メール アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="70762-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="70762-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="70762-105">Quick info</span></span>

<span data-ttu-id="70762-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70762-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70762-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="70762-107">Identifier:</span></span>  <br/> |<span data-ttu-id="70762-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="70762-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="70762-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="70762-109">Property type:</span></span>  <br/> |<span data-ttu-id="70762-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70762-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="70762-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="70762-111">Property tag:</span></span>  <br/> |<span data-ttu-id="70762-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="70762-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="70762-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="70762-113">Access:</span></span>  <br/> |<span data-ttu-id="70762-114">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="70762-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70762-115">備考</span><span class="sxs-lookup"><span data-stu-id="70762-115">Remarks</span></span>

 <span data-ttu-id="70762-116">**PROP_ACCT_USER_EMAIL_ADDR**は、すべてのアカウントが存在するように想定されていません。</span><span class="sxs-lookup"><span data-stu-id="70762-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="70762-117">[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)がない**PROP_ACCT_USER_EMAIL_ADDR**、たとえば、Exchange アカウントがある、SMTP と POP3 アカウントの中にこの状況が一変します。</span><span class="sxs-lookup"><span data-stu-id="70762-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="70762-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="70762-118">See also</span></span>

- [<span data-ttu-id="70762-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="70762-119">About the Account Management API</span></span>](about-the-account-management-api.md)

