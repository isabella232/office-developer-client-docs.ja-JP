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
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="c1c66-103">新規作成フォームの起動</span><span class="sxs-lookup"><span data-stu-id="c1c66-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="c1c66-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1c66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1c66-105">フォーム サーバーの実装者は、クライアント アプリケーションが作成用の新しいメッセージを開く際に、フォーム サーバーとフォーム オブジェクトへのメソッド呼び出しの次のシーケンスを期待する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1c66-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="c1c66-106">クライアント アプリケーションは [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) メソッドを呼び出して、フォーム サーバーのメッセージ クラスに関するクラス情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="c1c66-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="c1c66-107">クライアント アプリケーションは [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) を呼び出して新しいフォーム オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="c1c66-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="c1c66-108">MAPI フォーム マネージャーは、まだメモリ内に存在しない場合はフォーム サーバーを読み込み、フォーム サーバーから [IMAPIForm](imapiformiunknown.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="c1c66-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="c1c66-109">クライアント アプリケーションは、結果の **IMAPIForm** インターフェイスを受け取り [、IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) メソッドを呼び出して、オブジェクトの [IPersistMessage インターフェイスを取得](ipersistmessageiunknown.md) します。</span><span class="sxs-lookup"><span data-stu-id="c1c66-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="c1c66-110">クライアント アプリケーションは [、IPersistMessage::InitNew](ipersistmessage-initnew.md) メソッドを呼び出して、フォーム オブジェクトを [IMessage](imessageimapiprop.md)に関連付け、コンテキストを表示し、シンク オブジェクトにアドバイスします。</span><span class="sxs-lookup"><span data-stu-id="c1c66-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="c1c66-111">クライアント アプリケーションは [、IMAPIForm::D oVerb](imapiform-doverb.md) メソッドを呼び出して、開いている動詞を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c1c66-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c1c66-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1c66-112">See also</span></span>



[<span data-ttu-id="c1c66-113">フォーム サーバーの操作</span><span class="sxs-lookup"><span data-stu-id="c1c66-113">Form Server Interactions</span></span>](form-server-interactions.md)

