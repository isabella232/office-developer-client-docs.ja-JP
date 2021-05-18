---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: アカウント スタンプを返します。
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408251"
---
# <a name="prop_acct_stamp"></a><span data-ttu-id="4cf98-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="4cf98-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="4cf98-104">アカウント スタンプを返します。</span><span class="sxs-lookup"><span data-stu-id="4cf98-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4cf98-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="4cf98-105">Quick info</span></span>

<span data-ttu-id="4cf98-106">[「IOlkAccount」を参照してください](iolkaccount.md)。</span><span class="sxs-lookup"><span data-stu-id="4cf98-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4cf98-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="4cf98-107">Identifier:</span></span>  <br/> |<span data-ttu-id="4cf98-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="4cf98-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="4cf98-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="4cf98-109">Property type:</span></span>  <br/> |<span data-ttu-id="4cf98-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4cf98-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4cf98-111">プロパティ タグ:</span><span class="sxs-lookup"><span data-stu-id="4cf98-111">Property tag:</span></span>  <br/> |<span data-ttu-id="4cf98-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="4cf98-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="4cf98-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="4cf98-113">Access:</span></span>  <br/> |<span data-ttu-id="4cf98-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="4cf98-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cf98-115">注釈</span><span class="sxs-lookup"><span data-stu-id="4cf98-115">Remarks</span></span>

<span data-ttu-id="4cf98-116">[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。</span><span class="sxs-lookup"><span data-stu-id="4cf98-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="4cf98-117">クライアントがこのプロパティを設定しようとすると、このプロパティは次 **E_OLK_PROP_READ_ONLY。**</span><span class="sxs-lookup"><span data-stu-id="4cf98-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4cf98-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="4cf98-118">See also</span></span>

- [<span data-ttu-id="4cf98-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="4cf98-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="4cf98-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="4cf98-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

