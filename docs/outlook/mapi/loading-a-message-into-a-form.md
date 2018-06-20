---
title: フォームにメッセージを読み込む
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d677958b1a429201c05b5195c58bd7462d0f3d37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801277"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="bd976-103">フォームにメッセージを読み込む</span><span class="sxs-lookup"><span data-stu-id="bd976-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="bd976-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd976-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd976-105">フォームのサーバーを使用してフォームに既存のメッセージをロードするには、次の方法のいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="bd976-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="bd976-106">トークンを作成する[IMAPISession::PrepareForm](imapisession-prepareform.md)を呼び出すと[IMAPISession::ShowForm](imapisession-showform.md)フォームを表示し、します。</span><span class="sxs-lookup"><span data-stu-id="bd976-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="bd976-107">[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bd976-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="bd976-108">比較的簡単では、 **PrepareForm** 、 **ShowForm**の戦略を使用するが、フォームは、クライアントに対してはモーダルになります。</span><span class="sxs-lookup"><span data-stu-id="bd976-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="bd976-109">**ShowForm**への呼び出しは、フォームが終了するまでを返さないためにです。</span><span class="sxs-lookup"><span data-stu-id="bd976-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="bd976-110">フォームを非同期的に処理が必要な場合は、この方法を使わないでください。</span><span class="sxs-lookup"><span data-stu-id="bd976-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="bd976-111">メソッドがいくつかのパラメーターを必要とするため、 **LoadForm**戦略を使用するがより困難になります。</span><span class="sxs-lookup"><span data-stu-id="bd976-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="bd976-112">これらのパラメーターは、適切なコンテキストに適切なフォームのサーバーを起動し、適切なメッセージを表示するフォーム マネージャーに指示します。</span><span class="sxs-lookup"><span data-stu-id="bd976-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="bd976-113">フォーム サーバーが既に実行されている場合フォーム マネージャーは、フォームのサーバーの新しいインスタンスを起動しなくてもフォームのサーバーにメッセージを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="bd976-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="bd976-114">フォームを起動するサーバーを指定するには、 _lpszMessageClass_パラメーターの内容で、対象サーバーにより処理されるメッセージのクラスを渡します。</span><span class="sxs-lookup"><span data-stu-id="bd976-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="bd976-115">読み込むメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを取得することによって、適切なメッセージ クラスを確認できます。</span><span class="sxs-lookup"><span data-stu-id="bd976-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="bd976-116">サーバが存在しないフォーム指定したメッセージ クラスのメッセージのスーパークラスに属しているメッセージを処理するフォーム サーバーのみです。</span><span class="sxs-lookup"><span data-stu-id="bd976-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="bd976-117">そのクラスのメッセージを処理するもので具体的には、フォーム サーバーのみがメッセージを読み込むことを使用する場合は、 **LoadForm**の呼び出しで MAPIFORM_EXACTMATCH フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="bd976-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="bd976-118">詳細については、 [MAPI メッセージ クラス](mapi-message-classes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd976-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="bd976-119">**LoadForm**ビューアーのメッセージのサイトとビュー コンテキスト値へのポインターを対象のメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) と**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) も必要です。プロパティです。</span><span class="sxs-lookup"><span data-stu-id="bd976-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

