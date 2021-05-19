---
title: 受信者のコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3a4fb1a3f76481bf1960c251a33911b871a8791c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419087"
---
# <a name="copying-a-recipient"></a><span data-ttu-id="84841-103">受信者のコピー</span><span class="sxs-lookup"><span data-stu-id="84841-103">Copying a Recipient</span></span>

  
  
<span data-ttu-id="84841-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84841-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84841-105">1 つのコンテナーから別のコンテナーまたは同じコンテナーに 1 つ以上の受信者をコピーするには、まずターゲット コンテナーが変更可能なことを確認します。</span><span class="sxs-lookup"><span data-stu-id="84841-105">To copy one or more recipients from one container into another or the same container, first check that the target container is modifiable.</span></span> <span data-ttu-id="84841-106">変更可能なコンテナーは、AB_MODIFIABLE **(** [PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティPR_CONTAINER_FLAGSフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="84841-106">Containers that are modifiable set the AB_MODIFIABLE flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="84841-107">1 つ以上のエントリを変更可能なコンテナーにコピーするには、宛先コンテナーの [IABContainer::CopyEntries メソッドを呼び出](iabcontainer-copyentries.md) します。</span><span class="sxs-lookup"><span data-stu-id="84841-107">To copy one or more entries into a modifiable container, call the destination container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method.</span></span> <span data-ttu-id="84841-108">アドレス帳エントリのコピーには時間がかかる可能性があります **。CopyEntries** は、コピーするエントリのエントリ識別子の配列、ウィンドウ ハンドル、進行状況インジケーター、フラグのビットマスクの 4 つの入力パラメーターを受け入れる。</span><span class="sxs-lookup"><span data-stu-id="84841-108">Because copying address book entries can be time-consuming, **CopyEntries** accepts four input parameters: an array of entry identifiers for the entries to be copied, a window handle, a progress indicator, and a bitmask of flags.</span></span> 
  
<span data-ttu-id="84841-109">ウィンドウ ハンドルと進行状況インジケーターは、アドレス帳プロバイダーによって操作の状態をユーザーに表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="84841-109">The window handle and progress indicator are used by the address book provider to show the status of the operation to the user.</span></span> <span data-ttu-id="84841-110">進行状況を表示する場合は  _、ulUIParam_ パラメーターの進行状況インジケーターの親ウィンドウのウィンドウ ハンドルを渡し  _、ulFlags_ パラメーターに AB_NO_DIALOG フラグを設定しない。</span><span class="sxs-lookup"><span data-stu-id="84841-110">If you want to display progress, pass a window handle for the parent window of the progress indicator in the  _ulUIParam_ parameter and do not set the AB_NO_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="84841-111">進行状況インジケーターの独自の実装がある場合は  _、lpProgress_ パラメーターの実装へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="84841-111">If you have your own implementation of a progress indicator, pass a pointer to the implementation in the  _lpProgress_ parameter.</span></span> <span data-ttu-id="84841-112">指定しない場合は、NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="84841-112">If not, pass NULL.</span></span> <span data-ttu-id="84841-113">アドレス帳プロバイダーは、MAPI 進行状況インジケーターの実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="84841-113">The address book provider will use the MAPI progress indicator implementation.</span></span> 
  
<span data-ttu-id="84841-114">フラグのビットマスクは、進行状況インジケーターを表示するかどうか、および重複するエントリチェックの処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="84841-114">The bitmask of flags indicates whether or not you want to display a progress indicator and how duplicate entry checking should be handled.</span></span> <span data-ttu-id="84841-115">進行状況インジケーターをAB_NO_DIALOGするフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="84841-115">Set the AB_NO_DIALOG flag to suppress a progress indicator.</span></span> <span data-ttu-id="84841-116">重複をCREATE_CHECK_DUP_LOOSEチェックするようにアドレス帳プロバイダーに指示する場合は、CREATE_CHECK_DUP_LOOSEフラグを設定し、重複のチェックを厳密に行CREATE_CHECK_DUP_STRICTフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="84841-116">Set the CREATE_CHECK_DUP_LOOSE flag to instruct the address book provider to loosely check for duplicates or the CREATE_CHECK_DUP_STRICT flag for stricter duplicate checking.</span></span> <span data-ttu-id="84841-117">プロバイダーが重複CREATE_REPLACE判断した場合に、コピーされたエントリが既存のエントリに置き換わるかどうかを示すフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="84841-117">Set the CREATE_REPLACE flag to have copied entries replace existing entries when the provider determines there are duplicates.</span></span> 
  
<span data-ttu-id="84841-118">個人用アドレス帳 (PAB) コンテナーにコピーする場合、プロバイダーは各エントリのプロパティの一部またはすべてをコピーします。</span><span class="sxs-lookup"><span data-stu-id="84841-118">When copying into a personal address book (PAB) container, the provider copies some or all of the properties for each entry.</span></span> <span data-ttu-id="84841-119">MAPI はコンテナー コピー操作を実装するプロバイダーの要件を確立しないので、アドレス帳エントリでコピーされるプロパティの数と種類を想定することはできません。</span><span class="sxs-lookup"><span data-stu-id="84841-119">Because MAPI does not establish requirements for providers implementing container copy operations, you cannot make assumptions about the number and type of properties that are copied with an address book entry.</span></span>
  

