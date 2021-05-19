---
title: IMAPIFormInfo IMAPIProp
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417365"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="5d0c4-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5d0c4-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="5d0c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d0c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d0c4-105">クライアント アプリケーションに、フォーム定義に特定のプロパティへのアクセス権を与えます。</span><span class="sxs-lookup"><span data-stu-id="5d0c4-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="5d0c4-106">フォーム情報を別のオブジェクトに保持することで、フォーム ライブラリ プロバイダーは、フォームをアクティブ化せずに、クライアントにフォームを記述できます。</span><span class="sxs-lookup"><span data-stu-id="5d0c4-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d0c4-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5d0c4-107">Header file:</span></span>  <br/> |<span data-ttu-id="5d0c4-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="5d0c4-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="5d0c4-109">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="5d0c4-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="5d0c4-110">フォーム情報オブジェクト</span><span class="sxs-lookup"><span data-stu-id="5d0c4-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="5d0c4-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="5d0c4-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5d0c4-112">フォーム ライブラリ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="5d0c4-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="5d0c4-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5d0c4-113">Called by:</span></span>  <br/> |<span data-ttu-id="5d0c4-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5d0c4-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="5d0c4-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="5d0c4-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5d0c4-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="5d0c4-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="5d0c4-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="5d0c4-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="5d0c4-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="5d0c4-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="5d0c4-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="5d0c4-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="5d0c4-120">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="5d0c4-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5d0c4-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="5d0c4-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5d0c4-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="5d0c4-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="5d0c4-123">フォームで使用されるプロパティの完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5d0c4-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="5d0c4-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="5d0c4-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="5d0c4-125">フォームで使用される動詞の完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5d0c4-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="5d0c4-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="5d0c4-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="5d0c4-127">フォームのアイコン プロパティからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="5d0c4-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="5d0c4-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="5d0c4-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="5d0c4-129">特定のフォームの説明を構成ファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="5d0c4-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="5d0c4-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="5d0c4-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="5d0c4-131">特定のフォームがインストールされているフォーム コンテナーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5d0c4-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d0c4-132">注釈</span><span class="sxs-lookup"><span data-stu-id="5d0c4-132">Remarks</span></span>

<span data-ttu-id="5d0c4-133">MapiForm.h ヘッダー ファイルで定義されているほとんどのインターフェイスとは異なり **、IMAPIFormInfo は IMAPIProp** インターフェイスから継承します。ほとんどのフォーム情報は [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドへの呼び出しによってエクスポートされます。 [](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="5d0c4-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d0c4-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d0c4-134">See also</span></span>



[<span data-ttu-id="5d0c4-135">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="5d0c4-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

