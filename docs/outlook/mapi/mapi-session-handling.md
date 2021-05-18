---
title: MAPI �Z�b�V�����̏���
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422062"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="9348b-103">MAPI �Z�b�V�����̏���</span><span class="sxs-lookup"><span data-stu-id="9348b-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="9348b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9348b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9348b-105">サービス プロバイダーおよび基になるメッセージング システムと通信する前に、セッションを確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9348b-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="9348b-106">MAPI セッションは、クライアントから他の MAPI コンポーネントへのリンクです。</span><span class="sxs-lookup"><span data-stu-id="9348b-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="9348b-107">セッションを正常に開始した結果、MAPI は **、IMAPISession** インターフェイスを実装するオブジェクトであるセッション オブジェクトへのポインターをクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="9348b-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="9348b-108">詳細については [、「IMAPISession : IUnknown 」を参照してください](imapisessioniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="9348b-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="9348b-109">**IMAPISession** インターフェイスのメソッドを使用して、アドレス帳およびメッセージ ストア プロバイダーのオブジェクトにアクセスし、複数のテーブルにアクセスし、フォームを表示し、トランスポート プロバイダーのプロパティを設定し、プロファイルとメッセージ サービスの管理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="9348b-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="9348b-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="9348b-110">In this section</span></span>

[<span data-ttu-id="9348b-111">MAPI セッションの開始</span><span class="sxs-lookup"><span data-stu-id="9348b-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="9348b-112">MAPI セッションを開始する方法について説明し、詳細な情報を含むトピックへのリンクを含む。</span><span class="sxs-lookup"><span data-stu-id="9348b-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="9348b-113">MAPI セッションの終了</span><span class="sxs-lookup"><span data-stu-id="9348b-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="9348b-114">MAPI セッションを終了する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9348b-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="9348b-115">セッションを使用したオブジェクトへのアクセス</span><span class="sxs-lookup"><span data-stu-id="9348b-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="9348b-116">セッション ポインターを使用してセッション オブジェクトにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9348b-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="9348b-117">プライマリ ID とプロバイダー ID の取得</span><span class="sxs-lookup"><span data-stu-id="9348b-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="9348b-118">プライマリ ID とプロバイダー ID を取得するために使用されるプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9348b-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="9348b-119">Status Table オブジェクトと Status オブジェクト</span><span class="sxs-lookup"><span data-stu-id="9348b-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="9348b-120">状態テーブルから情報にアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9348b-120">Describes how to access information from the status table.</span></span>
    

