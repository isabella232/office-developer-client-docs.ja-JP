---
title: MAPI カスタム フォーム オブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4c1c04e5b04be9bb67b050f5cf498be89d380410
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318248"
---
# <a name="mapi-custom-form-objects"></a><span data-ttu-id="845cd-103">MAPI カスタム フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="845cd-103">MAPI custom form objects</span></span>
  
<span data-ttu-id="845cd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="845cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="845cd-105">カスタム フォームのオブジェクトは、次の 3 つの異なるコンポーネントによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="845cd-105">Objects for custom forms are implemented by three different components:</span></span>
  
- <span data-ttu-id="845cd-106">フォーム サーバー。</span><span class="sxs-lookup"><span data-stu-id="845cd-106">A form server.</span></span>
    
- <span data-ttu-id="845cd-107">フォーム ライブラリ プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="845cd-107">A form library provider.</span></span>
    
- <span data-ttu-id="845cd-108">フォーム ビューアー。</span><span class="sxs-lookup"><span data-stu-id="845cd-108">A form viewer.</span></span>
    
<span data-ttu-id="845cd-109">フォーム サーバーは、OLE 複合ドキュメント オブジェクト アプリケーションと機能が似ています。</span><span class="sxs-lookup"><span data-stu-id="845cd-109">A form server is similar in functionality to an OLE compound document object application.</span></span> <span data-ttu-id="845cd-110">フォームを実装する実行可能コンポーネントです。表示と、ユーザーが実行できる操作を制御します。</span><span class="sxs-lookup"><span data-stu-id="845cd-110">It is an executable component that implements the form; it controls its display and the operations that a user can perform.</span></span> <span data-ttu-id="845cd-111">MAPI は、ユーザーがフォーム サーバーでサポートされているフォームを使用して表示されるメッセージ クラスと共にメッセージを表示する場合に、要求に応じてフォーム サーバーを起動します。</span><span class="sxs-lookup"><span data-stu-id="845cd-111">MAPI starts a form server upon request when a user wants to view a message together with a message class that is displayed by using a form supported by the form server.</span></span> <span data-ttu-id="845cd-112">フォーム サーバーは、標準の OLE クラス ファクトリに似たフォーム ファクトリ オブジェクト、フォーム固有のイベントを処理するためのフォームアドバイスシンク、フォーム自体の 3 つのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="845cd-112">Form servers implement three objects: a form factory object that resembles the standard OLE class factory, a form advise sink for handling form-specific events, and the form itself.</span></span> 
  
<span data-ttu-id="845cd-113">フォーム ライブラリ プロバイダーは、クライアントに対して、フォームのプロパティ セット、コンテナー、および特定のクラスのメッセージをそのクラスのフォームを開くことができるサーバーにリンクするオブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="845cd-113">A form library provider supplies access for clients to a form's property set, to its container, and to the object that links messages of a specific class to the server that can open the form for that class.</span></span> <span data-ttu-id="845cd-114">フォーム ライブラリ プロバイダーは、フォーム情報オブジェクト、フォーム コンテナー、およびメッセージのクラスに基づいて適切なフォーム サーバーにメッセージをバインドするためのフォーム マネージャーの 3 つのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="845cd-114">Form library providers implement three objects: a form information object, a form container, and a form manager for binding a message to the appropriate form server based on the message's class.</span></span>
  
<span data-ttu-id="845cd-115">フォーム ビューアーは、フォルダー ビューアーでのカスタム フォームの表示をサポートするクライアントに含まれるコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="845cd-115">A form viewer is a component that is included in clients that support the display of custom forms in their folder viewers.</span></span> <span data-ttu-id="845cd-116">フォーム ビューアーは、フォーム ライブラリ プロバイダーやフォーム サーバーと同様に、独立した MAPI コンポーネントではありません。</span><span class="sxs-lookup"><span data-stu-id="845cd-116">Form viewers are not independent MAPI components, as are form library providers and form servers.</span></span> <span data-ttu-id="845cd-117">フォーム ビューアーはフォーム サーバーを起動し、コンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="845cd-117">Form viewers start form servers and provide context for them.</span></span> <span data-ttu-id="845cd-118">フォーム ビューアーは、メッセージ サイト、ビュー コンテキスト、およびビュー固有のイベントを処理するためのアドバイス シンクの 3 つのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="845cd-118">Form viewers implement three objects: a message site, a view context, and an advise sink for handling view-specific events.</span></span>
  
<span data-ttu-id="845cd-119">次の表では、すべてのカスタム フォーム オブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="845cd-119">The following table describes all of the custom form objects.</span></span> 
  
