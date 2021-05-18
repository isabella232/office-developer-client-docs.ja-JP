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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412416"
---
# <a name="loading-a-message-into-a-form"></a><span data-ttu-id="3d7c8-103">フォームへのメッセージの読み込み</span><span class="sxs-lookup"><span data-stu-id="3d7c8-103">Loading a Message Into a Form</span></span>

  
  
<span data-ttu-id="3d7c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d7c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d7c8-105">フォーム サーバーを使用して既存のメッセージをフォームに読み込むには、次のいずれかの方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-105">To load an existing message into a form using a form server, use one of the following strategies.</span></span>
  
- <span data-ttu-id="3d7c8-106">[IMAPISession::P repareForm](imapisession-prepareform.md)を呼び出してトークンを作成し、次に[IMAPISession::ShowForm](imapisession-showform.md)を呼び出してフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-106">Call [IMAPISession::PrepareForm](imapisession-prepareform.md) to create a token and then [IMAPISession::ShowForm](imapisession-showform.md) to display the form.</span></span> 
    
- <span data-ttu-id="3d7c8-107">[IMAPIFormMgr::LoadForm を呼び出します](imapiformmgr-loadform.md)。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-107">Call [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md).</span></span> 
    
<span data-ttu-id="3d7c8-108">**PrepareForm と** **ShowForm** 戦略の使用は比較的簡単ですが、クライアントに関してモーダルなフォームになります。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-108">Using the **PrepareForm** and **ShowForm** strategy is comparatively easy, but it results in forms that are modal with respect to your client.</span></span> <span data-ttu-id="3d7c8-109">これは、フォームが終了するまで **ShowForm** の呼び出しが返されないためです。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-109">This is because the call to **ShowForm** does not return until the form has exited.</span></span> <span data-ttu-id="3d7c8-110">フォームを非同期的に処理する必要がある場合は、この戦略を使用しない。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-110">If you need to handle forms asynchronously, do not use this strategy.</span></span> 
  
<span data-ttu-id="3d7c8-111">メソッドには **いくつかのパラメーターが必要なので、LoadForm** 戦略の使用は難しくなります。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-111">Using the **LoadForm** strategy is more difficult because the method requires several parameters.</span></span> <span data-ttu-id="3d7c8-112">これらのパラメーターは、適切なコンテキストで適切なフォーム サーバーを起動し、適切なメッセージを表示するようにフォーム マネージャーに指示します。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-112">These parameters instruct the form manager to launch the proper form server in the proper context and display the proper message.</span></span> <span data-ttu-id="3d7c8-113">フォーム サーバーが既に実行されている場合、フォーム マネージャーは、フォーム サーバーの新しいインスタンスを起動せずに、メッセージをフォーム サーバーに読み込む。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-113">If the form server is already running, the form manager loads the message into the form server without launching a new instance of the form server.</span></span> 
  
<span data-ttu-id="3d7c8-114">起動するフォーム サーバーを指定するには  _、lpszMessageClass_ パラメーターの内容でターゲット サーバーが処理するメッセージ クラスを渡します。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-114">To specify which form server to launch, pass the message class handled by the target server in the contents of the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="3d7c8-115">適切なメッセージ クラスは、読み込むメッセージの PR_MESSAGE_CLASS **(** [PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得することで決定できます。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-115">The appropriate message class can be determined by retrieving the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message to be loaded.</span></span> <span data-ttu-id="3d7c8-116">指定したメッセージ クラスのフォーム サーバーがない場合があります。メッセージのスーパークラスに属するメッセージを処理するフォーム サーバーのみです。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-116">Sometimes there is no form server for the specified message class, only a form server that handles messages belonging to the message's superclass.</span></span> <span data-ttu-id="3d7c8-117">そのクラスのメッセージを処理することを特に意図したフォーム サーバーによってのみメッセージを読み込む場合は **、LoadForm** 呼び出しで MAPIFORM_EXACTMATCH フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-117">If you prefer that the message be loaded only by a form server specifically meant to handle messages of that class, set the MAPIFORM_EXACTMATCH flag in the **LoadForm** call.</span></span> <span data-ttu-id="3d7c8-118">詳細については、「MAPI メッセージ [クラス」を参照してください](mapi-message-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="3d7c8-118">For more information, see [MAPI Message Classes](mapi-message-classes.md).</span></span>
  
 <span data-ttu-id="3d7c8-119">**LoadForm** には、ビューアーのメッセージ サイトへのポインターと、ターゲット メッセージ **の PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティと PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティのコンテキストと値が必要です。 </span><span class="sxs-lookup"><span data-stu-id="3d7c8-119">**LoadForm** also requires a pointer to your viewer's message site and view context and the value for the target message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) and **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) properties.</span></span>
  

