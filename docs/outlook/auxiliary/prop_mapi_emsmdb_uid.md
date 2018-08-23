---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Exchange アカウントの UID を含む ACCT_BIN 構造体を表します。
ms.openlocfilehash: 05e2e61601a08e0cb6f6dc99d265f12a10b19d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799588"
---
# <a name="propmapiemsmdbuid"></a><span data-ttu-id="c16fb-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="c16fb-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="c16fb-104">Exchange アカウントの UID を含む[ACCT_BIN](acct_bin.md)構造体を表します。</span><span class="sxs-lookup"><span data-stu-id="c16fb-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c16fb-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="c16fb-105">Quick info</span></span>

<span data-ttu-id="c16fb-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c16fb-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c16fb-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="c16fb-107">Identifier:</span></span>  <br/> |<span data-ttu-id="c16fb-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="c16fb-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="c16fb-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="c16fb-109">Property type:</span></span>  <br/> |<span data-ttu-id="c16fb-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c16fb-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c16fb-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="c16fb-111">Property tag:</span></span>  <br/> |<span data-ttu-id="c16fb-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="c16fb-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="c16fb-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="c16fb-113">Access:</span></span>  <br/> |<span data-ttu-id="c16fb-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="c16fb-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c16fb-115">注釈</span><span class="sxs-lookup"><span data-stu-id="c16fb-115">Remarks</span></span>

<span data-ttu-id="c16fb-116">[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="c16fb-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="c16fb-117">[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)を使用して、アカウントが Exchange アカウントかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c16fb-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="c16fb-118">場合は、**プロペラ\_MAPI_EMSMDB_UID** 、 **emsmdbUID**は、Exchange アカウントの一意の ID が含まれています**ACCT_BIN**は、です。</span><span class="sxs-lookup"><span data-stu-id="c16fb-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="c16fb-119">アカウントが Exchange アカウントでない場合は、このプロパティは定義されていません。</span><span class="sxs-lookup"><span data-stu-id="c16fb-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c16fb-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="c16fb-120">See also</span></span>

- [<span data-ttu-id="c16fb-121">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="c16fb-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="c16fb-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="c16fb-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="c16fb-123">複数の Exchange アカウントの使用</span><span class="sxs-lookup"><span data-stu-id="c16fb-123">Using Multiple Exchange Accounts</span></span>](http://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="c16fb-124">PidTagExchangeProfileSectionId ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="c16fb-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](http://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

