---
title: 受信者のコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: dd68bc2054136a7f587b05dc56dbeabd06de1f08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799836"
---
# <a name="copying-a-recipient"></a><span data-ttu-id="0670d-103">受信者のコピー</span><span class="sxs-lookup"><span data-stu-id="0670d-103">Copying a Recipient</span></span>

  
  
<span data-ttu-id="0670d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0670d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0670d-105">別の 1 つのコンテナー、または同じコンテナーには、1 つまたは複数の受信者をコピーするに最初の移行先コンテナーが変更可能なことを確認します。</span><span class="sxs-lookup"><span data-stu-id="0670d-105">To copy one or more recipients from one container into another or the same container, first check that the target container is modifiable.</span></span> <span data-ttu-id="0670d-106">コンテナーを変更することは、 **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) のプロパティで、AB_MODIFIABLE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="0670d-106">Containers that are modifiable set the AB_MODIFIABLE flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="0670d-107">変更可能なコンテナーに 1 つまたは複数のエントリをコピーするには、移動先のコンテナーの[IABContainer::CopyEntries](iabcontainer-copyentries.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0670d-107">To copy one or more entries into a modifiable container, call the destination container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method.</span></span> <span data-ttu-id="0670d-108">アドレス帳のエントリをコピーできますが、時間がかかるため**CopyEntries**は 4 つの入力パラメーターを受け入れる: エントリをコピーする、ウィンドウ ハンドルを進行状況のインジケーター、およびフラグのビットマスクのエントリの識別子の配列。</span><span class="sxs-lookup"><span data-stu-id="0670d-108">Because copying address book entries can be time-consuming, **CopyEntries** accepts four input parameters: an array of entry identifiers for the entries to be copied, a window handle, a progress indicator, and a bitmask of flags.</span></span> 
  
<span data-ttu-id="0670d-109">ウィンドウのハンドルと進行状況のインジケーターは、ユーザーに操作のステータスを表示するのには、アドレス帳プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="0670d-109">The window handle and progress indicator are used by the address book provider to show the status of the operation to the user.</span></span> <span data-ttu-id="0670d-110">進行状況を表示する場合は、 _ulUIParam_パラメーターの進行状況のインジケーターの親ウィンドウのウィンドウ ハンドルを渡すし、 _ulFlags_パラメーターでは AB_NO_DIALOG フラグを設定しません。</span><span class="sxs-lookup"><span data-stu-id="0670d-110">If you want to display progress, pass a window handle for the parent window of the progress indicator in the  _ulUIParam_ parameter and do not set the AB_NO_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="0670d-111">独自の実装の進行状況のインジケーターを使っている場合、実装、 _lpProgress_パラメーターへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="0670d-111">If you have your own implementation of a progress indicator, pass a pointer to the implementation in the  _lpProgress_ parameter.</span></span> <span data-ttu-id="0670d-112">それ以外の場合は、NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="0670d-112">If not, pass NULL.</span></span> <span data-ttu-id="0670d-113">アドレス帳プロバイダーでは、MAPI の進行状況インジケーター実装を使用します。</span><span class="sxs-lookup"><span data-stu-id="0670d-113">The address book provider will use the MAPI progress indicator implementation.</span></span> 
  
<span data-ttu-id="0670d-114">フラグのビットマスクを示し、進行状況のインジケーターを表示するかどうか重複したエントリを処理するかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0670d-114">The bitmask of flags indicates whether or not you want to display a progress indicator and how duplicate entry checking should be handled.</span></span> <span data-ttu-id="0670d-115">進行状況のインジケーターが表示されないようにするのには AB_NO_DIALOG フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="0670d-115">Set the AB_NO_DIALOG flag to suppress a progress indicator.</span></span> <span data-ttu-id="0670d-116">緩やかに重複データをチェックするのには、アドレス帳プロバイダーに指示するための CREATE_CHECK_DUP_LOOSE フラグまたは重複チェックの厳密な CREATE_CHECK_DUP_STRICT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="0670d-116">Set the CREATE_CHECK_DUP_LOOSE flag to instruct the address book provider to loosely check for duplicates or the CREATE_CHECK_DUP_STRICT flag for stricter duplicate checking.</span></span> <span data-ttu-id="0670d-117">エントリをコピーするのには CREATE_REPLACE フラグを設定しますは、プロバイダーは重複を決定するときに既存のエントリを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0670d-117">Set the CREATE_REPLACE flag to have copied entries replace existing entries when the provider determines there are duplicates.</span></span> 
  
<span data-ttu-id="0670d-118">個人用アドレス帳 (PAB) コンテナーにコピーする場合、プロバイダーは、各エントリのプロパティの一部またはすべてをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0670d-118">When copying into a personal address book (PAB) container, the provider copies some or all of the properties for each entry.</span></span> <span data-ttu-id="0670d-119">MAPI は、コンテナーのコピー操作を実装するプロバイダーの要件を確立していない、ために、エントリをアドレス帳にコピーされるプロパティの種類と数についての前提条件を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="0670d-119">Because MAPI does not establish requirements for providers implementing container copy operations, you cannot make assumptions about the number and type of properties that are copied with an address book entry.</span></span>
  

