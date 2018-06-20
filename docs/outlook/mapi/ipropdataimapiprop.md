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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d6a53d112e4c12cd9092ac627e99cf3c13d901f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801147"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="c7659-103">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c7659-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="c7659-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7659-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7659-105">取得し、オブジェクトのプロパティに対するアクセス権を変更する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="c7659-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7659-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c7659-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7659-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c7659-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c7659-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="c7659-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c7659-109">データ オブジェクトのプロパティ</span><span class="sxs-lookup"><span data-stu-id="c7659-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="c7659-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="c7659-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c7659-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="c7659-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="c7659-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c7659-112">Called by:</span></span>  <br/> |<span data-ttu-id="c7659-113">サービス プロバイダーとクライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="c7659-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="c7659-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="c7659-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c7659-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="c7659-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="c7659-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="c7659-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c7659-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="c7659-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="c7659-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="c7659-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="c7659-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="c7659-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c7659-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="c7659-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c7659-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="c7659-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="c7659-122">�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="c7659-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="c7659-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="c7659-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="c7659-124">状態の 1 つまたは複数オブジェクトのプロパティのアクセス レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="c7659-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="c7659-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="c7659-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="c7659-126">�A�N�Z�X ���x���� 1 �܂��͕����̃I�u�W�F�N�g�̃v���p�e�B�̏�Ԃ�擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="c7659-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="c7659-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="c7659-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="c7659-128">PT_OBJECT の種類の 1 つまたは複数のプロパティをオブジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="c7659-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7659-129">備考</span><span class="sxs-lookup"><span data-stu-id="c7659-129">Remarks</span></span>

<span data-ttu-id="c7659-130">**IPropData::IMAPIProp**インターフェイスは、MAPI によって実装され、 [CreateIProp](createiprop.md)関数を呼び出して、この実装にアクセスするサービス プロバイダーによって主に使用されます。</span><span class="sxs-lookup"><span data-stu-id="c7659-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="c7659-131">オブジェクトおよびプロパティのアクセス レベルに関する詳細については、[オブジェクトとプロパティのアクセス許可](permissions-for-mapi-objects-and-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7659-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c7659-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7659-132">See also</span></span>



[<span data-ttu-id="c7659-133">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c7659-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

