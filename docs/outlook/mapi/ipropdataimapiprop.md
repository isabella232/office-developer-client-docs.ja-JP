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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d6a53d112e4c12cd9092ac627e99cf3c13d901f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801147"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="7998f-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7998f-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="7998f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7998f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7998f-105">取得し、オブジェクトのプロパティに対するアクセス権を変更する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="7998f-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7998f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7998f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7998f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7998f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7998f-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="7998f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="7998f-109">データ オブジェクトのプロパティ</span><span class="sxs-lookup"><span data-stu-id="7998f-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="7998f-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="7998f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7998f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="7998f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="7998f-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7998f-112">Called by:</span></span>  <br/> |<span data-ttu-id="7998f-113">サービス プロバイダーとクライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="7998f-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="7998f-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="7998f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7998f-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="7998f-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="7998f-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="7998f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="7998f-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="7998f-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="7998f-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="7998f-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="7998f-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="7998f-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7998f-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="7998f-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7998f-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="7998f-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="7998f-122">�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="7998f-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="7998f-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="7998f-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="7998f-124">状態の 1 つまたは複数オブジェクトのプロパティのアクセス レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="7998f-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="7998f-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="7998f-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="7998f-126">�A�N�Z�X ���x���� 1 �܂��͕����̃I�u�W�F�N�g�̃v���p�e�B�̏�Ԃ�擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="7998f-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="7998f-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="7998f-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="7998f-128">PT_OBJECT の種類の 1 つまたは複数のプロパティをオブジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="7998f-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7998f-129">注釈</span><span class="sxs-lookup"><span data-stu-id="7998f-129">Remarks</span></span>

<span data-ttu-id="7998f-130">**IPropData::IMAPIProp**インターフェイスは、MAPI によって実装され、 [CreateIProp](createiprop.md)関数を呼び出して、この実装にアクセスするサービス プロバイダーによって主に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7998f-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="7998f-131">オブジェクトおよびプロパティのアクセス レベルに関する詳細については、[オブジェクトとプロパティのアクセス許可](permissions-for-mapi-objects-and-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7998f-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7998f-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="7998f-132">See also</span></span>



[<span data-ttu-id="7998f-133">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7998f-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

