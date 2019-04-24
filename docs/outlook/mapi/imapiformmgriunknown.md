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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321652"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="d6fde-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6fde-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="d6fde-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6fde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6fde-105">フォームビューアーがフォームサーバーに関する情報を取得し、アクティブ化できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d6fde-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6fde-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d6fde-106">Header file:</span></span>  <br/> |<span data-ttu-id="d6fde-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="d6fde-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="d6fde-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="d6fde-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="d6fde-109">フォームマネージャーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="d6fde-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="d6fde-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="d6fde-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d6fde-111">フォームライブラリプロバイダー</span><span class="sxs-lookup"><span data-stu-id="d6fde-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="d6fde-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d6fde-112">Called by:</span></span>  <br/> |<span data-ttu-id="d6fde-113">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="d6fde-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="d6fde-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="d6fde-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d6fde-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="d6fde-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="d6fde-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="d6fde-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="d6fde-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="d6fde-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d6fde-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="d6fde-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d6fde-119">loadform</span><span class="sxs-lookup"><span data-stu-id="d6fde-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="d6fde-120">既存のメッセージを開くフォームを開始します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="d6fde-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="d6fde-122">form コンテナー内のフォームに対してメッセージクラスを解決し、そのフォームのフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d6fde-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="d6fde-124">フォームコンテナー内のフォームに対するメッセージクラスのグループを解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="d6fde-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="d6fde-126">フォームのグループが使用するプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="d6fde-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="d6fde-128">フォームのメッセージクラスに基づいて新しいメッセージを作成するためのフォームを起動します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-129">selectform</span><span class="sxs-lookup"><span data-stu-id="d6fde-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="d6fde-130">ユーザーがフォームを選択できるようにするダイアログボックスを表示し、そのフォームを記述するフォーム情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-131">select多重フォーム</span><span class="sxs-lookup"><span data-stu-id="d6fde-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="d6fde-132">ユーザーが複数のフォームを選択できるようにするダイアログボックスを表示し、それらのフォームを記述するフォーム情報オブジェクトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-133">selectformcontainer</span><span class="sxs-lookup"><span data-stu-id="d6fde-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="d6fde-134">ユーザーがフォームコンテナーを選択できるようにするダイアログボックスを提供し、ユーザーが選択したコンテナーオブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-135">openformcontainer</span><span class="sxs-lookup"><span data-stu-id="d6fde-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="d6fde-136">特定のフォームコンテナーの[imapiformcontainer](imapiformcontaineriunknown.md)インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="d6fde-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="d6fde-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="d6fde-138">開くフォームをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="d6fde-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="d6fde-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="d6fde-140">フォームが独自のメッセージ競合を処理できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="d6fde-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="d6fde-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="d6fde-142">フォームマネージャーオブジェクトに発生する前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="d6fde-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6fde-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6fde-143">See also</span></span>



[<span data-ttu-id="d6fde-144">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="d6fde-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

