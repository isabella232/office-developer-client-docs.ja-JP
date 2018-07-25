---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: アカウントのタイムスタンプを返します。
ms.openlocfilehash: ec1824d8c8c61d392b4e11cdb5213a85100d971e
ms.sourcegitcommit: c55eec212ae794592c83bbf06b01eab5ca6bff6d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2018
ms.locfileid: "19799576"
---
# <a name="propacctstamp"></a><span data-ttu-id="960d1-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="960d1-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="960d1-104">アカウントのタイムスタンプを返します。</span><span class="sxs-lookup"><span data-stu-id="960d1-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="960d1-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="960d1-105">Quick info</span></span>

<span data-ttu-id="960d1-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="960d1-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="960d1-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="960d1-107">Identifier:</span></span>  <br/> |<span data-ttu-id="960d1-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="960d1-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="960d1-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="960d1-109">Property type:</span></span>  <br/> |<span data-ttu-id="960d1-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="960d1-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="960d1-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="960d1-111">Property tag:</span></span>  <br/> |<span data-ttu-id="960d1-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="960d1-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="960d1-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="960d1-113">Access:</span></span>  <br/> |<span data-ttu-id="960d1-114">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="960d1-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="960d1-115">注釈</span><span class="sxs-lookup"><span data-stu-id="960d1-115">Remarks</span></span>

<span data-ttu-id="960d1-116">[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="960d1-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="960d1-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="960d1-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="960d1-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="960d1-118">See also</span></span>

- [<span data-ttu-id="960d1-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="960d1-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="960d1-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="960d1-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

