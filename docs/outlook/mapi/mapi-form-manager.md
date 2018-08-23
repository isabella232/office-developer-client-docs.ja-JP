---
title: MAPI フォーム マネージャー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f78c25285c7ac3f8736006e4a45079a7d9a6d867
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592298"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="52b01-103">MAPI フォーム マネージャー</span><span class="sxs-lookup"><span data-stu-id="52b01-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="52b01-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52b01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52b01-105">フォーム マネージャーは、 [IMAPIFormMgr](imapiformmgriunknown.md)インターフェイスを実装するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="52b01-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="52b01-106">ほとんどの組織では、付属の既定のフォーム マネージャーと呼ばれる、MAPI フォーム マネージャーを使用します。</span><span class="sxs-lookup"><span data-stu-id="52b01-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="52b01-107">ただし、組織置き換えることが既定のフォーム マネージャーのユーザー設定フォーム マネージャーが必要な場合。</span><span class="sxs-lookup"><span data-stu-id="52b01-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="52b01-108">フォーム ライブラリ内でフォームを検索して、ユーザーの要求への応答としてフォームを読み込み、ユーザーのローカル フォーム ライブラリ、フォルダー フォーム ライブラリまたは個人用フォーム ライブラリにフォームをインストールするのフォーム マネージャーによって行われます。</span><span class="sxs-lookup"><span data-stu-id="52b01-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="52b01-109">メッセージと対話するユーザーのメッセージのメッセージ クラスのフォームのサーバーのインスタンスが作成され、メッセージが表示され、メッセージに対して要求された操作を実行するアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="52b01-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="52b01-110">[MAPI フォーム ライブラリ](mapi-form-libraries.md)のトピックで説明したとおり、フォームの実装はいくつかの別の場所 (フォーム ライブラリ) と、フォームまたはそのサーバーがローカルで使用可能または実行中にユーザーが対話しようとしたときの状態は保証されていませんします。</span><span class="sxs-lookup"><span data-stu-id="52b01-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="52b01-111">検索して、フォームをアクティブ化の詳細] の [フォーム マネージャーによって行われます。</span><span class="sxs-lookup"><span data-stu-id="52b01-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="52b01-112">クライアントは、検索し、フォームをアクティブにするフォームのマネージャーによって提供されるサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="52b01-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="52b01-113">**IMAPIFormMgr**インターフェイスは、フォーム マネージャーによって実装され、そのサービスにアクセスするクライアントによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="52b01-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="52b01-114">フォーム マネージャーは、ほとんどすべての詳細を検索して、メッセージング クライアントからのフォームをアクティブにするが非表示にするために必要不可欠なコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="52b01-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="52b01-115">フォームのサーバーにロードするとき、既定のフォーム マネージャーは、フォームのメッセージ クラスの実装が存在する最初のフォーム ライブラリからフォームを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="52b01-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="52b01-116">既定のフォーム マネージャーは、次の順序で、フォーム ライブラリを検索します。</span><span class="sxs-lookup"><span data-stu-id="52b01-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="52b01-117">ユーザーのローカル フォーム ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="52b01-117">The user's local form library.</span></span> <span data-ttu-id="52b01-118">ローカル フォーム ライブラリの実装がインストールされている場合は、フォームの実装に最も高速なアクセスを提供するため、このフォーム ライブラリを最初に検索します。</span><span class="sxs-lookup"><span data-stu-id="52b01-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="52b01-119">メッセージのコンテナーのフォルダー フォーム ライブラリ: 読み込まれているメッセージが格納されるフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="52b01-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="52b01-120">ユーザーの個人用フォーム ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="52b01-120">The user's personal form library.</span></span>
    
<span data-ttu-id="52b01-121">カスタム フォーム マネージャーは、任意の順序で利用可能なフォーム ライブラリを検索することができます。 または組織用フォーム ライブラリなどの他のフォーム ライブラリを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="52b01-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="52b01-122">フォーム ライブラリの詳細については、 [MAPI フォーム ライブラリ](mapi-form-libraries.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52b01-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52b01-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="52b01-123">See also</span></span>



[<span data-ttu-id="52b01-124">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="52b01-124">MAPI Forms</span></span>](mapi-forms.md)

