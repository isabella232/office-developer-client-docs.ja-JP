---
title: メッセージ サービス インストールのサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1f82741e3c44c589a18a1428fd68cebe6a501d5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581994"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="c438e-103">メッセージ サービス インストールのサポート</span><span class="sxs-lookup"><span data-stu-id="c438e-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="c438e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c438e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c438e-105">メッセージ サービスをインストールするためのセットアップ プログラムは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c438e-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="c438e-106">ワークステーション上のローカル ドライブに CD またはディスクからのメッセージ サービスとサービス ・ プロバイダー Dll など、メッセージ サービスのファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="c438e-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="c438e-107">コピーする必要のあるファイルは、メッセージ サービスに依存します。</span><span class="sxs-lookup"><span data-stu-id="c438e-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="c438e-108">通常、少なくとも 1 つの DLL をコピーします。</span><span class="sxs-lookup"><span data-stu-id="c438e-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="c438e-109">Mapisvc.inf の構成ファイルにエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="c438e-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="c438e-110">メッセージ サービスのサービス プロバイダーをサポートするためにこのファイルを変更する方法の詳細については、 [MapiSvc.inf のファイル形式](file-format-of-mapisvc-inf.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c438e-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="c438e-111">必要に応じて、メッセージ サービスのレジストリにエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="c438e-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="c438e-112">システム レジストリのエントリの表示方法の詳細については、 [MAPI サブシステムのインストール](installing-the-mapi-subsystem.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c438e-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="c438e-113">次の項目のいずれかを使用していずれかのまだ存在しない場合は、既定のプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="c438e-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="c438e-114">プロファイル ウィザードは一連のダイアログ ボックスを通じてユーザーとの対話を使用してプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="c438e-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="c438e-115">プロファイル ウィザードの使用方法の詳細については、[プロファイル ウィザードを使用してプロファイルを作成する](creating-a-profile-by-using-the-profile-wizard.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c438e-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="c438e-116">ユーザーとの対話を使用してプロファイルを作成するコントロール パネルです。</span><span class="sxs-lookup"><span data-stu-id="c438e-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="c438e-117">コントロール パネルは、ユーザー プロファイル ウィザードのメッセージ サービスを構成して、プロファイル プロパティの設定よりも高い柔軟性を提供します。</span><span class="sxs-lookup"><span data-stu-id="c438e-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="c438e-118">指定されたパブリック ディレクトリでセットアップ プログラムを配置します。</span><span class="sxs-lookup"><span data-stu-id="c438e-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="c438e-119">これは、オプションは、[コントロール パネル] など、構成のほとんどのクライアントは、ユーザーがディレクトリの名前を入力する必要があるため重要です。</span><span class="sxs-lookup"><span data-stu-id="c438e-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="c438e-120">コントロール パネルは、ユーザーは、 **[追加**] ボタンをクリックすると、 **[ディスク**] ダイアログ ボックスで、起動し、プログラムへのパスを指定すると、セットアップ プログラムを起動します。</span><span class="sxs-lookup"><span data-stu-id="c438e-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="c438e-121">コントロール パネルでは、プログラムを実行し、 _ulContext_パラメーターを MSG_SERVICE_INSTALL に設定して、メッセージ サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c438e-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="c438e-122">プロファイルは MAPI アーキテクチャの消耗ユニットの一部であるため、そのインストール プログラムには格納されません何も既定のプロファイルを再作成することが困難になることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c438e-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="c438e-123">プロファイル ・ リカバリのプロファイルを 1 つのコンピューター間で移動する、オフライン バックアップの場合、またはバックアップ コピーから復元を個別またはグローバルのユーティリティはありません。</span><span class="sxs-lookup"><span data-stu-id="c438e-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c438e-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="c438e-124">See also</span></span>



[<span data-ttu-id="c438e-125">メッセージ サービスの実装</span><span class="sxs-lookup"><span data-stu-id="c438e-125">Message Service Implementation</span></span>](message-service-implementation.md)

