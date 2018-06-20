---
title: MAPI オブジェクトのユーザー設定フォーム
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ecb40262959834ec511601ec3176887c919d944f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801346"
---
# <a name="mapi-custom-form-objects"></a><span data-ttu-id="aa3c3-103">MAPI オブジェクトのユーザー設定フォーム</span><span class="sxs-lookup"><span data-stu-id="aa3c3-103">MAPI custom form objects</span></span>
  
<span data-ttu-id="aa3c3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa3c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa3c3-105">カスタム フォームのオブジェクトは、3 つの異なるコンポーネントによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-105">Objects for custom forms are implemented by three different components:</span></span>
  
- <span data-ttu-id="aa3c3-106">フォーム サーバーです。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-106">A form server.</span></span>
    
- <span data-ttu-id="aa3c3-107">フォーム ライブラリのプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-107">A form library provider.</span></span>
    
- <span data-ttu-id="aa3c3-108">フォーム ビューアーです。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-108">A form viewer.</span></span>
    
<span data-ttu-id="aa3c3-109">フォーム サーバーは、OLE 複合ドキュメント オブジェクト アプリケーションの機能に似ています。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-109">A form server is similar in functionality to an OLE compound document object application.</span></span> <span data-ttu-id="aa3c3-110">フォームを実装する実行可能ファイルのコンポーネントします。表示とユーザーが実行できる操作を制御します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-110">It is an executable component that implements the form; it controls its display and the operations that a user can perform.</span></span> <span data-ttu-id="aa3c3-111">MAPI は、ユーザーがフォームのサーバーでサポートされているフォームを使用して表示されているメッセージ クラスとメッセージを表示するときに、要求時にフォームのサーバを起動します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-111">MAPI starts a form server upon request when a user wants to view a message together with a message class that is displayed by using a form supported by the form server.</span></span> <span data-ttu-id="aa3c3-112">フォームのサーバー実装の 3 つのオブジェクト: フォーム クラスの工場出荷時に標準的な OLE のようなフォームのファクトリ オブジェクト、フォーム固有のイベント、およびフォーム自体を処理するためのシンクをアドバイスします。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-112">Form servers implement three objects: a form factory object that resembles the standard OLE class factory, a form advise sink for handling form-specific events, and the form itself.</span></span> 
  
<span data-ttu-id="aa3c3-113">フォーム ライブラリのプロバイダーは、クライアント フォームのプロパティのセット、コンテナー、およびそのクラスのフォームを開くことができるサーバーに特定のクラスのメッセージをリンクしているオブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-113">A form library provider supplies access for clients to a form's property set, to its container, and to the object that links messages of a specific class to the server that can open the form for that class.</span></span> <span data-ttu-id="aa3c3-114">フォーム ライブラリ プロバイダー実装の 3 つのオブジェクト: フォーム情報のオブジェクト、フォームのコンテナー、およびメッセージをメッセージのクラスに基づくフォームが適切なサーバーにバインドするためのフォーム マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-114">Form library providers implement three objects: a form information object, a form container, and a form manager for binding a message to the appropriate form server based on the message's class.</span></span>
  
<span data-ttu-id="aa3c3-115">フォーム ビューアーは、そのフォルダーのあるユーザーのユーザー設定フォームの表示をサポートしているクライアントに含まれるコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-115">A form viewer is a component that is included in clients that support the display of custom forms in their folder viewers.</span></span> <span data-ttu-id="aa3c3-116">フォーム ビューアーは、フォーム ライブラリのプロバイダー、およびフォームのサーバー、独立の MAPI コンポーネントではありません。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-116">Form viewers are not independent MAPI components, as are form library providers and form servers.</span></span> <span data-ttu-id="aa3c3-117">フォームの閲覧者は、フォーム サーバーを起動し、それらのコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-117">Form viewers start form servers and provide context for them.</span></span> <span data-ttu-id="aa3c3-118">フォームの閲覧者は、3 つのオブジェクトを実装します。 メッセージ サイト、ビュー コンテキスト、およびビューに固有のイベントを処理するアドバイズ シンクします。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-118">Form viewers implement three objects: a message site, a view context, and an advise sink for handling view-specific events.</span></span>
  
<span data-ttu-id="aa3c3-119">次の表では、すべてのユーザー設定のフォーム オブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-119">The following table describes all of the custom form objects.</span></span> 
  
