---
title: メッセージ サービスのインストールのサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404702"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="089ae-103">メッセージ サービスのインストールのサポート</span><span class="sxs-lookup"><span data-stu-id="089ae-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="089ae-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="089ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="089ae-105">メッセージ サービスをインストールするセットアップ プログラムは、次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="089ae-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="089ae-106">メッセージ サービスやサービス プロバイダー DLL などのメッセージ サービス ファイルを CD またはディスクからワークステーションのローカル ドライブにコピーします。</span><span class="sxs-lookup"><span data-stu-id="089ae-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="089ae-107">コピーする必要があるファイルは、メッセージ サービスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="089ae-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="089ae-108">通常、少なくとも 1 つの DLL をコピーします。</span><span class="sxs-lookup"><span data-stu-id="089ae-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="089ae-109">Mapisvc.inf 構成ファイルにエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="089ae-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="089ae-110">メッセージ サービスでサービス プロバイダーをサポートするようにこのファイルを変更する方法の詳細については [、「MapiSvc.inf のファイル形式」を参照してください](file-format-of-mapisvc-inf.md)。</span><span class="sxs-lookup"><span data-stu-id="089ae-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="089ae-111">必要に応じて、メッセージ サービスのシステム レジストリにエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="089ae-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="089ae-112">エントリをシステム レジストリに表示する方法の詳細については、「MAPI サブシステムのインストール [」を参照してください](installing-the-mapi-subsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="089ae-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="089ae-113">次のいずれかの項目を使用して、既定のプロファイルがまだ存在しない場合は、既定のプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="089ae-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="089ae-114">一連のダイアログ ボックスによるユーザー操作を使用してプロファイルを作成するプロファイル ウィザード。</span><span class="sxs-lookup"><span data-stu-id="089ae-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="089ae-115">プロファイル ウィザードの使用の詳細については、「プロファイル ウィザードを使用 [してプロファイルを作成する」を参照してください](creating-a-profile-by-using-the-profile-wizard.md)。</span><span class="sxs-lookup"><span data-stu-id="089ae-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="089ae-116">ユーザー操作を使用してプロファイルを作成するコントロール パネル。</span><span class="sxs-lookup"><span data-stu-id="089ae-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="089ae-117">コントロール パネルは、メッセージ サービスを構成し、プロファイル プロパティを設定するためのプロファイル ウィザードよりも柔軟性が高いユーザーを提供します。</span><span class="sxs-lookup"><span data-stu-id="089ae-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="089ae-118">セットアップ プログラムを指定されたパブリック ディレクトリに配置します。</span><span class="sxs-lookup"><span data-stu-id="089ae-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="089ae-119">これは重要です。コントロール パネルなどのほとんどの構成クライアントでは、ユーザーがディレクトリの名前を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="089ae-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="089ae-120">コントロール パネルは、ユーザーが [追加] ボタンをクリックし、[ディスクを持つ] ダイアログ ボックスを呼び出し、プログラムへのパスを指定すると、セットアップ プログラムを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="089ae-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="089ae-121">コントロール パネルは、プログラムを実行し、メッセージ サービスのエントリ ポイント関数を呼び出し  _、ulContext_ パラメーターを指定MSG_SERVICE_INSTALL。</span><span class="sxs-lookup"><span data-stu-id="089ae-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="089ae-122">プロファイルは MAPI アーキテクチャの消耗品なので、再作成が困難な既定のプロファイルにインストール プログラムが格納されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="089ae-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="089ae-123">プロファイルの回復、あるコンピューターから別のコンピューターへのプロファイルの移動、オフライン バックアップ、またはバックアップ コピーからの個別またはグローバルな復元のためのユーティリティはありません。</span><span class="sxs-lookup"><span data-stu-id="089ae-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="089ae-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="089ae-124">See also</span></span>



[<span data-ttu-id="089ae-125">Message Service の実装</span><span class="sxs-lookup"><span data-stu-id="089ae-125">Message Service Implementation</span></span>](message-service-implementation.md)

