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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333062"
---
# <a name="copying-a-recipient"></a><span data-ttu-id="38430-103">受信者のコピー</span><span class="sxs-lookup"><span data-stu-id="38430-103">Copying a Recipient</span></span>

  
  
<span data-ttu-id="38430-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38430-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38430-105">1つまたは複数の受信者を1つのコンテナーから別のコンテナーまたは同じコンテナーにコピーするには、最初にターゲットコンテナーが変更可能であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="38430-105">To copy one or more recipients from one container into another or the same container, first check that the target container is modifiable.</span></span> <span data-ttu-id="38430-106">変更可能なコンテナーは、 **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティで AB_MODIFIABLE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="38430-106">Containers that are modifiable set the AB_MODIFIABLE flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="38430-107">1つまたは複数のエントリを変更可能なコンテナーにコピーするには、destination コンテナーの[IABContainer:: copyentries](iabcontainer-copyentries.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="38430-107">To copy one or more entries into a modifiable container, call the destination container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method.</span></span> <span data-ttu-id="38430-108">アドレス帳エントリのコピーには時間がかかることがあるため、 **copyentries**は4つの入力パラメーターを受け取ります。コピーするエントリのエントリ識別子の配列、ウィンドウハンドル、進行状況インジケーター、およびフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="38430-108">Because copying address book entries can be time-consuming, **CopyEntries** accepts four input parameters: an array of entry identifiers for the entries to be copied, a window handle, a progress indicator, and a bitmask of flags.</span></span> 
  
<span data-ttu-id="38430-109">ウィンドウハンドルと進行状況インジケーターは、ユーザーに対する操作の状態を表示するためにアドレス帳プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="38430-109">The window handle and progress indicator are used by the address book provider to show the status of the operation to the user.</span></span> <span data-ttu-id="38430-110">進行状況を表示する場合は、 _uluiparam_パラメーターで進行状況インジケーターの親ウィンドウのウィンドウハンドルを渡し、 _ulflags_パラメーターに AB_NO_DIALOG フラグを設定しないようにします。</span><span class="sxs-lookup"><span data-stu-id="38430-110">If you want to display progress, pass a window handle for the parent window of the progress indicator in the  _ulUIParam_ parameter and do not set the AB_NO_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="38430-111">進行状況インジケーターを独自に実装している場合は、 _lpprogress_パラメーターで実装へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="38430-111">If you have your own implementation of a progress indicator, pass a pointer to the implementation in the  _lpProgress_ parameter.</span></span> <span data-ttu-id="38430-112">含まれていない場合は、NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="38430-112">If not, pass NULL.</span></span> <span data-ttu-id="38430-113">アドレス帳プロバイダーは、MAPI 進行状況インジケーターの実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="38430-113">The address book provider will use the MAPI progress indicator implementation.</span></span> 
  
<span data-ttu-id="38430-114">フラグのビットマスクは、進行状況のインジケーターを表示するかどうか、および重複するエントリチェックをどのように処理するかを示します。</span><span class="sxs-lookup"><span data-stu-id="38430-114">The bitmask of flags indicates whether or not you want to display a progress indicator and how duplicate entry checking should be handled.</span></span> <span data-ttu-id="38430-115">AB_NO_DIALOG フラグを設定して、進行状況インジケーターを抑制します。</span><span class="sxs-lookup"><span data-stu-id="38430-115">Set the AB_NO_DIALOG flag to suppress a progress indicator.</span></span> <span data-ttu-id="38430-116">CREATE_CHECK_DUP_LOOSE フラグを設定して、アドレス帳プロバイダーに対して重複を緩やかにチェックするように指示します。また、より厳密な重複チェックを行うには CREATE_CHECK_DUP_STRICT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="38430-116">Set the CREATE_CHECK_DUP_LOOSE flag to instruct the address book provider to loosely check for duplicates or the CREATE_CHECK_DUP_STRICT flag for stricter duplicate checking.</span></span> <span data-ttu-id="38430-117">CREATE_REPLACE フラグを設定して、プロバイダーが重複していることを確認したときに、既存のエントリを上書きコピーします。</span><span class="sxs-lookup"><span data-stu-id="38430-117">Set the CREATE_REPLACE flag to have copied entries replace existing entries when the provider determines there are duplicates.</span></span> 
  
<span data-ttu-id="38430-118">個人用アドレス帳 (PAB) コンテナーにコピーすると、プロバイダーによって、各エントリのプロパティの一部またはすべてがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="38430-118">When copying into a personal address book (PAB) container, the provider copies some or all of the properties for each entry.</span></span> <span data-ttu-id="38430-119">MAPI は、コンテナーコピー操作を実装するプロバイダーの要件を確立しないため、アドレス帳エントリと共にコピーされるプロパティの数と種類について前提条件を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="38430-119">Because MAPI does not establish requirements for providers implementing container copy operations, you cannot make assumptions about the number and type of properties that are copied with an address book entry.</span></span>
  

