---
title: MAPI を Windows サービスから呼び出す
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318107"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="24056-103">MAPI を Windows サービスから呼び出す</span><span class="sxs-lookup"><span data-stu-id="24056-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="24056-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24056-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24056-105">MAPI 準拠のサービス プロバイダーとWindows MAPI クライアント アプリケーションを有効にするには、MAPI にはいくつかの制限と要件が適用されます。</span><span class="sxs-lookup"><span data-stu-id="24056-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="24056-106">MAPI クライアントには、次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="24056-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="24056-107">ユーザー インターフェイスを許可することはできません。</span><span class="sxs-lookup"><span data-stu-id="24056-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="24056-108">メッセージは、緊密に結合されたメッセージ ストアとトランスポート プロバイダーを介してのみ送信できます。</span><span class="sxs-lookup"><span data-stu-id="24056-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="24056-109">さらに、MAPI クライアントは、サーバーまたは別のサーバー ベースのトランスポート プロバイダー Microsoft Exchange Serverを使用してメッセージを送受信できます。</span><span class="sxs-lookup"><span data-stu-id="24056-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="24056-110">クライアント アプリケーションと MAPI スプーラー間の ID とセキュリティの問題のため、ほとんどのトランスポート プロバイダーはサービスではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="24056-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="24056-111">MAPI クライアント アプリケーションは、すべての MAPI クライアント アプリケーションWindows、MAPI ライブラリを初期化するために[MAPIInitialize](mapiinitialize.md)関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="24056-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="24056-112">OLE ライブラリを [使用するには、OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) 関数の呼び出しも必要です。</span><span class="sxs-lookup"><span data-stu-id="24056-112">A call to the [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="24056-113">[MAPIInitialize と](mapiinitialize.md) [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)の両方が[CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx)関数を呼び出して、コンポーネント オブジェクト モデル (COM) ライブラリを初期化します。</span><span class="sxs-lookup"><span data-stu-id="24056-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="24056-114">サービスであるクライアントは [、MAPIInitialize](mapiinitialize.md)に渡される [MAPIINIT_0](mapiinit_0.md)構造体の **ulFlags** メンバーと [、MAPILogonEx](mapilogonex.md)関数に渡される _ulFlags_ パラメーターに特別なフラグ MAPI_NT_SERVICE を設定して、MAPI に特別な実装を通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24056-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="24056-115">MAPI クライアント は、サービスWindows、MAPI クライアント インターフェイスで書き込まれる場合は、追加の要件を満たします。</span><span class="sxs-lookup"><span data-stu-id="24056-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="24056-116">MAPILogonEx の呼び出MAPI_NO_MAILフラグを設定 [する必要があります](mapilogonex.md)。</span><span class="sxs-lookup"><span data-stu-id="24056-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="24056-117">他の種類のクライアントは、MAPI によって自動的に設定されますので、ログオン用のフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24056-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="24056-118">初期化スレッド内のメッセージを処理するために、サービスとして実装される MAPI クライアントは次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="24056-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="24056-119">メイン スレッド [がブロックされている場合は、MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="24056-119">Calls the [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="24056-120">[MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx)が nCount パラメーターの値と WAIT_OBJECT_0 の値の合計を返す場合に、メッセージを処理するために、Windows 関数の[GetMessage、TranslateMessage、](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx)および[DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx)シーケンスを呼び出します。これは、メッセージがキュー内にあるかどうかを示します。 [](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx) </span><span class="sxs-lookup"><span data-stu-id="24056-120">Calls the [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24056-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="24056-121">See also</span></span>



[<span data-ttu-id="24056-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="24056-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="24056-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="24056-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="24056-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="24056-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="24056-125">オペレーティング環境の問題</span><span class="sxs-lookup"><span data-stu-id="24056-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

