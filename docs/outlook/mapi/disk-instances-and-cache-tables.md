---
title: ディスク インスタンスとキャッシュ テーブル
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
# <a name="disk-instances-and-cache-tables"></a><span data-ttu-id="6c867-103">ディスク インスタンスとキャッシュ テーブル</span><span class="sxs-lookup"><span data-stu-id="6c867-103">Disk Instances and Cache Tables</span></span>

<span data-ttu-id="6c867-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c867-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c867-105">フォームをアクティブ化するには、その実行可能ファイルをユーザーのコンピューターで使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c867-105">To activate a form, its executable files must be available on the user's computer.</span></span> <span data-ttu-id="6c867-106">使用できない場合は、フォーム ライブラリからローカル ディスクにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c867-106">If they are not available, they must be copied from the form library to the local disk.</span></span> <span data-ttu-id="6c867-107">これを行うには、既定のフォーム マネージャーは、ユーザーの Windows ディレクトリにサブディレクトリを作成して、フォームの実行可能ファイル (.EXEs,.HLP)。</span><span class="sxs-lookup"><span data-stu-id="6c867-107">To do this, the default form manager creates a subdirectory in the user's Windows directory to contain the form's executable files (.EXEs,.HLPs).</span></span> <span data-ttu-id="6c867-108">このディレクトリは、フォームのディスク インスタンスと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6c867-108">This directory is referred to as the disk instance of the form.</span></span>
  
<span data-ttu-id="6c867-109">既定のフォーム マネージャーは、すべてのディスク インスタンスのテーブルを保持し、ディスク インスタンスが既に存在する場合は、フォーム ライブラリからユーザーのディスクにファイルをコピーせずに使用できます。</span><span class="sxs-lookup"><span data-stu-id="6c867-109">The default form manager maintains a table of all disk instances so that if a disk instance already exists it can be used without having to copy files from the form library to the user's disk.</span></span> <span data-ttu-id="6c867-110">ディスク インスタンスのテーブルは、最も頻繁に使用されるキャッシュとして管理されます。</span><span class="sxs-lookup"><span data-stu-id="6c867-110">The table of disk instances is managed as a least-frequently-used cache.</span></span> <span data-ttu-id="6c867-111">新しいディスク インスタンスが必要な場合は、最も頻繁に使用されるディスク インスタンスを置き換え、ユーザーのコンピューターにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6c867-111">If a new disk instance is needed, it is copied to the user's computer, replacing the least-frequently-used disk instance.</span></span> <span data-ttu-id="6c867-112">その後、ディスク インスタンス キャッシュ テーブルが更新され、最新の構成が反映されます。</span><span class="sxs-lookup"><span data-stu-id="6c867-112">The disk instance cache table is then updated to reflect the latest configuration.</span></span> <span data-ttu-id="6c867-113">ディスク キャッシュのサイズは、ユーザーが構成できるオプションであり、ユーザーは速度と使用可能なディスク容量のバランスを取る機能です。</span><span class="sxs-lookup"><span data-stu-id="6c867-113">The size of the disk cache is a user-configurable option, enabling users to balance speed with available disk capacity.</span></span>
  
<span data-ttu-id="6c867-114">既定のフォーム マネージャーは、ディスク インスタンス キャッシュに加えて、ユーザーのコンピューター上のフォーム サーバーのすべての実行中のインスタンスを一覧表示する実行中のインスタンス テーブルを保持します。</span><span class="sxs-lookup"><span data-stu-id="6c867-114">In addition to the disk instance cache, the default form manager maintains a running instance table that lists all running instances of form servers on the user's computer.</span></span> <span data-ttu-id="6c867-115">これにより、MAPI の機能を使用して、そのフォーム サーバーのメッセージ クラスのフォームがアクティブ化されるまで、アイドル状態のフォーム インスタンスを非表示の状態で実行し続けることができます。</span><span class="sxs-lookup"><span data-stu-id="6c867-115">This uses MAPI's ability to keep idle form instances running in an invisible state until a form of that form server's message class is activated.</span></span> <span data-ttu-id="6c867-116">つまり、フォーム サーバーを RAM にキャッシュして、フォームの実行可能ファイルをフォーム ライブラリ内に格納し、ディスクまたはネットワーク上のメモリに読み込む必要がある回数を最小限に抑える必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c867-116">In other words, form servers can be cached in RAM to minimize the number of times a form's executable must be located within a form library and loaded into memory from disk or over the network.</span></span> <span data-ttu-id="6c867-117">ディスク インスタンス キャッシュと同様に、実行中のインスタンス キャッシュは最も頻繁に使用される方法で動作し、実行中のフォーム インスタンスをキャッシュから削除して別のフォーム インスタンスを空き領域にできます。</span><span class="sxs-lookup"><span data-stu-id="6c867-117">Like the disk instance cache, the running instance cache behaves in a least-frequently-used fashion so that a running form instance can be purged from the cache to make room for another form instance.</span></span> <span data-ttu-id="6c867-118">このキャッシュは、フォーム ライブラリがフォーム サーバーを検索する前に、フォーム サーバーの実行中のインスタンスを検索します。</span><span class="sxs-lookup"><span data-stu-id="6c867-118">This cache is searched for a running instance of a form server before the form libraries are searched for the form server.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6c867-119">既定のフォーム マネージャーは、ユーザーのワークステーションにフォームをインストールするときに進行状況インジケーターを表示し、ユーザーが操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="6c867-119">The default form manager displays a progress indicator when installing a form on a user's workstation, enabling the user to cancel the operation.</span></span> <span data-ttu-id="6c867-120">これは、フォーム サーバーの実行可能ファイルへのユーザーの接続が低帯域幅ネットワークを超える場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="6c867-120">This is especially useful if the user's connection to the form server's executable file is over a low bandwidth network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c867-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c867-121">See also</span></span>

- [<span data-ttu-id="6c867-122">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="6c867-122">MAPI Forms</span></span>](mapi-forms.md)

