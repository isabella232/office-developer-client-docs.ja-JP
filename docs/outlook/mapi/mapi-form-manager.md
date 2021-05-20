---
title: MAPI フォーム マネージャー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430197"
---
# <a name="mapi-form-manager"></a><span data-ttu-id="b578a-103">MAPI フォーム マネージャー</span><span class="sxs-lookup"><span data-stu-id="b578a-103">MAPI Form Manager</span></span>

  
  
<span data-ttu-id="b578a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b578a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b578a-105">フォーム マネージャーは [、IMAPIFormMgr インターフェイスを実装するオブジェクト](imapiformmgriunknown.md) です。</span><span class="sxs-lookup"><span data-stu-id="b578a-105">A form manager is an object that implements the [IMAPIFormMgr](imapiformmgriunknown.md) interface.</span></span> <span data-ttu-id="b578a-106">ほとんどの組織では、既定のフォーム マネージャーと呼ばれる MAPI で提供されるフォーム マネージャーを使用します。</span><span class="sxs-lookup"><span data-stu-id="b578a-106">Most organizations will use the form manager supplied with MAPI, referred to as the default form manager.</span></span> <span data-ttu-id="b578a-107">ただし、必要に応じて、組織は既定のフォーム マネージャーをカスタム フォーム マネージャーに置き換える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b578a-107">However, an organization can replace the default form manager with a custom form manager if desired.</span></span> <span data-ttu-id="b578a-108">フォーム マネージャーは、フォーム ライブラリ内のフォームの検索、ユーザーの要求に応じてフォームの読み込み、ユーザーのローカル フォーム ライブラリ、フォルダー フォーム ライブラリ、または個人用フォーム ライブラリへのフォームのインストールを行います。</span><span class="sxs-lookup"><span data-stu-id="b578a-108">The form manager takes care of locating forms within form libraries, loading forms in response to user requests, and installing forms into a user's local form library, folder form library, or personal form library.</span></span> 
  
<span data-ttu-id="b578a-109">ユーザーがメッセージを操作するには、メッセージのメッセージ クラス用のフォーム サーバーのインスタンスを作成してアクティブ化して、メッセージを表示し、要求された操作をメッセージに対して実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b578a-109">For a user to interact with a message, an instance of the form server for the message's message class must be created and activated to display the message and carry out the requested operation on the message.</span></span> <span data-ttu-id="b578a-110">[「MAPI](mapi-form-libraries.md)フォーム ライブラリ」のトピックで説明したように、フォームの実装は複数の異なる場所 (フォーム ライブラリ) に存在する可能性があります。フォームまたはサーバーがローカルで利用可能になるか、ユーザーが操作する場合に実行中の状態になるという保証はありません。</span><span class="sxs-lookup"><span data-stu-id="b578a-110">As described in the topic [MAPI Form Libraries](mapi-form-libraries.md), a form's implementation can exist in several different locations (form libraries) and there is no guarantee that a form or its server will be locally available or in a running state when a user wants to interact with it.</span></span> <span data-ttu-id="b578a-111">フォーム マネージャーは、フォームの検索とアクティブ化の詳細を管理します。</span><span class="sxs-lookup"><span data-stu-id="b578a-111">The form manager takes care of the details of locating and activating the form.</span></span>
  
<span data-ttu-id="b578a-112">クライアントは、フォーム マネージャーが提供するサービスを使用して、フォームを検索およびアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="b578a-112">Clients use services provided by the form manager to find and activate forms.</span></span> <span data-ttu-id="b578a-113">**IMAPIFormMgr** インターフェイスはフォーム マネージャーによって実装され、クライアントがサービスにアクセスするために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b578a-113">The **IMAPIFormMgr** interface is implemented by the form manager and is called by clients to access its services.</span></span> <span data-ttu-id="b578a-114">フォーム マネージャーは、メッセージング クライアントからフォームを検索およびアクティブ化するほとんどすべての詳細を非表示にしています。</span><span class="sxs-lookup"><span data-stu-id="b578a-114">The form manager is an essential component because it hides almost all the details of finding and activating forms from messaging clients.</span></span> 
  
<span data-ttu-id="b578a-115">フォーム サーバーを読み込むときに、既定のフォーム マネージャーは、フォームのメッセージ クラスの実装が見つかった最初のフォーム ライブラリからフォームを読み込む。</span><span class="sxs-lookup"><span data-stu-id="b578a-115">When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found.</span></span> <span data-ttu-id="b578a-116">既定のフォーム マネージャーは、フォーム ライブラリを次の順序で検索します。</span><span class="sxs-lookup"><span data-stu-id="b578a-116">The default form manager searches the form libraries in the following order:</span></span>
  
1. <span data-ttu-id="b578a-117">ユーザーのローカル フォーム ライブラリ。</span><span class="sxs-lookup"><span data-stu-id="b578a-117">The user's local form library.</span></span> <span data-ttu-id="b578a-118">このフォーム ライブラリは、実装がローカル フォーム ライブラリにインストールされている場合、フォームの実装に最も高速にアクセスできるので、最初に検索されます。</span><span class="sxs-lookup"><span data-stu-id="b578a-118">This form library is searched first because it provides the fastest access to a form's implementation if the implementation is installed in the local form library.</span></span>
    
2. <span data-ttu-id="b578a-119">メッセージのコンテナーのフォルダー フォーム ライブラリ (読み込まれるメッセージが格納されているフォルダー)。</span><span class="sxs-lookup"><span data-stu-id="b578a-119">The folder form library of the message's container — the folder in which the message being loaded is stored.</span></span>
    
3. <span data-ttu-id="b578a-120">ユーザーの個人用フォーム ライブラリ。</span><span class="sxs-lookup"><span data-stu-id="b578a-120">The user's personal form library.</span></span>
    
<span data-ttu-id="b578a-121">カスタム フォーム マネージャーは、使用可能なフォーム ライブラリを任意の順序で検索したり、組織全体のフォーム ライブラリなどの他のフォーム ライブラリを実装できます。</span><span class="sxs-lookup"><span data-stu-id="b578a-121">A custom form manager can search the available form libraries in any order, or can implement other form libraries such as an organization-wide form library.</span></span> <span data-ttu-id="b578a-122">フォーム ライブラリの詳細については、「MAPI フォーム ライブラリ [」を参照してください](mapi-form-libraries.md)。</span><span class="sxs-lookup"><span data-stu-id="b578a-122">For more details on form libraries, see [MAPI Form Libraries](mapi-form-libraries.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b578a-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b578a-123">See also</span></span>



[<span data-ttu-id="b578a-124">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="b578a-124">MAPI Forms</span></span>](mapi-forms.md)

