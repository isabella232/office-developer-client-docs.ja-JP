---
title: メッセージを読むフォームを起動する
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
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="c8ab7-103">メッセージを読むフォームを起動する</span><span class="sxs-lookup"><span data-stu-id="c8ab7-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="c8ab7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8ab7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8ab7-105">フォーム サーバーの実装者は、クライアント アプリケーションがメッセージを読み込むときに、フォーム サーバーとフォーム オブジェクトへのメソッド呼び出しの次のシーケンスを期待する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8ab7-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="c8ab7-106">クライアント アプリケーションは [、MAPIOpenFormMgr](mapiopenformmgr.md) 関数を呼び出してフォーム マネージャーを開きます。</span><span class="sxs-lookup"><span data-stu-id="c8ab7-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="c8ab7-107">クライアント アプリケーションは [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) メソッドを呼び出し [、IMAPIForm](imapiformiunknown.md)を持つオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="c8ab7-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="c8ab7-108">フォーム マネージャーがフォームのアクティブ化に使用されない場合は、フォーム マネージャーがリリースされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c8ab7-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="c8ab7-109">LoadForm の呼び出し **には** 、フォーム マネージャーがフォーム サーバーの実行可能ファイルをインストールしてから進む必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="c8ab7-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="c8ab7-110">必要に応じて、クライアント アプリケーションは [IMAPIViewContext](imapiviewcontextiunknown.md) を準備して、フォーム オブジェクトがフォルダー内の前または次のメッセージを読み込む可能性がある操作を制御できます。</span><span class="sxs-lookup"><span data-stu-id="c8ab7-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="c8ab7-111">クライアント アプリケーションでは [、IMAPIForm::SetViewContext](imapiform-setviewcontext.md) メソッドを使用して **、LoadForm** 呼び出しで設定された既定のビュー コンテキストを変更できます。</span><span class="sxs-lookup"><span data-stu-id="c8ab7-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="c8ab7-112">クライアント アプリケーションは [、IPersistMessage::Load](ipersistmessage-load.md) メソッドを呼び出して、メッセージ データをフォーム オブジェクトに読み込む。</span><span class="sxs-lookup"><span data-stu-id="c8ab7-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="c8ab7-113">クライアント アプリケーションは [IMAPIForm::D oVerb](imapiform-doverb.md) を呼び出して、開いている動詞を呼び出し、オプションの [IMAPIViewContext](imapiviewcontextiunknown.md) インターフェイス ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="c8ab7-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c8ab7-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8ab7-114">See also</span></span>



[<span data-ttu-id="c8ab7-115">フォーム サーバーの操作</span><span class="sxs-lookup"><span data-stu-id="c8ab7-115">Form Server Interactions</span></span>](form-server-interactions.md)

