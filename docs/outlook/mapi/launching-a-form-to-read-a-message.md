---
title: メッセージを読むためのフォームの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 675de7eeda534d8761887cdcb6d5c94a209ca18b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801272"
---
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="35564-103">メッセージを読むためのフォームの起動</span><span class="sxs-lookup"><span data-stu-id="35564-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="35564-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35564-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35564-105">フォーム サーバーの実装では、クライアント アプリケーションがメッセージを読み込むとき、サーバーのフォームとフォーム オブジェクトのメソッド呼び出しの次の順序の期待される結果必要があります。</span><span class="sxs-lookup"><span data-stu-id="35564-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="35564-106">クライアント アプリケーションは、 [MAPIOpenFormMgr](mapiopenformmgr.md)関数を呼び出して、フォーム マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="35564-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="35564-107">クライアント メソッドを呼び出して、 [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) 、 [IMAPIForm](imapiformiunknown.md)を使用してオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="35564-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="35564-108">さらにフォームのアクティブ化を使用しない場合、フォーム マネージャーを解放可能性があります。</span><span class="sxs-lookup"><span data-stu-id="35564-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="35564-109">フォーム マネージャーは、続行する前に、フォームのサーバーの実行可能ファイルをインストールする必要がありますので**LoadForm**への呼び出しは時間がかかることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="35564-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="35564-110">必要に応じて、クライアント アプリケーションでは、フォルダー内の前または次のメッセージをロードするフォーム オブジェクトを引き起こす可能性のあるコントロールの操作に[IMAPIViewContext](imapiviewcontextiunknown.md)を準備できます。</span><span class="sxs-lookup"><span data-stu-id="35564-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="35564-111">クライアント アプリケーションは、 [IMAPIForm::SetViewContext](imapiform-setviewcontext.md)メソッドを使用して、設定された既定のビュー コンテキストを変更するのには**LoadForm**の呼び出しで。</span><span class="sxs-lookup"><span data-stu-id="35564-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="35564-112">クライアント アプリケーションでは、form オブジェクトにメッセージのデータをロードするのには[IPersistMessage::Load](ipersistmessage-load.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="35564-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="35564-113">クライアント アプリケーションでは、省略可能な[IMAPIViewContext](imapiviewcontextiunknown.md)インターフェイス ポインターを渡すこと、開いている動詞を呼び出すには、 [IMAPIForm::DoVerb](imapiform-doverb.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="35564-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="35564-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="35564-114">See also</span></span>



[<span data-ttu-id="35564-115">フォーム サーバーの相互作用</span><span class="sxs-lookup"><span data-stu-id="35564-115">Form Server Interactions</span></span>](form-server-interactions.md)

