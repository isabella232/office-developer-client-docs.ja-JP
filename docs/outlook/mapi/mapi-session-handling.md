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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328225"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="f557c-103">MAPI �Z�b�V�����̏���</span><span class="sxs-lookup"><span data-stu-id="f557c-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="f557c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f557c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f557c-105">サービスプロバイダおよび基盤となるメッセージングシステムと通信するには、事前にセッションを確立しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="f557c-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="f557c-106">mapi セッションは、クライアントから他の mapi コンポーネントへのリンクです。</span><span class="sxs-lookup"><span data-stu-id="f557c-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="f557c-107">セッションが正常に開始された結果、MAPI はクライアントに session オブジェクトへのポインターを返します。これは、 **imapisession**インターフェイスを実装するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="f557c-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="f557c-108">詳細については、「 [imapisession: IUnknown](imapisessioniunknown.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f557c-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="f557c-109">**imapisession**インターフェイスのメソッドを使用すると、アドレス帳およびメッセージストアプロバイダーのオブジェクトにアクセスし、複数のテーブルにアクセスしたり、フォームを表示したり、トランスポートプロバイダーのプロパティを設定したり、プロファイルとメッセージサービスの管理を実行したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="f557c-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="f557c-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="f557c-110">In this section</span></span>

[<span data-ttu-id="f557c-111">MAPI セッションの開始</span><span class="sxs-lookup"><span data-stu-id="f557c-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="f557c-112">MAPI セッションを開始する方法について説明し、詳細情報を含むトピックへのリンクを示します。</span><span class="sxs-lookup"><span data-stu-id="f557c-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="f557c-113">MAPI セッションの終了</span><span class="sxs-lookup"><span data-stu-id="f557c-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="f557c-114">MAPI セッションを終了する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f557c-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="f557c-115">セッションを使用してオブジェクトにアクセスする</span><span class="sxs-lookup"><span data-stu-id="f557c-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="f557c-116">セッションポインターを使用して session オブジェクトにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f557c-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="f557c-117">プライマリとプロバイダー id の取得</span><span class="sxs-lookup"><span data-stu-id="f557c-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="f557c-118">プライマリとプロバイダーの id を取得するために使用されるプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f557c-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="f557c-119">状態テーブルと状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f557c-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="f557c-120">状態テーブルから情報にアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f557c-120">Describes how to access information from the status table.</span></span>
    

