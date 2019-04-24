---
title: ipropdata imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279543"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="231bf-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="231bf-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="231bf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="231bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="231bf-105">オブジェクトのプロパティのアクセスを取得および変更する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="231bf-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="231bf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="231bf-106">Header file:</span></span>  <br/> |<span data-ttu-id="231bf-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="231bf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="231bf-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="231bf-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="231bf-109">プロパティデータオブジェクト</span><span class="sxs-lookup"><span data-stu-id="231bf-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="231bf-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="231bf-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="231bf-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="231bf-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="231bf-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="231bf-112">Called by:</span></span>  <br/> |<span data-ttu-id="231bf-113">サービスプロバイダおよびクライアントアプリケーション</span><span class="sxs-lookup"><span data-stu-id="231bf-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="231bf-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="231bf-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="231bf-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="231bf-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="231bf-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="231bf-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="231bf-117">lppropdata</span><span class="sxs-lookup"><span data-stu-id="231bf-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="231bf-118">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="231bf-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="231bf-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="231bf-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="231bf-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="231bf-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="231bf-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="231bf-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="231bf-122">�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="231bf-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="231bf-123">hrsetpropaccess</span><span class="sxs-lookup"><span data-stu-id="231bf-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="231bf-124">1つ以上のオブジェクトのプロパティのアクセスレベルと状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="231bf-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="231bf-125">hrgetpropaccess</span><span class="sxs-lookup"><span data-stu-id="231bf-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="231bf-126">�A�N�Z�X ���x���� 1 �܂��͕����̃I�u�W�F�N�g�̃v���p�e�B�̏�Ԃ�擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="231bf-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="231bf-127">hraddobjprops</span><span class="sxs-lookup"><span data-stu-id="231bf-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="231bf-128">オブジェクトに PT_OBJECT 型の1つ以上のプロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="231bf-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="231bf-129">解説</span><span class="sxs-lookup"><span data-stu-id="231bf-129">Remarks</span></span>

<span data-ttu-id="231bf-130">**ipropdata:: imapiprop**インターフェイスは MAPI で実装されており、主に、 [createiprop](createiprop.md)関数を呼び出してこの実装にアクセスするサービスプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="231bf-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="231bf-131">オブジェクトおよびプロパティのアクセスレベルの詳細については、「[オブジェクトおよびプロパティのアクセス許可](permissions-for-mapi-objects-and-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="231bf-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="231bf-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="231bf-132">See also</span></span>



[<span data-ttu-id="231bf-133">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="231bf-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

