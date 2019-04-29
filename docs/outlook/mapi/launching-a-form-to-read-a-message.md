---
title: メッセージを読むためのフォームの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425933"
---
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="34683-103">メッセージを読むためのフォームの起動</span><span class="sxs-lookup"><span data-stu-id="34683-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="34683-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34683-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34683-105">フォームサーバーの実装者は、クライアントアプリケーションがメッセージを読み込むときに、次のようなフォームサーバーとフォームオブジェクトのメソッド呼び出しを想定してください。</span><span class="sxs-lookup"><span data-stu-id="34683-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="34683-106">クライアントアプリケーションは、 [MAPIOpenFormMgr](mapiopenformmgr.md)関数への呼び出しを使用してフォームマネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="34683-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="34683-107">クライアントアプリケーションは、 [imapiformmgr:: loadform](imapiformmgr-loadform.md)メソッドを呼び出します。このメソッドは[imapiform](imapiformiunknown.md)を使用してオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="34683-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="34683-108">フォームマネージャーがさらにフォームのアクティブ化に使用されない場合は、今リリースされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="34683-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="34683-109">作業を進める前に、フォームマネージャーがフォームサーバーの実行可能ファイルをインストールする必要がある場合があるため、 **loadform**の呼び出しには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="34683-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="34683-110">必要に応じて、クライアントアプリケーションで[imapiviewcontext](imapiviewcontextiunknown.md)を準備し、form オブジェクトがフォルダー内の前または次のメッセージを読み込むことができる操作を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="34683-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="34683-111">クライアントアプリケーションは、 [imapiform:: setviewcontext](imapiform-setviewcontext.md)メソッドを使用して、 **loadform**呼び出しで設定された既定のビューコンテキストを変更できます。</span><span class="sxs-lookup"><span data-stu-id="34683-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="34683-112">クライアントアプリケーションは、 [IPersistMessage:: Load](ipersistmessage-load.md)メソッドを呼び出して、メッセージデータを form オブジェクトに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="34683-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="34683-113">クライアントアプリケーションは、 [imapiform を呼び出します。:D overb](imapiform-doverb.md)を呼び出して open 動詞を呼び出し、省略可能な[imapiform](imapiviewcontextiunknown.md)インターフェイスポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="34683-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="34683-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="34683-114">See also</span></span>



[<span data-ttu-id="34683-115">フォームサーバーの相互作用</span><span class="sxs-lookup"><span data-stu-id="34683-115">Form Server Interactions</span></span>](form-server-interactions.md)

