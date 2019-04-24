---
title: 新規作成フォームの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270057"
---
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="f044a-103">新規作成フォームの起動</span><span class="sxs-lookup"><span data-stu-id="f044a-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="f044a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f044a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f044a-105">フォームサーバーの実装者は、クライアントアプリケーションが新しいメッセージを作成するときに、次のようなメソッド呼び出しをフォームサーバーとフォームオブジェクトに対して実行することを前提としています。</span><span class="sxs-lookup"><span data-stu-id="f044a-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="f044a-106">クライアントアプリケーションは、 [imapiformmgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出して、フォームサーバーのメッセージクラスに関するクラス情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="f044a-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="f044a-107">クライアントアプリケーションは、 [imapiformmgr:: CreateForm](imapiformmgr-createform.md)を呼び出して、新しい form オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="f044a-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="f044a-108">MAPI フォームマネージャーが、まだメモリにない場合はフォームサーバーを読み込み、フォームサーバーから[imapiform](imapiformiunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="f044a-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="f044a-109">クライアントアプリケーションは、生成された**imapiform**インターフェイスを受け取り、 [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出して、オブジェクトの[IPersistMessage](ipersistmessageiunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="f044a-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="f044a-110">クライアントアプリケーションは、 [IPersistMessage:: InitNew](ipersistmessage-initnew.md)メソッドを呼び出して、form オブジェクトを[IMessage](imessageimapiprop.md)、ビューコンテキスト、およびアドバイズシンクオブジェクトに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f044a-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="f044a-111">クライアントアプリケーションは、 [imapiform::D overb](imapiform-doverb.md)メソッドを呼び出して open 動詞を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f044a-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f044a-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="f044a-112">See also</span></span>



[<span data-ttu-id="f044a-113">フォームサーバーの相互作用</span><span class="sxs-lookup"><span data-stu-id="f044a-113">Form Server Interactions</span></span>](form-server-interactions.md)

