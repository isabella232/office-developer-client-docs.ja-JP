---
title: Windows サービスからの MAPI 呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f77b3dd9ca8c977574aab337b0df572404061b4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565866"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="c01cc-103">Windows サービスからの MAPI 呼び出し</span><span class="sxs-lookup"><span data-stu-id="c01cc-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="c01cc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c01cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c01cc-105">MAPI に準拠したサービス ・ プロバイダーで動作する Windows サービスとして記述されている MAPI クライアント アプリケーションを有効にするには、MAPI には、いくつかの制限事項と要件が課されます。</span><span class="sxs-lookup"><span data-stu-id="c01cc-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="c01cc-106">MAPI クライアントでは、次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="c01cc-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="c01cc-107">ユーザー インターフェイスすることができません。</span><span class="sxs-lookup"><span data-stu-id="c01cc-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="c01cc-108">密結合のメッセージ ・ ストアおよびトランスポート経由でのみメッセージを送信するプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="c01cc-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="c01cc-109">さらに、MAPI クライアントは送信し、Microsoft Exchange Server ではのみ、または別のサーバ ・ ベースのトランスポート プロバイダーを使用してメッセージを受信できます。</span><span class="sxs-lookup"><span data-stu-id="c01cc-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="c01cc-110">ほとんどのトランスポート プロバイダーは、クライアント アプリケーションと MAPI スプーラーとの間の id およびセキュリティの問題のため、サービスでサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c01cc-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="c01cc-111">すべての MAPI クライアント アプリケーション、Windows サービスとして実装されるかどうかが MAPI ライブラリを初期化するために[生じます](mapiinitialize.md)関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c01cc-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="c01cc-112">[OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx)関数の呼び出しは、OLE ライブラリを使用する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="c01cc-112">A call to the [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="c01cc-113">[生じます](mapiinitialize.md)、 [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx)の両方は、コンポーネント オブジェクト モデル (COM) ライブラリを初期化するために、 [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx)関数への呼び出しを確認します。</span><span class="sxs-lookup"><span data-stu-id="c01cc-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="c01cc-114">サービスのクライアント、MAPI_NT_SERVICE、特別なフラグ、 **ulFlags** 、 [MAPIINIT_0](mapiinit_0.md)構造体のメンバー[生じます](mapiinitialize.md)に渡されるのと設定[MAPILogonEx](mapilogonex.md)に渡される_ulFlags_パラメーターでMAPI の特殊な実装に通知する関数です。</span><span class="sxs-lookup"><span data-stu-id="c01cc-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="c01cc-115">Windows サービスとして作成され、MAPI クライアント ・ インタ フェースを記述する MAPI クライアントでは、追加の要件があります。</span><span class="sxs-lookup"><span data-stu-id="c01cc-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="c01cc-116">[MAPILogonEx](mapilogonex.md)の呼び出しでは、MAPI_NO_MAIL フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c01cc-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="c01cc-117">その他の種類のクライアントは、MAPI によって自動的に設定されているために、ログオンにフラグを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c01cc-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="c01cc-118">初期化スレッドでメッセージを処理するためにサービスとして実装されている MAPI クライアントは、次の。</span><span class="sxs-lookup"><span data-stu-id="c01cc-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="c01cc-119">[MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx)関数を呼び出すときに、メイン スレッドはブロックします。</span><span class="sxs-lookup"><span data-stu-id="c01cc-119">Calls the [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="c01cc-120">_NCount_パラメーターの値の合計が[MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx)に返されるときにメッセージを処理するために Windows の機能の[自動インクリメント](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx)を[獲得](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx)で[もないとき](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx)のシーケンスを呼び出すと、**WAIT_OBJECT_0**メッセージがキュー内であることを示す値です。</span><span class="sxs-lookup"><span data-stu-id="c01cc-120">Calls the [GetMessage](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx), [TranslateMessage](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c01cc-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="c01cc-121">See also</span></span>



[<span data-ttu-id="c01cc-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="c01cc-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="c01cc-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="c01cc-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="c01cc-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="c01cc-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="c01cc-125">操作環境の問題</span><span class="sxs-lookup"><span data-stu-id="c01cc-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

