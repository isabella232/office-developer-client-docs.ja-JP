---
title: メッセージサービスインストールのサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350632"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="7a704-103">メッセージサービスインストールのサポート</span><span class="sxs-lookup"><span data-stu-id="7a704-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="7a704-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a704-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a704-105">message service をインストールするためのセットアッププログラムでは、次の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a704-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="7a704-106">メッセージサービスファイル (メッセージサービス、サービスプロバイダ dll など) を、CD またはディスクからワークステーションのローカルドライブにコピーします。</span><span class="sxs-lookup"><span data-stu-id="7a704-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="7a704-107">コピーする必要があるファイルは、メッセージサービスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="7a704-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="7a704-108">通常は、少なくとも1つの DLL をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7a704-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="7a704-109">mapisvc.inf 構成ファイルにエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="7a704-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="7a704-110">このファイルを、メッセージサービスのサービスプロバイダーをサポートするように変更する方法の詳細については、「[ファイル形式の mapisvc.inf](file-format-of-mapisvc-inf.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a704-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="7a704-111">必要に応じて、メッセージサービスのシステムレジストリにエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="7a704-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="7a704-112">エントリがシステムレジストリにどのように表示されるかの詳細については、「 [MAPI サブシステムのインストール](installing-the-mapi-subsystem.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a704-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="7a704-113">次のいずれかの項目を使用して、まだ存在しない場合は、既定のプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7a704-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="7a704-114">プロファイルウィザードは、一連のダイアログボックスを使用してユーザーの操作を使用してプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7a704-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="7a704-115">プロファイルウィザードの使用方法の詳細については、「プロファイル[ウィザードを使用してプロファイルを作成](creating-a-profile-by-using-the-profile-wizard.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a704-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="7a704-116">ユーザーの操作を使用してプロファイルを作成するコントロールパネル。</span><span class="sxs-lookup"><span data-stu-id="7a704-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="7a704-117">コントロールパネルを使用すると、ユーザーは、メッセージサービスを構成したりプロファイルプロパティを設定したりするためのプロファイルウィザードよりも柔軟に作業を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7a704-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="7a704-118">セットアッププログラムは、指定されたパブリックディレクトリに配置します。</span><span class="sxs-lookup"><span data-stu-id="7a704-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="7a704-119">多くの構成クライアント (コントロールパネルなど) では、ユーザーがディレクトリの名前を入力する必要があるため、これは重要です。</span><span class="sxs-lookup"><span data-stu-id="7a704-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="7a704-120">ユーザーが [**追加**] ボタンをクリックして [**ディスク**を開く] ダイアログボックスを起動し、プログラムへのパスを指定すると、コントロールパネルはセットアッププログラムを起動します。</span><span class="sxs-lookup"><span data-stu-id="7a704-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="7a704-121">コントロールパネルはプログラムを実行し、 _ulcontext_パラメーターを MSG_SERVICE_INSTALL に設定して、メッセージサービスのエントリポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7a704-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="7a704-122">プロファイルは MAPI アーキテクチャの一部に含まれないため、再作成するのが困難な既定のプロファイルにインストールプログラムが保存されていないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7a704-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="7a704-123">プロファイルの復元用のユーティリティはありません。プロファイルをあるコンピューターから別のコンピューターに移動したり、オフラインバックアップを行ったり、バックアップコピーから個別またはグローバルに復元したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="7a704-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a704-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a704-124">See also</span></span>



[<span data-ttu-id="7a704-125">メッセージサービスの実装</span><span class="sxs-lookup"><span data-stu-id="7a704-125">Message Service Implementation</span></span>](message-service-implementation.md)

