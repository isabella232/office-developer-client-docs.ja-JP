---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413060"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="d86e6-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d86e6-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="d86e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d86e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d86e6-105">フォーム ビューアーがフォーム サーバーに関する情報を取得し、アクティブ化できます。</span><span class="sxs-lookup"><span data-stu-id="d86e6-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d86e6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d86e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="d86e6-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="d86e6-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="d86e6-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="d86e6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="d86e6-109">フォーム マネージャー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d86e6-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="d86e6-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="d86e6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d86e6-111">フォーム ライブラリ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d86e6-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="d86e6-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d86e6-112">Called by:</span></span>  <br/> |<span data-ttu-id="d86e6-113">フォーム ビューアー</span><span class="sxs-lookup"><span data-stu-id="d86e6-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="d86e6-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="d86e6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d86e6-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="d86e6-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="d86e6-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="d86e6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="d86e6-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="d86e6-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d86e6-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="d86e6-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d86e6-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="d86e6-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="d86e6-120">既存のメッセージを開くフォームを開始します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="d86e6-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="d86e6-122">メッセージ クラスをフォーム コンテナー内のフォームに解決し、そのフォームのフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d86e6-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="d86e6-124">メッセージ クラスのグループをフォーム コンテナー内のフォームに解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="d86e6-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="d86e6-126">フォームのグループが使用するプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="d86e6-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="d86e6-128">フォームを起動して、フォームのメッセージ クラスに基づいて新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="d86e6-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="d86e6-130">ユーザーがフォームを選択できるダイアログ ボックスを表示し、そのフォームを説明するフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="d86e6-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="d86e6-132">ユーザーが複数のフォームを選択できるダイアログ ボックスを表示し、それらのフォームを記述するフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="d86e6-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="d86e6-134">ユーザーがフォーム コンテナーを選択できるダイアログ ボックスを表示し、ユーザーが選択したコンテナー オブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="d86e6-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="d86e6-136">特定の [フォーム コンテナーの IMAPIFormContainer](imapiformcontaineriunknown.md) インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="d86e6-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="d86e6-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="d86e6-138">開くフォームをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="d86e6-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="d86e6-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="d86e6-140">フォームが独自のメッセージ競合を処理できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="d86e6-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="d86e6-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="d86e6-142">フォーム マネージャー オブジェクトに発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="d86e6-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d86e6-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="d86e6-143">See also</span></span>



[<span data-ttu-id="d86e6-144">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="d86e6-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

