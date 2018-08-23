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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b4eaf424bd22f5cb7f40778d81a18cca0ef1dcc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581518"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="ddfc4-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ddfc4-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="ddfc4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddfc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddfc4-105">フォームの閲覧者に関する情報を取得し、フォームのサーバーをアクティブ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddfc4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ddfc4-106">Header file:</span></span>  <br/> |<span data-ttu-id="ddfc4-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="ddfc4-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ddfc4-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ddfc4-109">フォーム マネージャー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ddfc4-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="ddfc4-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ddfc4-111">フォーム ライブラリのプロバイダー</span><span class="sxs-lookup"><span data-stu-id="ddfc4-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="ddfc4-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-112">Called by:</span></span>  <br/> |<span data-ttu-id="ddfc4-113">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="ddfc4-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="ddfc4-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ddfc4-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="ddfc4-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="ddfc4-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ddfc4-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="ddfc4-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ddfc4-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="ddfc4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ddfc4-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="ddfc4-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="ddfc4-120">フォームを開くには既存のメッセージを開始します。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="ddfc4-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="ddfc4-122">フォームのコンテナー内のフォームにメッセージ クラスを解決し、そのフォームのフォームについてはオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="ddfc4-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="ddfc4-124">フォームのコンテナー内でユーザーがフォームにメッセージ クラスのグループを解決し、それらのフォームのオブジェクトの情報、フォームの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="ddfc4-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="ddfc4-126">フォームのグループを使用するプロパティの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="ddfc4-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="ddfc4-128">フォームのメッセージ クラスに基づく新しいメッセージを作成するためのフォームを起動します。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="ddfc4-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="ddfc4-130">、フォームを選択するユーザーを有効にする] ダイアログ ボックスを表示し、そのフォームを記述するフォームの情報オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="ddfc4-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="ddfc4-132">複数のフォームを選択するユーザーを有効にする] ダイアログ ボックスを表示し、それらのフォームを記述するオブジェクトの情報、フォームの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="ddfc4-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="ddfc4-134">により、ユーザーがフォームのコンテナーを選択し、ユーザーが選択したコンテナーのオブジェクトのインターフェイスを返しますダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="ddfc4-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="ddfc4-136">[IMAPIFormContainer](imapiformcontaineriunknown.md)インターフェイスの特定のフォームのコンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="ddfc4-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="ddfc4-138">開始するためのフォームをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="ddfc4-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="ddfc4-140">フォームに独自のメッセージの競合を処理できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="ddfc4-141">発生しました</span><span class="sxs-lookup"><span data-stu-id="ddfc4-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="ddfc4-142">フォーム マネージャー オブジェクトに発生する前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="ddfc4-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ddfc4-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="ddfc4-143">See also</span></span>



[<span data-ttu-id="ddfc4-144">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ddfc4-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

