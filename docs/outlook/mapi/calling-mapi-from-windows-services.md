---
title: Windows サービスからの MAPI の呼び出し
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
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="6358e-103">Windows サービスからの MAPI の呼び出し</span><span class="sxs-lookup"><span data-stu-id="6358e-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="6358e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6358e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6358e-105">mapi 準拠のサービスプロバイダーで動作するように Windows サービスとして記述されている mapi クライアントアプリケーションを有効にするために、mapi にはいくつかの制限と要件があります。</span><span class="sxs-lookup"><span data-stu-id="6358e-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="6358e-106">MAPI クライアントには、次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="6358e-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="6358e-107">ユーザーインターフェイスを許可することはできません。</span><span class="sxs-lookup"><span data-stu-id="6358e-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="6358e-108">メッセージは密結合されたメッセージストアとトランスポートプロバイダーを使用してのみ送信できます。</span><span class="sxs-lookup"><span data-stu-id="6358e-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="6358e-109">また、MAPI クライアントは、Microsoft Exchange Server または別のサーバーベースのトランスポートプロバイダーのみを使用して、メッセージの送受信を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6358e-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="6358e-110">クライアントアプリケーションと MAPI スプーラーとの間の id とセキュリティの問題のため、サービスではほとんどのトランスポートプロバイダーがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6358e-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="6358e-111">Windows サービスとして実装されているかどうかにかかわらず、すべての mapi クライアントアプリケーションは、 [MAPIInitialize](mapiinitialize.md)関数を呼び出して mapi ライブラリを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6358e-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="6358e-112">[oleinitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)関数の呼び出しは、OLE ライブラリを使用するためにも必要です。</span><span class="sxs-lookup"><span data-stu-id="6358e-112">A call to the [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="6358e-113">[MAPIInitialize](mapiinitialize.md)と[oleinitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)の両方で、 [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx)関数を呼び出して、コンポーネントオブジェクトモデル (COM) ライブラリを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6358e-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="6358e-114">サービスであるクライアントは、 [MAPIInitialize](mapiinitialize.md)に渡される[MAPIINIT_0](mapiinit_0.md)構造の**ulflags**メンバーと、 [MAPILogonEx](mapilogonex.md)に渡される_ulflags_パラメーターに、特殊なフラグ MAPI_NT_SERVICE を設定する必要があります。MAPI に特別な実装を通知する関数。</span><span class="sxs-lookup"><span data-stu-id="6358e-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="6358e-115">Windows サービスとして記述され、mapi クライアントインターフェイスで記述された mapi クライアントには、追加の要件があります。</span><span class="sxs-lookup"><span data-stu-id="6358e-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="6358e-116">MAPI_NO_MAIL フラグは、 [MAPILogonEx](mapilogonex.md)への呼び出しで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6358e-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="6358e-117">他の種類のクライアントは、MAPI によって自動的に設定されるので、ログオンのフラグを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6358e-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="6358e-118">初期化スレッドでメッセージを処理するために、サービスとして実装されている MAPI クライアントは次のことを行います。</span><span class="sxs-lookup"><span data-stu-id="6358e-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="6358e-119">メインスレッドがブロックされたときに[MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6358e-119">Calls the [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="6358e-120">[GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx)、 [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)、および[DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx)の一連の Windows 関数を呼び出して、 [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx)が_nCount_パラメーターの値の合計を返す場合にメッセージを処理します。**WAIT_OBJECT_0**の値。これは、メッセージがキューにあることを示します。</span><span class="sxs-lookup"><span data-stu-id="6358e-120">Calls the [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6358e-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="6358e-121">See also</span></span>



[<span data-ttu-id="6358e-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="6358e-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="6358e-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="6358e-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="6358e-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="6358e-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="6358e-125">操作環境の問題</span><span class="sxs-lookup"><span data-stu-id="6358e-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

