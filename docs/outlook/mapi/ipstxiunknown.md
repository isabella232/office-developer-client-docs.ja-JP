---
title: ipstx IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX
api_type:
- COM
ms.assetid: 73752f57-6fbc-0201-bf95-0e75c56c04e6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4c758ecd0134ca11ced6f771303896bd885a22c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278800"
---
# <a name="ipstx--iunknown"></a><span data-ttu-id="a44f4-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a44f4-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="a44f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a44f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a44f4-105">このインターフェイスは、 **[iostx](iostxiunknown.md)** インターフェイスを介してレプリケーションを実行するときに、ヘルパー機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="a44f4-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a44f4-106">提供元</span><span class="sxs-lookup"><span data-stu-id="a44f4-106">Provided by</span></span>  <br/> |<span data-ttu-id="a44f4-107">[IMsgStore](imsgstoreimapiprop.md)のクエリ</span><span class="sxs-lookup"><span data-stu-id="a44f4-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="a44f4-108">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="a44f4-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a44f4-109">IID_IPSTX</span><span class="sxs-lookup"><span data-stu-id="a44f4-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a44f4-110">v の順序</span><span class="sxs-lookup"><span data-stu-id="a44f4-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a44f4-111">**[GetLastError](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="a44f4-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="a44f4-112">最新のエラーに関する拡張情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="a44f4-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="a44f4-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="a44f4-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="a44f4-114">関連付けられた**[iostx](iostxiunknown.md)** インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="a44f4-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="a44f4-115">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="a44f4-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a44f4-116">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="a44f4-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="a44f4-117">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="a44f4-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a44f4-118">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="a44f4-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="a44f4-119">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="a44f4-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a44f4-120">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="a44f4-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="a44f4-121">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="a44f4-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a44f4-122">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="a44f4-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="a44f4-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="a44f4-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="a44f4-124">Outlook プロトコルマネージャーをエミュレートして、送信メッセージをサーバーにスプールするように、ローカルストアを設定します。</span><span class="sxs-lookup"><span data-stu-id="a44f4-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="a44f4-125">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="a44f4-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a44f4-126">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="a44f4-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="a44f4-127">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="a44f4-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a44f4-128">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="a44f4-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="a44f4-129">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="a44f4-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a44f4-130">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="a44f4-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="a44f4-131">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="a44f4-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a44f4-132">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="a44f4-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="a44f4-133">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="a44f4-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="a44f4-134">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="a44f4-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a44f4-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="a44f4-135">See also</span></span>



[<span data-ttu-id="a44f4-136">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a44f4-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a44f4-137">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="a44f4-137">MAPI Constants</span></span>](mapi-constants.md)

