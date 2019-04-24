---
title: MAPI カスタムフォームオブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 306d62b1-d541-4039-9759-3903f62e0f26
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4c1c04e5b04be9bb67b050f5cf498be89d380410
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318248"
---
# <a name="mapi-custom-form-objects"></a><span data-ttu-id="6a9bf-103">MAPI カスタムフォームオブジェクト</span><span class="sxs-lookup"><span data-stu-id="6a9bf-103">MAPI custom form objects</span></span>
  
<span data-ttu-id="6a9bf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a9bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a9bf-105">ユーザー設定フォームのオブジェクトは、3つの異なるコンポーネントによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-105">Objects for custom forms are implemented by three different components:</span></span>
  
- <span data-ttu-id="6a9bf-106">フォームサーバー。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-106">A form server.</span></span>
    
- <span data-ttu-id="6a9bf-107">フォームライブラリプロバイダ。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-107">A form library provider.</span></span>
    
- <span data-ttu-id="6a9bf-108">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="6a9bf-108">A form viewer.</span></span>
    
<span data-ttu-id="6a9bf-109">フォームサーバーは、OLE 複合ドキュメントオブジェクトアプリケーションの機能に似ています。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-109">A form server is similar in functionality to an OLE compound document object application.</span></span> <span data-ttu-id="6a9bf-110">フォームを実装する実行可能コンポーネントです。ユーザーが実行できる表示と操作を制御します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-110">It is an executable component that implements the form; it controls its display and the operations that a user can perform.</span></span> <span data-ttu-id="6a9bf-111">MAPI は、フォームサーバーでサポートされているフォームを使用して表示されるメッセージクラスと共にメッセージを表示するときに、要求時にフォームサーバーを開始します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-111">MAPI starts a form server upon request when a user wants to view a message together with a message class that is displayed by using a form supported by the form server.</span></span> <span data-ttu-id="6a9bf-112">フォームサーバーは、標準の OLE クラスファクトリに似たフォームファクトリオブジェクト、フォーム固有のイベントを処理するためのフォームアドバイズシンク、フォーム自体の3つのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-112">Form servers implement three objects: a form factory object that resembles the standard OLE class factory, a form advise sink for handling form-specific events, and the form itself.</span></span> 
  
<span data-ttu-id="6a9bf-113">フォームライブラリプロバイダーは、クライアントへのアクセスをフォームのプロパティセット、そのコンテナー、および特定のクラスのフォームを開くことができるサーバーにそのクラスのメッセージをリンクするオブジェクトに渡します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-113">A form library provider supplies access for clients to a form's property set, to its container, and to the object that links messages of a specific class to the server that can open the form for that class.</span></span> <span data-ttu-id="6a9bf-114">フォームライブラリプロバイダーは、フォーム情報オブジェクト、フォームコンテナー、およびメッセージをメッセージのクラスに基づいて適切なフォームサーバーにバインドするフォームマネージャーの3つのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-114">Form library providers implement three objects: a form information object, a form container, and a form manager for binding a message to the appropriate form server based on the message's class.</span></span>
  
<span data-ttu-id="6a9bf-115">フォームビューアーは、フォルダービューアーでのユーザー設定フォームの表示をサポートするクライアントに含まれるコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-115">A form viewer is a component that is included in clients that support the display of custom forms in their folder viewers.</span></span> <span data-ttu-id="6a9bf-116">フォームビューアーは、フォームライブラリプロバイダーやフォームサーバーと同様に、独立した MAPI コンポーネントではありません。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-116">Form viewers are not independent MAPI components, as are form library providers and form servers.</span></span> <span data-ttu-id="6a9bf-117">フォームビューアーは、フォームサーバーを起動し、それらのコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-117">Form viewers start form servers and provide context for them.</span></span> <span data-ttu-id="6a9bf-118">フォームビューアーは、メッセージサイト、ビューコンテキスト、およびビュー固有のイベントを処理するためのアドバイズシンクの3つのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-118">Form viewers implement three objects: a message site, a view context, and an advise sink for handling view-specific events.</span></span>
  
<span data-ttu-id="6a9bf-119">次の表では、すべてのカスタムフォームオブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-119">The following table describes all of the custom form objects.</span></span> 
  