|<span data-ttu-id="aa3c3-120">**フォーム オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="aa3c3-120">**Form object**</span></span>|<span data-ttu-id="aa3c3-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="aa3c3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa3c3-122">[Form/フォーム]</span><span class="sxs-lookup"><span data-stu-id="aa3c3-122">Form</span></span>  <br/> |<span data-ttu-id="aa3c3-123">表示およびユーザー設定フォームの特定のクラスのメッセージを表示するための操作を制御します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-123">Controls the display and operation of a custom form for viewing messages of a specific class.</span></span>  <br/> |
|<span data-ttu-id="aa3c3-124">フォームのアドバイズ シンク</span><span class="sxs-lookup"><span data-stu-id="aa3c3-124">Form advise sink</span></span>  <br/> |<span data-ttu-id="aa3c3-125">フォーム ビューアーからの通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-125">Handles notifications from the form viewer.</span></span>  <br/> |
|<span data-ttu-id="aa3c3-126">フォーム工場</span><span class="sxs-lookup"><span data-stu-id="aa3c3-126">Form factory</span></span>  <br/> |<span data-ttu-id="aa3c3-127">フォームのインスタンスを作成し、メモリ内に存続するには、そのサーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-127">Creates an instance of a form and allows its server to remain in memory.</span></span>  <br/> |
|<span data-ttu-id="aa3c3-128">フォームのコンテナー</span><span class="sxs-lookup"><span data-stu-id="aa3c3-128">Form container</span></span>  <br/> |<span data-ttu-id="aa3c3-129">フォームの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-129">Contains form information.</span></span>  <br/> |
|<span data-ttu-id="aa3c3-130">フォーム情報</span><span class="sxs-lookup"><span data-stu-id="aa3c3-130">Form information</span></span>  <br/> |<span data-ttu-id="aa3c3-131">メッセージおよびその他のメッセージのコンテナーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-131">Contains messages and other message containers.</span></span>  <br/> |
|<span data-ttu-id="aa3c3-132">フォーム マネージャー</span><span class="sxs-lookup"><span data-stu-id="aa3c3-132">Form manager</span></span>  <br/> |<span data-ttu-id="aa3c3-133">すべてのインストールされているフォームに関連付けられているユーザー設定フォーム情報の統合のビューへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-133">Provides access to an integrated view of custom form information that is related to all of the installed forms.</span></span> <span data-ttu-id="aa3c3-134">メッセージ クラスに対応するフォームのクラス識別子とも一致します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-134">Also matches message classes with corresponding form class identifiers.</span></span>  <br/> |
|<span data-ttu-id="aa3c3-135">メッセージ サイト</span><span class="sxs-lookup"><span data-stu-id="aa3c3-135">Message site</span></span>  <br/> |<span data-ttu-id="aa3c3-136">クライアント内からフォームのオブジェクトの操作を処理し、フォーム マネージャー オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-136">Handles the manipulation of form objects from inside the client, and provides access to a form manager object.</span></span>  <br/> |
|<span data-ttu-id="aa3c3-137">ビュー コンテキスト</span><span class="sxs-lookup"><span data-stu-id="aa3c3-137">View context</span></span>  <br/> |<span data-ttu-id="aa3c3-138">サポートは、次または前のメッセージをアクティブ化するため、保存または印刷するためのコマンドを形成します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-138">Supports form commands for activating next and previous messages and for saving or printing.</span></span>  <br/> |
|<span data-ttu-id="aa3c3-139">ビューのアドバイズ シンク</span><span class="sxs-lookup"><span data-stu-id="aa3c3-139">View advise sink</span></span>  <br/> |<span data-ttu-id="aa3c3-140">フォームのサーバーからの通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-140">Handles notifications from the form server.</span></span>  <br/> |
   
<span data-ttu-id="aa3c3-141">次の図は、カスタム フォームのコンポーネント、オブジェクトと、実装するインターフェイス、およびオブジェクトのユーザーは、コンポーネント間の関係を示します。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-141">The following illustration shows the relationship between custom form components, the objects and interfaces that they implement, and the components that are users of the objects.</span></span> <span data-ttu-id="aa3c3-142">、他のほとんどの MAPI オブジェクトとは異なり、フォーム オブジェクトを実装する直接の継承関係のない 2 つのインターフェイスに注意してください。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-142">Notice that, unlike most other MAPI objects, the form object implements two interfaces that are not related by direct inheritance.</span></span> <span data-ttu-id="aa3c3-143">オブジェクトは、複数の独立したインターフェイスを公開する場合、インタ フェースのいずれかにポインターを持っているオブジェクトのユーザーは、他のインターフェイスのいずれかへのポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-143">When an object exposes multiple independent interfaces, a user of the object that has a pointer to one of the interfaces can retrieve a pointer to any of the other interfaces.</span></span> <span data-ttu-id="aa3c3-144">オブジェクトのインターフェイスの実装の間で移動するには、この機能は、 [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドの機能です。</span><span class="sxs-lookup"><span data-stu-id="aa3c3-144">This ability to navigate between an object's interface implementations is a feature of the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> 
  
<span data-ttu-id="aa3c3-145">**カスタム フォームのコンポーネント**</span><span class="sxs-lookup"><span data-stu-id="aa3c3-145">**Custom form components**</span></span>
  
<span data-ttu-id="aa3c3-146">![ユーザー設定フォームのコンポーネント](media/amapi_67.gif "ユーザー設定フォームのコンポーネント")</span><span class="sxs-lookup"><span data-stu-id="aa3c3-146">![Custom form components](media/amapi_67.gif "Custom form components")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa3c3-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa3c3-147">See also</span></span>

- [<span data-ttu-id="aa3c3-148">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="aa3c3-148">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

