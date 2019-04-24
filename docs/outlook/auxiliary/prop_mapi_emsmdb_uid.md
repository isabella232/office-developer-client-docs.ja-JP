---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Exchange アカウントの UID を含む ACCT_BIN 構造体を表します。
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326552"
---
# <a name="propmapiemsmdbuid"></a><span data-ttu-id="cbf17-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="cbf17-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="cbf17-104">Exchange アカウントの UID を含む[ACCT_BIN](acct_bin.md)構造体を表します。</span><span class="sxs-lookup"><span data-stu-id="cbf17-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="cbf17-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="cbf17-105">Quick info</span></span>

<span data-ttu-id="cbf17-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbf17-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cbf17-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="cbf17-107">Identifier:</span></span>  <br/> |<span data-ttu-id="cbf17-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="cbf17-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="cbf17-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="cbf17-109">Property type:</span></span>  <br/> |<span data-ttu-id="cbf17-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cbf17-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cbf17-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="cbf17-111">Property tag:</span></span>  <br/> |<span data-ttu-id="cbf17-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="cbf17-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="cbf17-113">接続</span><span class="sxs-lookup"><span data-stu-id="cbf17-113">Access:</span></span>  <br/> |<span data-ttu-id="cbf17-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="cbf17-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbf17-115">解説</span><span class="sxs-lookup"><span data-stu-id="cbf17-115">Remarks</span></span>

<span data-ttu-id="cbf17-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="cbf17-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="cbf17-117">[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)を使用して、アカウントが Exchange アカウントであるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="cbf17-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="cbf17-118">その場合、 **PROP\_MAPI_EMSMDB_UID**は、Exchange アカウントの一意の ID である**emsmdbUID**を含む**ACCT_BIN**です。</span><span class="sxs-lookup"><span data-stu-id="cbf17-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="cbf17-119">アカウントが Exchange アカウントではない場合、このプロパティは未定義です。</span><span class="sxs-lookup"><span data-stu-id="cbf17-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cbf17-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="cbf17-120">See also</span></span>

- [<span data-ttu-id="cbf17-121">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="cbf17-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="cbf17-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="cbf17-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="cbf17-123">複数の Exchange アカウントの使用</span><span class="sxs-lookup"><span data-stu-id="cbf17-123">Using Multiple Exchange Accounts</span></span>](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="cbf17-124">PidTagExchangeProfileSectionId ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cbf17-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

