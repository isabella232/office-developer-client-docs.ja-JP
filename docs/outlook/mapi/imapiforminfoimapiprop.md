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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b2abf4440ee2d81a8e95dcdb5fde2daeaa6e6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575911"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="604e3-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="604e3-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="604e3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="604e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="604e3-105">フォームの定義には特定のプロパティには、クライアント アプリケーション アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="604e3-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="604e3-106">フォームの情報を保持する別のオブジェクトに、フォーム ライブラリのプロバイダーは、フォームをアクティブにすることがなくクライアントにフォームを記述できます。</span><span class="sxs-lookup"><span data-stu-id="604e3-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="604e3-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="604e3-107">Header file:</span></span>  <br/> |<span data-ttu-id="604e3-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="604e3-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="604e3-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="604e3-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="604e3-110">フォーム オブジェクトの情報</span><span class="sxs-lookup"><span data-stu-id="604e3-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="604e3-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="604e3-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="604e3-112">フォーム ライブラリのプロバイダー</span><span class="sxs-lookup"><span data-stu-id="604e3-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="604e3-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="604e3-113">Called by:</span></span>  <br/> |<span data-ttu-id="604e3-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="604e3-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="604e3-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="604e3-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="604e3-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="604e3-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="604e3-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="604e3-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="604e3-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="604e3-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="604e3-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="604e3-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="604e3-120">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="604e3-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="604e3-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="604e3-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="604e3-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="604e3-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="604e3-123">フォームを使用するプロパティの完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="604e3-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="604e3-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="604e3-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="604e3-125">フォームを使用する動詞の完全なセットへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="604e3-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="604e3-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="604e3-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="604e3-127">フォームのアイコンのプロパティからアイコンを作成します。</span><span class="sxs-lookup"><span data-stu-id="604e3-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="604e3-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="604e3-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="604e3-129">構成ファイル内の特定のフォームの説明を保存します。</span><span class="sxs-lookup"><span data-stu-id="604e3-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="604e3-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="604e3-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="604e3-131">特定のフォームがインストールされているフォームのコンテナーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="604e3-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="604e3-132">注釈</span><span class="sxs-lookup"><span data-stu-id="604e3-132">Remarks</span></span>

<span data-ttu-id="604e3-133">MapiForm.h ヘッダー ファイルで定義されているほとんどのインタ フェースとは異なり、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの呼び出しを通じてほとんどのフォームの情報をエクスポートするため**IMAPIFormInfo**を[IMAPIProp](imapipropiunknown.md)インターフェイスから継承します。</span><span class="sxs-lookup"><span data-stu-id="604e3-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="604e3-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="604e3-134">See also</span></span>



[<span data-ttu-id="604e3-135">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="604e3-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