|<span data-ttu-id="6a9bf-120">**Form オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="6a9bf-120">**Form object**</span></span>|<span data-ttu-id="6a9bf-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="6a9bf-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a9bf-122">[Form/フォーム]</span><span class="sxs-lookup"><span data-stu-id="6a9bf-122">Form</span></span>  <br/> |<span data-ttu-id="6a9bf-123">特定のクラスのメッセージを表示するためのユーザー設定フォームの表示と操作を制御します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-123">Controls the display and operation of a custom form for viewing messages of a specific class.</span></span>  <br/> |
|<span data-ttu-id="6a9bf-124">フォームアドバイズシンク</span><span class="sxs-lookup"><span data-stu-id="6a9bf-124">Form advise sink</span></span>  <br/> |<span data-ttu-id="6a9bf-125">フォームビューアーからの通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-125">Handles notifications from the form viewer.</span></span>  <br/> |
|<span data-ttu-id="6a9bf-126">フォームファクトリ</span><span class="sxs-lookup"><span data-stu-id="6a9bf-126">Form factory</span></span>  <br/> |<span data-ttu-id="6a9bf-127">フォームのインスタンスを作成し、そのサーバーをメモリ内に残すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-127">Creates an instance of a form and allows its server to remain in memory.</span></span>  <br/> |
|<span data-ttu-id="6a9bf-128">Form コンテナー</span><span class="sxs-lookup"><span data-stu-id="6a9bf-128">Form container</span></span>  <br/> |<span data-ttu-id="6a9bf-129">フォーム情報を含みます。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-129">Contains form information.</span></span>  <br/> |
|<span data-ttu-id="6a9bf-130">フォーム情報</span><span class="sxs-lookup"><span data-stu-id="6a9bf-130">Form information</span></span>  <br/> |<span data-ttu-id="6a9bf-131">メッセージおよびその他のメッセージコンテナーが保存されています。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-131">Contains messages and other message containers.</span></span>  <br/> |
|<span data-ttu-id="6a9bf-132">フォーム マネージャー</span><span class="sxs-lookup"><span data-stu-id="6a9bf-132">Form manager</span></span>  <br/> |<span data-ttu-id="6a9bf-133">インストールされているすべてのフォームに関連するユーザー設定フォーム情報の統合ビューへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-133">Provides access to an integrated view of custom form information that is related to all of the installed forms.</span></span> <span data-ttu-id="6a9bf-134">また、対応するフォームクラス識別子を持つメッセージクラスにも一致します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-134">Also matches message classes with corresponding form class identifiers.</span></span>  <br/> |
|<span data-ttu-id="6a9bf-135">メッセージサイト</span><span class="sxs-lookup"><span data-stu-id="6a9bf-135">Message site</span></span>  <br/> |<span data-ttu-id="6a9bf-136">クライアント内部からフォームオブジェクトの操作を処理し、フォームマネージャーオブジェクトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-136">Handles the manipulation of form objects from inside the client, and provides access to a form manager object.</span></span>  <br/> |
|<span data-ttu-id="6a9bf-137">ビューのコンテキスト</span><span class="sxs-lookup"><span data-stu-id="6a9bf-137">View context</span></span>  <br/> |<span data-ttu-id="6a9bf-138">次および前のメッセージをアクティブにし、保存または印刷するためのフォームコマンドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-138">Supports form commands for activating next and previous messages and for saving or printing.</span></span>  <br/> |
|<span data-ttu-id="6a9bf-139">アドバイズシンクの表示</span><span class="sxs-lookup"><span data-stu-id="6a9bf-139">View advise sink</span></span>  <br/> |<span data-ttu-id="6a9bf-140">フォームサーバーからの通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-140">Handles notifications from the form server.</span></span>  <br/> |
   
<span data-ttu-id="6a9bf-141">次の図は、カスタムフォームコンポーネント、それらが実装するオブジェクトとインターフェイス、およびオブジェクトのユーザーであるコンポーネント間の関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-141">The following illustration shows the relationship between custom form components, the objects and interfaces that they implement, and the components that are users of the objects.</span></span> <span data-ttu-id="6a9bf-142">その他のほとんどの MAPI オブジェクトとは異なり、form オブジェクトは直接的な継承によって関連付けられていない2つのインターフェイスを実装していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-142">Notice that, unlike most other MAPI objects, the form object implements two interfaces that are not related by direct inheritance.</span></span> <span data-ttu-id="6a9bf-143">オブジェクトが複数の独立したインターフェイスを公開する場合、いずれかのインターフェイスへのポインターを持つオブジェクトのユーザーは、他のインターフェイスへのポインターを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-143">When an object exposes multiple independent interfaces, a user of the object that has a pointer to one of the interfaces can retrieve a pointer to any of the other interfaces.</span></span> <span data-ttu-id="6a9bf-144">このオブジェクトのインターフェイス実装間を移動する機能は、 [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドの機能です。</span><span class="sxs-lookup"><span data-stu-id="6a9bf-144">This ability to navigate between an object's interface implementations is a feature of the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> 
  
<span data-ttu-id="6a9bf-145">**カスタム フォーム コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="6a9bf-145">**Custom form components**</span></span>
  
<span data-ttu-id="6a9bf-146">![カスタムフォームコンポーネント](media/amapi_67.gif "カスタムフォームコンポーネント")</span><span class="sxs-lookup"><span data-stu-id="6a9bf-146">![Custom form components](media/amapi_67.gif "Custom form components")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a9bf-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a9bf-147">See also</span></span>

- [<span data-ttu-id="6a9bf-148">MAPI のオブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="6a9bf-148">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

