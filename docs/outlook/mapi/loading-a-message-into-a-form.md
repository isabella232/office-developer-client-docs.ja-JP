---
title: フォームへのメッセージの読み込み
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355748"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="2d7c4-103">フォームへのメッセージの読み込み</span><span class="sxs-lookup"><span data-stu-id="2d7c4-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="2d7c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d7c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d7c4-105">フォームサーバーを使用して既存のメッセージをフォームに読み込むには、次のいずれかの方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="2d7c4-106">次のように、imapisession を呼び出します。トークンを作成し、次に、フォームを表示するために[apiapisession:: showform](imapisession-showform.md)を実行するには[:P repareform](imapisession-prepareform.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="2d7c4-107">[imapiformmgr:: loadform](imapiformmgr-loadform.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="2d7c4-108">**PrepareForm**および**showform**戦略は、比較的簡単ですが、クライアントに関してはモーダルであるフォームが生成されます。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="2d7c4-109">これは、 **showform**の呼び出しが、フォームが終了するまで返されないためです。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="2d7c4-110">フォームを非同期的に処理する必要がある場合は、この方法を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="2d7c4-111">メソッドにはいくつかのパラメーターが必要なため、 **loadform**戦略を使用することは困難です。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="2d7c4-112">これらのパラメーターによって、フォームマネージャーは適切なコンテキストで適切なフォームサーバーを起動し、適切なメッセージを表示するように指示されます。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="2d7c4-113">フォームサーバーが既に実行されている場合、フォームマネージャーはフォームサーバーの新しいインスタンスを起動せずに、そのメッセージをフォームサーバーに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="2d7c4-114">起動するフォームサーバーを指定するには、ターゲットサーバーによって処理されるメッセージクラスを_lpszmessageclass_パラメーターの内容で渡します。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="2d7c4-115">適切なメッセージクラスは、読み込まれるメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得することによって判断できます。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="2d7c4-116">指定したメッセージクラスのフォームサーバーがなく、メッセージのスーパークラスに属するメッセージを処理するフォームサーバーだけが存在することもあります。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="2d7c4-117">このクラスのメッセージを処理することを目的としたフォームサーバーのみがメッセージを読み込むことを希望する場合は、 **loadform**呼び出しで MAPIFORM_EXACTMATCH フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="2d7c4-118">詳細については、「 [MAPI メッセージクラス](mapi-message-classes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d7c4-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="2d7c4-119">また、 **loadform**には、ビューアーのメッセージサイトとビューコンテキストへのポインターと、ターゲットメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) および**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) の値を指定する必要があります。プロパティ.</span><span class="sxs-lookup"><span data-stu-id="2d7c4-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

