---
title: MAPI セッションの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801456"
---
# <a name="mapi-session-handling"></a><span data-ttu-id="2d52a-103">MAPI セッションの処理</span><span class="sxs-lookup"><span data-stu-id="2d52a-103">MAPI Session Handling</span></span>

  
  
<span data-ttu-id="2d52a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d52a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d52a-105">サービス プロバイダーと、基になるメッセージング システムと通信するには、セッションを確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d52a-105">Before you can communicate with service providers and an underlying messaging system, you must establish a session.</span></span> <span data-ttu-id="2d52a-106">MAPI セッションは、クライアントからその他の MAPI コンポーネントへのリンクです。</span><span class="sxs-lookup"><span data-stu-id="2d52a-106">A MAPI session is a link from a client to other MAPI components.</span></span> <span data-ttu-id="2d52a-107">結果として正常にセッションを開始、MAPI クライアントに返しますセッション オブジェクトへのポインター、 **IMAPISession**インターフェイスを実装するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="2d52a-107">As the result of successfully starting a session, MAPI returns to clients a pointer to a session object — an object that implements the **IMAPISession** interface.</span></span> <span data-ttu-id="2d52a-108">詳細についてを参照してください[IMAPISession: IUnknown](imapisessioniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="2d52a-108">For more information, see [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span> <span data-ttu-id="2d52a-109">アドレス帳、メッセージ ストア プロバイダーのオブジェクトにアクセスする、いくつかのテーブルにアクセス、フォームを表示する、トランスポート プロバイダーのプロパティを設定およびプロファイルおよびメッセージ サービス管理を実行するのには、 **IMAPISession**インターフェイスのメソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2d52a-109">You can use the methods of the **IMAPISession** interface to access the objects of address book and message store providers, access several tables, display forms, set transport provider properties, and perform profile and message service administration.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="2d52a-110">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="2d52a-110">In this section</span></span>

[<span data-ttu-id="2d52a-111">MAPI セッションを開始</span><span class="sxs-lookup"><span data-stu-id="2d52a-111">Starting a MAPI Session</span></span>](starting-a-mapi-session.md)
  
> <span data-ttu-id="2d52a-112">MAPI セッションを開始する方法について説明しより詳細な情報を含むトピックへのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2d52a-112">Describes how to start a MAPI session and includes links to topics with more detailed information.</span></span>
    
[<span data-ttu-id="2d52a-113">MAPI セッションを終了</span><span class="sxs-lookup"><span data-stu-id="2d52a-113">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)
  
> <span data-ttu-id="2d52a-114">MAPI セッションを終了する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2d52a-114">Describes how to end a MAPI session.</span></span>
    
[<span data-ttu-id="2d52a-115">セッションを使用してオブジェクトへのアクセス</span><span class="sxs-lookup"><span data-stu-id="2d52a-115">Accessing Objects by Using the Session</span></span>](accessing-objects-by-using-the-session.md)
  
> <span data-ttu-id="2d52a-116">セッション オブジェクトにアクセスするセッションのポインターを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2d52a-116">Describes how to use a session pointer to access session objects.</span></span>
    
[<span data-ttu-id="2d52a-117">プライマリ デバイスとプロバイダーの Id を取得しています。</span><span class="sxs-lookup"><span data-stu-id="2d52a-117">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
> <span data-ttu-id="2d52a-118">プロバイダーの id、プライマリを取得するためのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2d52a-118">Describes the properties used to retrieve primary and provider identity.</span></span>
    
[<span data-ttu-id="2d52a-119">状態テーブルとオブジェクトの状態</span><span class="sxs-lookup"><span data-stu-id="2d52a-119">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)
  
> <span data-ttu-id="2d52a-120">状態テーブルから情報にアクセスする方法をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2d52a-120">Describes how to access information from the status table.</span></span>
    

