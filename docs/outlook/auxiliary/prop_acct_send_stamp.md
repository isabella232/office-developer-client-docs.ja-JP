---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: accountsendstamp を返します。
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423007"
---
# <a name="prop_acct_send_stamp"></a><span data-ttu-id="76e84-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="76e84-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="76e84-104">アカウントの "送信" スタンプを返します。</span><span class="sxs-lookup"><span data-stu-id="76e84-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="76e84-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="76e84-105">Quick info</span></span>

<span data-ttu-id="76e84-106">[「IOlkAccount」を参照してください](iolkaccount.md)。</span><span class="sxs-lookup"><span data-stu-id="76e84-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76e84-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="76e84-107">Identifier:</span></span>  <br/> |<span data-ttu-id="76e84-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="76e84-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="76e84-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="76e84-109">Property type:</span></span>  <br/> |<span data-ttu-id="76e84-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="76e84-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="76e84-111">プロパティ タグ:</span><span class="sxs-lookup"><span data-stu-id="76e84-111">Property tag:</span></span>  <br/> |<span data-ttu-id="76e84-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="76e84-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="76e84-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="76e84-113">Access:</span></span>  <br/> |<span data-ttu-id="76e84-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="76e84-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76e84-115">注釈</span><span class="sxs-lookup"><span data-stu-id="76e84-115">Remarks</span></span>

<span data-ttu-id="76e84-116">[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。</span><span class="sxs-lookup"><span data-stu-id="76e84-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="76e84-117">クライアントがこのプロパティを設定しようとすると、このプロパティは次 **E_OLK_PROP_READ_ONLY。**</span><span class="sxs-lookup"><span data-stu-id="76e84-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76e84-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="76e84-118">See also</span></span>

- [<span data-ttu-id="76e84-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="76e84-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="76e84-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="76e84-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

