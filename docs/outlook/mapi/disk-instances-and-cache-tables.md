---
title: ディスクインスタンスとキャッシュテーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4f0b66476b1ab3d149b6f7e7b8171de7a509b597
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436756"
---
# <a name="disk-instances-and-cache-tables"></a><span data-ttu-id="5d6f5-103">ディスクインスタンスとキャッシュテーブル</span><span class="sxs-lookup"><span data-stu-id="5d6f5-103">Disk Instances and Cache Tables</span></span>

<span data-ttu-id="5d6f5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d6f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d6f5-105">フォームをアクティブにするには、その実行可能ファイルがユーザーのコンピューターで使用可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-105">To activate a form, its executable files must be available on the user's computer.</span></span> <span data-ttu-id="5d6f5-106">使用できない場合は、フォームライブラリからローカルディスクにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-106">If they are not available, they must be copied from the form library to the local disk.</span></span> <span data-ttu-id="5d6f5-107">これを行うために、既定のフォームマネージャーは、フォームの実行可能ファイルを格納するために、ユーザーの Windows ディレクトリにサブディレクトリを作成します (。exe、。HLPs)</span><span class="sxs-lookup"><span data-stu-id="5d6f5-107">To do this, the default form manager creates a subdirectory in the user's Windows directory to contain the form's executable files (.EXEs,.HLPs).</span></span> <span data-ttu-id="5d6f5-108">このディレクトリは、フォームのディスクインスタンスと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-108">This directory is referred to as the disk instance of the form.</span></span>
  
<span data-ttu-id="5d6f5-109">既定のフォームマネージャーは、すべてのディスクインスタンスのテーブルを保持するので、ディスクインスタンスが既に存在する場合は、フォームライブラリからユーザーのディスクにファイルをコピーしなくても使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-109">The default form manager maintains a table of all disk instances so that if a disk instance already exists it can be used without having to copy files from the form library to the user's disk.</span></span> <span data-ttu-id="5d6f5-110">ディスクインスタンスのテーブルは、使用頻度の低いキャッシュとして管理されます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-110">The table of disk instances is managed as a least-frequently-used cache.</span></span> <span data-ttu-id="5d6f5-111">新しいディスクインスタンスが必要な場合は、ユーザーのコンピューターにコピーされ、使用頻度の低いディスクインスタンスを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-111">If a new disk instance is needed, it is copied to the user's computer, replacing the least-frequently-used disk instance.</span></span> <span data-ttu-id="5d6f5-112">その後、ディスクインスタンスキャッシュテーブルが更新され、最新の構成が反映されます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-112">The disk instance cache table is then updated to reflect the latest configuration.</span></span> <span data-ttu-id="5d6f5-113">ディスクキャッシュのサイズはユーザーが構成可能なオプションであり、ユーザーは使用可能なディスク容量で速度のバランスを取ることができます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-113">The size of the disk cache is a user-configurable option, enabling users to balance speed with available disk capacity.</span></span>
  
<span data-ttu-id="5d6f5-114">ディスクインスタンスキャッシュに加えて、既定のフォームマネージャーは、ユーザーのコンピューター上で実行されているフォームサーバーのすべての実行中のインスタンスを一覧表示する、実行中のインスタンステーブルを保持します。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-114">In addition to the disk instance cache, the default form manager maintains a running instance table that lists all running instances of form servers on the user's computer.</span></span> <span data-ttu-id="5d6f5-115">これにより、MAPI の機能を使用して、そのフォームサーバーのメッセージクラスのフォームがアクティブ化されるまで、非表示の状態でアイドル形式のインスタンスを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-115">This uses MAPI's ability to keep idle form instances running in an invisible state until a form of that form server's message class is activated.</span></span> <span data-ttu-id="5d6f5-116">言い換えると、フォームの実行可能ファイルをフォームライブラリ内に配置して、ディスクから、またはネットワーク経由でメモリにロードする必要がある回数を最小限に抑えるために、フォームサーバーを RAM にキャッシュすることができます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-116">In other words, form servers can be cached in RAM to minimize the number of times a form's executable must be located within a form library and loaded into memory from disk or over the network.</span></span> <span data-ttu-id="5d6f5-117">ディスクインスタンスキャッシュと同様に、実行中のインスタンスキャッシュは、使用頻度の低い方法で動作します。これにより、実行中のフォームインスタンスをキャッシュから削除して、別のフォームインスタンスにスペースを空けることができます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-117">Like the disk instance cache, the running instance cache behaves in a least-frequently-used fashion so that a running form instance can be purged from the cache to make room for another form instance.</span></span> <span data-ttu-id="5d6f5-118">フォームサーバーのフォームライブラリが検索される前に、フォームサーバーの実行中のインスタンスがこのキャッシュで検索されます。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-118">This cache is searched for a running instance of a form server before the form libraries are searched for the form server.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5d6f5-119">ユーザーのワークステーションにフォームをインストールすると、既定のフォームマネージャーには進行状況インジケーターが表示されます。これにより、ユーザーは操作を取り消すことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-119">The default form manager displays a progress indicator when installing a form on a user's workstation, enabling the user to cancel the operation.</span></span> <span data-ttu-id="5d6f5-120">これは、フォームサーバーの実行可能ファイルに対するユーザーの接続が低帯域幅のネットワーク上にある場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="5d6f5-120">This is especially useful if the user's connection to the form server's executable file is over a low bandwidth network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d6f5-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d6f5-121">See also</span></span>

- [<span data-ttu-id="5d6f5-122">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="5d6f5-122">MAPI Forms</span></span>](mapi-forms.md)

