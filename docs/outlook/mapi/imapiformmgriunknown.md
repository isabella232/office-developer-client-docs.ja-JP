---
title: imapiformmgr IUnknown
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
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="4642e-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4642e-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="4642e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4642e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4642e-105">フォームビューアーがフォームサーバーに関する情報を取得し、アクティブ化できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4642e-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4642e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4642e-106">Header file:</span></span>  <br/> |<span data-ttu-id="4642e-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="4642e-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4642e-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="4642e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4642e-109">フォームマネージャーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="4642e-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="4642e-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="4642e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4642e-111">フォームライブラリプロバイダー</span><span class="sxs-lookup"><span data-stu-id="4642e-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="4642e-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="4642e-112">Called by:</span></span>  <br/> |<span data-ttu-id="4642e-113">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="4642e-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="4642e-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="4642e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4642e-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="4642e-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="4642e-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="4642e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4642e-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="4642e-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4642e-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="4642e-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4642e-119">loadform</span><span class="sxs-lookup"><span data-stu-id="4642e-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="4642e-120">既存のメッセージを開くフォームを開始します。</span><span class="sxs-lookup"><span data-stu-id="4642e-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="4642e-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="4642e-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="4642e-122">form コンテナー内のフォームに対してメッセージクラスを解決し、そのフォームのフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="4642e-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="4642e-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="4642e-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="4642e-124">フォームコンテナー内のフォームに対するメッセージクラスのグループを解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="4642e-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="4642e-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="4642e-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="4642e-126">フォームのグループが使用するプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="4642e-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="4642e-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="4642e-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="4642e-128">フォームのメッセージクラスに基づいて新しいメッセージを作成するためのフォームを起動します。</span><span class="sxs-lookup"><span data-stu-id="4642e-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="4642e-129">selectform</span><span class="sxs-lookup"><span data-stu-id="4642e-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="4642e-130">ユーザーがフォームを選択できるようにするダイアログボックスを表示し、そのフォームを記述するフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="4642e-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="4642e-131">select多重フォーム</span><span class="sxs-lookup"><span data-stu-id="4642e-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="4642e-132">ユーザーが複数のフォームを選択できるようにするダイアログボックスを表示し、それらのフォームを記述するフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="4642e-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="4642e-133">selectformcontainer</span><span class="sxs-lookup"><span data-stu-id="4642e-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="4642e-134">ユーザーがフォームコンテナーを選択できるようにするダイアログボックスを提供し、ユーザーが選択したコンテナーオブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="4642e-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="4642e-135">openformcontainer</span><span class="sxs-lookup"><span data-stu-id="4642e-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="4642e-136">特定のフォームコンテナーの[imapiformcontainer](imapiformcontaineriunknown.md)インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="4642e-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="4642e-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="4642e-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="4642e-138">開くフォームをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="4642e-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="4642e-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="4642e-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="4642e-140">フォームが独自のメッセージ競合を処理できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4642e-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="4642e-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="4642e-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="4642e-142">フォームマネージャーオブジェクトに発生する前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="4642e-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4642e-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="4642e-143">See also</span></span>



[<span data-ttu-id="4642e-144">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="4642e-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

