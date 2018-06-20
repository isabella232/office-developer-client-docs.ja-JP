---
title: ディスク インスタンスおよびキャッシュのテーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c3b371a226c9eb6a3cf675ee316bf22a597fe806
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799926"
---
# <a name="disk-instances-and-cache-tables"></a><span data-ttu-id="e0b70-103">ディスク インスタンスおよびキャッシュのテーブル</span><span class="sxs-lookup"><span data-stu-id="e0b70-103">Disk Instances and Cache Tables</span></span>

<span data-ttu-id="e0b70-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0b70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0b70-105">フォームをアクティブにするには、実行可能ファイルをユーザーのコンピューターで使用できるにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0b70-105">To activate a form, its executable files must be available on the user's computer.</span></span> <span data-ttu-id="e0b70-106">利用できない場合は、これらでローカル ディスクにフォーム ライブラリからにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0b70-106">If they are not available, they must be copied from the form library to the local disk.</span></span> <span data-ttu-id="e0b70-107">これを行うには、既定のフォーム マネージャーは、フォームの実行可能ファイルを格納するユーザーの Windows ディレクトリのサブディレクトリを作成 (。Exe、します。HLPs)。</span><span class="sxs-lookup"><span data-stu-id="e0b70-107">To do this, the default form manager creates a subdirectory in the user's Windows directory to contain the form's executable files (.EXEs,.HLPs).</span></span> <span data-ttu-id="e0b70-108">このディレクトリは、"フォームのディスク インスタンス"と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e0b70-108">This directory is referred to as the disk instance of the form.</span></span>
  
<span data-ttu-id="e0b70-109">ディスクのインスタンスが既に存在する場合、フォーム ライブラリからユーザーのディスクにファイルをコピーすることがなく使用できますように、既定のフォーム マネージャーはディスクのすべてのインスタンスのテーブルを保持します。</span><span class="sxs-lookup"><span data-stu-id="e0b70-109">The default form manager maintains a table of all disk instances so that if a disk instance already exists it can be used without having to copy files from the form library to the user's disk.</span></span> <span data-ttu-id="e0b70-110">ディスク インスタンスのテーブルは、最も頻繁に使用するキャッシュとして管理されます。</span><span class="sxs-lookup"><span data-stu-id="e0b70-110">The table of disk instances is managed as a least-frequently-used cache.</span></span> <span data-ttu-id="e0b70-111">ディスクの新しいインスタンスが必要な場合は、最も頻繁に使用するディスクのインスタンスを置き換える、ユーザーのコンピューターにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="e0b70-111">If a new disk instance is needed, it is copied to the user's computer, replacing the least-frequently-used disk instance.</span></span> <span data-ttu-id="e0b70-112">ディスクのインスタンスのキャッシュ テーブルが最新の構成を反映するように更新されます。</span><span class="sxs-lookup"><span data-stu-id="e0b70-112">The disk instance cache table is then updated to reflect the latest configuration.</span></span> <span data-ttu-id="e0b70-113">ディスク キャッシュのサイズは、ユーザーが利用可能なディスク容量と速度のバランスを有効にすると、ユーザーが構成可能なオプションです。</span><span class="sxs-lookup"><span data-stu-id="e0b70-113">The size of the disk cache is a user-configurable option, enabling users to balance speed with available disk capacity.</span></span>
  
<span data-ttu-id="e0b70-114">だけでなく、ディスクのインスタンスのキャッシュは、デフォルト フォームのマネージャーは、ユーザーのコンピューター上のフォームのサーバーの実行中のすべてのインスタンスを一覧表示する実行中のインスタンスのテーブルを保持します。</span><span class="sxs-lookup"><span data-stu-id="e0b70-114">In addition to the disk instance cache, the default form manager maintains a running instance table that lists all running instances of form servers on the user's computer.</span></span> <span data-ttu-id="e0b70-115">そのフォーム クラスがアクティブになったサーバーのメッセージを形成するまで非表示の状態で実行しているアイドル状態のフォームのインスタンスを保持するのには MAPI の機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="e0b70-115">This uses MAPI's ability to keep idle form instances running in an invisible state until a form of that form server's message class is activated.</span></span> <span data-ttu-id="e0b70-116">つまり、フォームのサーバーは、フォームの実行可能ファイルをフォーム ライブラリ内にある、ディスクまたはネットワーク上でのメモリに読み込まれる必要があります回数を最小限に抑えるための RAM にキャッシュできます。</span><span class="sxs-lookup"><span data-stu-id="e0b70-116">In other words, form servers can be cached in RAM to minimize the number of times a form's executable must be located within a form library and loaded into memory from disk or over the network.</span></span> <span data-ttu-id="e0b70-117">ディスク インスタンス キャッシュのように実行中のインスタンスのキャッシュは実行中のフォーム インスタンスは、フォーム インスタンスを別の場所を確保するためにキャッシュからパージできるようにするために最も頻繁に使用方法で動作します。</span><span class="sxs-lookup"><span data-stu-id="e0b70-117">Like the disk instance cache, the running instance cache behaves in a least-frequently-used fashion so that a running form instance can be purged from the cache to make room for another form instance.</span></span> <span data-ttu-id="e0b70-118">フォーム サーバーのフォーム ライブラリを検索する前に、フォームのサーバーの実行中のインスタンスにこのキャッシュが検索されます。</span><span class="sxs-lookup"><span data-stu-id="e0b70-118">This cache is searched for a running instance of a form server before the form libraries are searched for the form server.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e0b70-119">既定のフォーム マネージャーが表示されます、進行状況インジケーター ユーザーのワークステーションでは、フォームをインストールするときに操作をキャンセルするユーザーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="e0b70-119">The default form manager displays a progress indicator when installing a form on a user's workstation, enabling the user to cancel the operation.</span></span> <span data-ttu-id="e0b70-120">フォーム サーバーの実行可能ファイルへのユーザーの接続は、低帯域幅ネットワークを経由する場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="e0b70-120">This is especially useful if the user's connection to the form server's executable file is over a low bandwidth network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0b70-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0b70-121">See also</span></span>

- [<span data-ttu-id="e0b70-122">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="e0b70-122">MAPI Forms</span></span>](mapi-forms.md)

