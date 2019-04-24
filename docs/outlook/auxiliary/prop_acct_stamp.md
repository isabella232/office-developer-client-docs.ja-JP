---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: アカウントスタンプを返します。
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327595"
---
# <a name="propacctstamp"></a><span data-ttu-id="b31f2-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="b31f2-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="b31f2-104">アカウントスタンプを返します。</span><span class="sxs-lookup"><span data-stu-id="b31f2-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b31f2-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b31f2-105">Quick info</span></span>

<span data-ttu-id="b31f2-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b31f2-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b31f2-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="b31f2-107">Identifier:</span></span>  <br/> |<span data-ttu-id="b31f2-108">0x000d</span><span class="sxs-lookup"><span data-stu-id="b31f2-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="b31f2-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="b31f2-109">Property type:</span></span>  <br/> |<span data-ttu-id="b31f2-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b31f2-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b31f2-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="b31f2-111">Property tag:</span></span>  <br/> |<span data-ttu-id="b31f2-112">0x000d001f</span><span class="sxs-lookup"><span data-stu-id="b31f2-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="b31f2-113">接続</span><span class="sxs-lookup"><span data-stu-id="b31f2-113">Access:</span></span>  <br/> |<span data-ttu-id="b31f2-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="b31f2-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b31f2-115">解説</span><span class="sxs-lookup"><span data-stu-id="b31f2-115">Remarks</span></span>

<span data-ttu-id="b31f2-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="b31f2-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="b31f2-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="b31f2-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b31f2-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="b31f2-118">See also</span></span>

- [<span data-ttu-id="b31f2-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="b31f2-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="b31f2-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="b31f2-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

