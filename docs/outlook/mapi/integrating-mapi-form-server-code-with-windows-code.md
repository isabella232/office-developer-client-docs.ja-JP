---
title: MAPI フォームのサーバー コードを Windows のコードと統合します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 31f09b1c2f7b23d63e17f59c28b7bcf377b769d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801068"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="caaeb-103">MAPI フォームのサーバー コードを Windows のコードと統合します。</span><span class="sxs-lookup"><span data-stu-id="caaeb-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="caaeb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="caaeb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="caaeb-105">フォーム サーバーが Win32 アプリケーションであることに注意します。</span><span class="sxs-lookup"><span data-stu-id="caaeb-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="caaeb-106">などは、フォームのサーバーをメモリに読み込むと、正常に終了に関連するいくつかのタスクがあります。</span><span class="sxs-lookup"><span data-stu-id="caaeb-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="caaeb-107">すべての Windows アプリケーションと同様に、フォームのサーバーのエントリ ポイントが**WinMain**関数です。</span><span class="sxs-lookup"><span data-stu-id="caaeb-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="caaeb-108">この関数は、次のタスクを実行する適切な場所です。</span><span class="sxs-lookup"><span data-stu-id="caaeb-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="caaeb-109">作成して、フォームのサーバーがほかの OLE コンポーネントを使用して対話できるように、ウィンドウ クラスを登録します。</span><span class="sxs-lookup"><span data-stu-id="caaeb-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="caaeb-110">作成して、ウィンドウ クラスまたはフォームのオブジェクトのユーザー インターフェイスのクラスを登録します。</span><span class="sxs-lookup"><span data-stu-id="caaeb-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="caaeb-111">[生じます](mapiinitialize.md)関数を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="caaeb-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="caaeb-112">**生じます**が、必要な OLE の初期化には、同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="caaeb-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="caaeb-113">これは、フォーム サーバーのインスタンスごと 1 回だけ実行してください。</span><span class="sxs-lookup"><span data-stu-id="caaeb-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="caaeb-114">フォーム サーバーのクラス識別子 (CLSID) の文字列表現でグローバル アトムを登録しています。</span><span class="sxs-lookup"><span data-stu-id="caaeb-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="caaeb-115">フォーム サーバーの有効期間のこのアトムが存在します。</span><span class="sxs-lookup"><span data-stu-id="caaeb-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="caaeb-116">フォーム サーバーのクラス ファクトリを OLE に登録して[います](http://msdn.microsoft.com/en-us/library/ms693407.aspx)OLE 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="caaeb-116">Calling the OLE function [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="caaeb-117">メッセージを受信するのにはメイン ウィンドウを作成しています。</span><span class="sxs-lookup"><span data-stu-id="caaeb-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="caaeb-118">このウィンドウはおそらく、ユーザーが個々 のフォーム オブジェクトに関連付けられている特定の windows と対話するために、表示する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="caaeb-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="caaeb-119">ただし、開発時にメイン ・ ウィンドウは、出力またはフォーム サーバーのコントロールをデバッグするための便利な場所。</span><span class="sxs-lookup"><span data-stu-id="caaeb-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="caaeb-120">フォーム サーバーの有効期間を実行するためのメッセージ ループを作成して、翻訳作業中のフォーム オブジェクトへの windows メッセージのディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="caaeb-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="caaeb-121">フォーム サーバーが終了するは、次のタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="caaeb-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="caaeb-122">OLE 関数、メッセージ クラスの OLE の登録を取り消すには[CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="caaeb-122">Call the OLE function [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="caaeb-123">Mapi フォーム サーバーの接続を正しく閉じるには、 **MAPIUninitialize**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="caaeb-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="caaeb-124">クラス識別子の文字列表現が含まれているグローバル アトムを削除します。</span><span class="sxs-lookup"><span data-stu-id="caaeb-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="caaeb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="caaeb-125">See also</span></span>



[<span data-ttu-id="caaeb-126">フォーム サーバー コードの記述</span><span class="sxs-lookup"><span data-stu-id="caaeb-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

