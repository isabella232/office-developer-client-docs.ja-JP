---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: アカウントが Exchange アカウントの場合は true。
ms.openlocfilehash: db9f5ae46096d221ac3636a44f588c6a90ce146e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799553"
---
# <a name="propacctisexch"></a><span data-ttu-id="3a364-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="3a364-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="3a364-104">アカウントが Exchange アカウントの場合は true。</span><span class="sxs-lookup"><span data-stu-id="3a364-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3a364-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3a364-105">Quick info</span></span>

<span data-ttu-id="3a364-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3a364-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a364-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="3a364-107">Identifier:</span></span>  <br/> |<span data-ttu-id="3a364-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="3a364-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="3a364-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="3a364-109">Property type:</span></span>  <br/> |<span data-ttu-id="3a364-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3a364-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3a364-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="3a364-111">Property tag:</span></span>  <br/> |<span data-ttu-id="3a364-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="3a364-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="3a364-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="3a364-113">Access:</span></span>  <br/> |<span data-ttu-id="3a364-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3a364-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a364-115">注釈</span><span class="sxs-lookup"><span data-stu-id="3a364-115">Remarks</span></span>

<span data-ttu-id="3a364-116">[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="3a364-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="3a364-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="3a364-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a364-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a364-118">See also</span></span>

- [<span data-ttu-id="3a364-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="3a364-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="3a364-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="3a364-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

