---
title: 新しい作成フォームの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 66aa5fe08b1c0be3906fa9a0483bbdec37c095c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564501"
---
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="d1d97-103">新しい作成フォームの起動</span><span class="sxs-lookup"><span data-stu-id="d1d97-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="d1d97-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1d97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1d97-105">フォーム サーバーの実装は次の一連のフォームのサーバーへのメソッド呼び出しを期待する必要があり、フォーム オブジェクトの場合、クライアント アプリケーションを作成するための新しいメッセージを開きます。</span><span class="sxs-lookup"><span data-stu-id="d1d97-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="d1d97-106">クライアント アプリケーションは、フォームのサーバーのメッセージ クラスのクラス情報を取得する[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d1d97-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="d1d97-107">クライアント アプリケーションは、新しいフォーム オブジェクトを取得する[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d1d97-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="d1d97-108">MAPI フォーム マネージャーでは、フォームのサーバーから[IMAPIForm](imapiformiunknown.md)インターフェイスを取得し、メモリ、されていない場合は、フォーム サーバーが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="d1d97-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="d1d97-109">クライアント アプリケーションは、結果として得られる**IMAPIForm**インタ フェースし、オブジェクトの[IPersistMessage](ipersistmessageiunknown.md)インターフェイスを取得する[IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d1d97-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="d1d97-110">クライアント アプリケーションでは、 [IMessage](imessageimapiprop.md)、ビュー コンテキスト、フォーム オブジェクトに関連付けると、アドバイズ シンク オブジェクトの[IPersistMessage::InitNew](ipersistmessage-initnew.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d1d97-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="d1d97-111">クライアント アプリケーションでは、開いている動詞を呼び出すための[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d1d97-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d1d97-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1d97-112">See also</span></span>



[<span data-ttu-id="d1d97-113">フォーム サーバーの相互作用</span><span class="sxs-lookup"><span data-stu-id="d1d97-113">Form Server Interactions</span></span>](form-server-interactions.md)

