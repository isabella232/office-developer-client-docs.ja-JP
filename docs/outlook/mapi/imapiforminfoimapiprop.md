---
title: imapiforminfo imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321736"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="640cd-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="640cd-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="640cd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="640cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="640cd-105">クライアントアプリケーションに、フォーム定義に特したプロパティへのアクセス権を付与します。</span><span class="sxs-lookup"><span data-stu-id="640cd-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="640cd-106">フォームの情報を別のオブジェクトに保持することにより、フォームライブラリプロバイダーは、フォームをアクティブ化せずに、フォームをクライアントに対して記述することができます。</span><span class="sxs-lookup"><span data-stu-id="640cd-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="640cd-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="640cd-107">Header file:</span></span>  <br/> |<span data-ttu-id="640cd-108">Mapiform</span><span class="sxs-lookup"><span data-stu-id="640cd-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="640cd-109">公開者:</span><span class="sxs-lookup"><span data-stu-id="640cd-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="640cd-110">フォーム情報オブジェクト</span><span class="sxs-lookup"><span data-stu-id="640cd-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="640cd-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="640cd-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="640cd-112">フォームライブラリプロバイダー</span><span class="sxs-lookup"><span data-stu-id="640cd-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="640cd-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="640cd-113">Called by:</span></span>  <br/> |<span data-ttu-id="640cd-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="640cd-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="640cd-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="640cd-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="640cd-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="640cd-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="640cd-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="640cd-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="640cd-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="640cd-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="640cd-119">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="640cd-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="640cd-120">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="640cd-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="640cd-121">v の順序</span><span class="sxs-lookup"><span data-stu-id="640cd-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="640cd-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="640cd-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="640cd-123">フォームが使用するプロパティの完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="640cd-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="640cd-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="640cd-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="640cd-125">フォームが使用する動詞の完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="640cd-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="640cd-126">makeiconfrombinary</span><span class="sxs-lookup"><span data-stu-id="640cd-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="640cd-127">フォームの icon プロパティからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="640cd-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="640cd-128">saveform</span><span class="sxs-lookup"><span data-stu-id="640cd-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="640cd-129">構成ファイルに特定のフォームの説明を保存します。</span><span class="sxs-lookup"><span data-stu-id="640cd-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="640cd-130">openformcontainer</span><span class="sxs-lookup"><span data-stu-id="640cd-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="640cd-131">特定のフォームがインストールされているフォームコンテナーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="640cd-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="640cd-132">解説</span><span class="sxs-lookup"><span data-stu-id="640cd-132">Remarks</span></span>

<span data-ttu-id="640cd-133">MapiForm ヘッダーファイルで定義されているほとんどのインターフェイスとは異なり、 **imapiforminfo**は imapiprop [:: GetProps](imapiprop-getprops.md)メソッドへの呼び出しを使用してほとんどのフォーム情報をエクスポートするため、imapiprop インターフェイスから継承します。 [](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="640cd-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="640cd-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="640cd-134">See also</span></span>



[<span data-ttu-id="640cd-135">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="640cd-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

