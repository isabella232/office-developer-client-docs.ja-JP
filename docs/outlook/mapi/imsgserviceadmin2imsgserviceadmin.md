---
title: IMsgServiceAdmin2 IMsgServiceAdmin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2
api_type:
- COM
ms.assetid: 14654259-e884-46bf-84ff-9e3c1a8cd60d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b1e00938800fb6517e634c3ba365276e0e76bd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348840"
---
# <a name="imsgserviceadmin2--imsgserviceadmin"></a><span data-ttu-id="0264d-103">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="0264d-103">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>

  
  
<span data-ttu-id="0264d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0264d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0264d-105">プロファイル内のメッセージサービスの変更を行います。</span><span class="sxs-lookup"><span data-stu-id="0264d-105">Makes changes to a message service in a profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0264d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0264d-106">Header file:</span></span>  <br/> |<span data-ttu-id="0264d-107">Mapiaux</span><span class="sxs-lookup"><span data-stu-id="0264d-107">Mapiaux.h</span></span>  <br/> |
|<span data-ttu-id="0264d-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="0264d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0264d-109">メッセージサービスの管理オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0264d-109">Message service administration objects</span></span>  <br/> |
|<span data-ttu-id="0264d-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="0264d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0264d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0264d-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="0264d-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="0264d-112">Called by:</span></span>  <br/> |<span data-ttu-id="0264d-113">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0264d-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="0264d-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="0264d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0264d-115">IID_IMsgServiceAdmin2</span><span class="sxs-lookup"><span data-stu-id="0264d-115">IID_IMsgServiceAdmin2</span></span>  <br/> |
|<span data-ttu-id="0264d-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="0264d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0264d-117">LPSERVICEADMIN2</span><span class="sxs-lookup"><span data-stu-id="0264d-117">LPSERVICEADMIN2</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0264d-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="0264d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0264d-119">CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="0264d-119">CreateMsgServiceEx</span></span>](imsgserviceadmin2-createmsgserviceex.md) <br/> |<span data-ttu-id="0264d-120">現在のプロファイルにメッセージサービスを追加し、新しく追加されたサービス UID を返します。</span><span class="sxs-lookup"><span data-stu-id="0264d-120">Adds a message service to the current profile and returns that newly added service UID.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0264d-121">解説</span><span class="sxs-lookup"><span data-stu-id="0264d-121">Remarks</span></span>

<span data-ttu-id="0264d-122">**IMsgServiceAdmin2**インターフェイスは、 [IMsgServiceAdmin](imsgserviceadminiunknown.md)インターフェイスを公開するのと同じオブジェクトによって公開されており、Microsoft outlook 2003 以降の outlook の MAPI サブシステムの実装を使用して利用できるようになっています。</span><span class="sxs-lookup"><span data-stu-id="0264d-122">The **IMsgServiceAdmin2** interface is exposed by the same objects that expose the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface, and has been available using Outlook's implementation of the MAPI subsystem since Microsoft Outlook 2003.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0264d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="0264d-123">See also</span></span>



[<span data-ttu-id="0264d-124">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="0264d-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

