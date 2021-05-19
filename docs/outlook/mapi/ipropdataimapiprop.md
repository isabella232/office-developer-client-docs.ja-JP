---
title: IPropData IMAPIProp
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435146"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="5c827-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5c827-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="5c827-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c827-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c827-105">オブジェクトのプロパティのアクセスを取得および変更する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c827-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c827-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5c827-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c827-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5c827-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5c827-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="5c827-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5c827-109">プロパティ データ オブジェクト</span><span class="sxs-lookup"><span data-stu-id="5c827-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="5c827-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="5c827-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5c827-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5c827-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="5c827-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5c827-112">Called by:</span></span>  <br/> |<span data-ttu-id="5c827-113">サービス プロバイダーとクライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5c827-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="5c827-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="5c827-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5c827-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="5c827-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="5c827-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="5c827-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5c827-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="5c827-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="5c827-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="5c827-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="5c827-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="5c827-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5c827-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="5c827-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5c827-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="5c827-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="5c827-122">�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="5c827-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="5c827-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="5c827-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="5c827-124">1 つ以上のオブジェクトのプロパティのアクセス レベルと状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="5c827-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="5c827-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="5c827-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="5c827-126">�A�N�Z�X ���x���� 1 �܂��͕����̃I�u�W�F�N�g�̃v���p�e�B�̏�Ԃ�擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="5c827-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="5c827-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="5c827-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="5c827-128">オブジェクトの種類のプロパティを 1 つ以上PT_OBJECTオブジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="5c827-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c827-129">注釈</span><span class="sxs-lookup"><span data-stu-id="5c827-129">Remarks</span></span>

<span data-ttu-id="5c827-130">**IPropData::IMAPIProp** インターフェイスは MAPI によって実装され、主に CreateIProp 関数を呼び出してこの実装にアクセスする [サービス プロバイダーによって使用](createiprop.md)されます。</span><span class="sxs-lookup"><span data-stu-id="5c827-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="5c827-131">オブジェクトとプロパティのアクセス レベルの詳細については、「オブジェクトとプロパティの [アクセス許可」を参照してください](permissions-for-mapi-objects-and-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="5c827-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c827-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c827-132">See also</span></span>



[<span data-ttu-id="5c827-133">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="5c827-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

