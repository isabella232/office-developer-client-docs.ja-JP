---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True の場合は、アカウントがアカウントExchangeします。
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418233"
---
# <a name="prop_acct_is_exch"></a><span data-ttu-id="1ca7e-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="1ca7e-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="1ca7e-104">True の場合は、アカウントがアカウントExchangeします。</span><span class="sxs-lookup"><span data-stu-id="1ca7e-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1ca7e-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1ca7e-105">Quick info</span></span>

<span data-ttu-id="1ca7e-106">[「IOlkAccount」を参照してください](iolkaccount.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca7e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ca7e-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="1ca7e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="1ca7e-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="1ca7e-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="1ca7e-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="1ca7e-109">Property type:</span></span>  <br/> |<span data-ttu-id="1ca7e-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1ca7e-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1ca7e-111">プロパティ タグ:</span><span class="sxs-lookup"><span data-stu-id="1ca7e-111">Property tag:</span></span>  <br/> |<span data-ttu-id="1ca7e-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="1ca7e-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="1ca7e-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="1ca7e-113">Access:</span></span>  <br/> |<span data-ttu-id="1ca7e-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1ca7e-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ca7e-115">注釈</span><span class="sxs-lookup"><span data-stu-id="1ca7e-115">Remarks</span></span>

<span data-ttu-id="1ca7e-116">[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca7e-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="1ca7e-117">クライアントがこのプロパティを設定しようとすると、このプロパティは次 **E_OLK_PROP_READ_ONLY。**</span><span class="sxs-lookup"><span data-stu-id="1ca7e-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ca7e-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ca7e-118">See also</span></span>

- [<span data-ttu-id="1ca7e-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="1ca7e-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="1ca7e-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="1ca7e-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