|<span data-ttu-id="845cd-120">**Form オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="845cd-120">**Form object**</span></span>|<span data-ttu-id="845cd-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="845cd-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="845cd-122">フォーム</span><span class="sxs-lookup"><span data-stu-id="845cd-122">Form</span></span>  <br/> |<span data-ttu-id="845cd-123">特定のクラスのメッセージを表示するカスタム フォームの表示と操作を制御します。</span><span class="sxs-lookup"><span data-stu-id="845cd-123">Controls the display and operation of a custom form for viewing messages of a specific class.</span></span>  <br/> |
|<span data-ttu-id="845cd-124">フォームのアドバイス シンク</span><span class="sxs-lookup"><span data-stu-id="845cd-124">Form advise sink</span></span>  <br/> |<span data-ttu-id="845cd-125">フォーム ビューアーからの通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="845cd-125">Handles notifications from the form viewer.</span></span>  <br/> |
|<span data-ttu-id="845cd-126">フォーム ファクトリ</span><span class="sxs-lookup"><span data-stu-id="845cd-126">Form factory</span></span>  <br/> |<span data-ttu-id="845cd-127">フォームのインスタンスを作成し、そのサーバーがメモリ内に残ります。</span><span class="sxs-lookup"><span data-stu-id="845cd-127">Creates an instance of a form and allows its server to remain in memory.</span></span>  <br/> |
|<span data-ttu-id="845cd-128">フォーム コンテナー</span><span class="sxs-lookup"><span data-stu-id="845cd-128">Form container</span></span>  <br/> |<span data-ttu-id="845cd-129">フォーム情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="845cd-129">Contains form information.</span></span>  <br/> |
|<span data-ttu-id="845cd-130">フォーム情報</span><span class="sxs-lookup"><span data-stu-id="845cd-130">Form information</span></span>  <br/> |<span data-ttu-id="845cd-131">メッセージと他のメッセージ コンテナーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="845cd-131">Contains messages and other message containers.</span></span>  <br/> |
|<span data-ttu-id="845cd-132">フォーム マネージャー</span><span class="sxs-lookup"><span data-stu-id="845cd-132">Form manager</span></span>  <br/> |<span data-ttu-id="845cd-133">インストールされているすべてのフォームに関連するカスタム フォーム情報の統合ビューへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="845cd-133">Provides access to an integrated view of custom form information that is related to all of the installed forms.</span></span> <span data-ttu-id="845cd-134">また、メッセージ クラスと対応するフォーム クラス識別子を一致します。</span><span class="sxs-lookup"><span data-stu-id="845cd-134">Also matches message classes with corresponding form class identifiers.</span></span>  <br/> |
|<span data-ttu-id="845cd-135">メッセージ サイト</span><span class="sxs-lookup"><span data-stu-id="845cd-135">Message site</span></span>  <br/> |<span data-ttu-id="845cd-136">クライアント内部からのフォーム オブジェクトの操作を処理し、フォーム マネージャー オブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="845cd-136">Handles the manipulation of form objects from inside the client, and provides access to a form manager object.</span></span>  <br/> |
|<span data-ttu-id="845cd-137">コンテキストの表示</span><span class="sxs-lookup"><span data-stu-id="845cd-137">View context</span></span>  <br/> |<span data-ttu-id="845cd-138">次のメッセージと以前のメッセージをアクティブ化し、保存または印刷するフォーム コマンドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="845cd-138">Supports form commands for activating next and previous messages and for saving or printing.</span></span>  <br/> |
|<span data-ttu-id="845cd-139">View アアドバイス シンク</span><span class="sxs-lookup"><span data-stu-id="845cd-139">View advise sink</span></span>  <br/> |<span data-ttu-id="845cd-140">フォーム サーバーからの通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="845cd-140">Handles notifications from the form server.</span></span>  <br/> |
   
<span data-ttu-id="845cd-141">次の図は、カスタム フォーム コンポーネント、実装するオブジェクトとインターフェイス、およびオブジェクトのユーザーであるコンポーネントの関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="845cd-141">The following illustration shows the relationship between custom form components, the objects and interfaces that they implement, and the components that are users of the objects.</span></span> <span data-ttu-id="845cd-142">他のほとんどの MAPI オブジェクトとは異なり、フォーム オブジェクトは直接継承によって関連付けされない 2 つのインターフェイスを実装しています。</span><span class="sxs-lookup"><span data-stu-id="845cd-142">Notice that, unlike most other MAPI objects, the form object implements two interfaces that are not related by direct inheritance.</span></span> <span data-ttu-id="845cd-143">オブジェクトが複数の独立したインターフェイスを公開すると、1 つのインターフェイスへのポインターを持つオブジェクトのユーザーは、他のインターフェイスへのポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="845cd-143">When an object exposes multiple independent interfaces, a user of the object that has a pointer to one of the interfaces can retrieve a pointer to any of the other interfaces.</span></span> <span data-ttu-id="845cd-144">オブジェクトのインターフェイス実装間を移動する機能は [、IUnknown::QueryInterface メソッドの機能](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) です。</span><span class="sxs-lookup"><span data-stu-id="845cd-144">This ability to navigate between an object's interface implementations is a feature of the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> 
  
<span data-ttu-id="845cd-145">**カスタム フォーム コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="845cd-145">**Custom form components**</span></span>
  
<span data-ttu-id="845cd-146">![カスタム フォーム コンポーネント](media/amapi_67.gif "カスタム フォーム コンポーネント")</span><span class="sxs-lookup"><span data-stu-id="845cd-146">![Custom form components](media/amapi_67.gif "Custom form components")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="845cd-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="845cd-147">See also</span></span>

- [<span data-ttu-id="845cd-148">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="845cd-148">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

