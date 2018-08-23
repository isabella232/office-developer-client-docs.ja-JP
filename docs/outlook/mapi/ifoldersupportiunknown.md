---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d17de9cc11bd791c75b83093a0431c138fd606d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564172"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="e7fad-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7fad-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="e7fad-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7fad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7fad-105">共有フォルダーのサポートに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e7fad-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7fad-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="e7fad-106">Provided by:</span></span>  <br/> |<span data-ttu-id="e7fad-107">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e7fad-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="e7fad-108">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="e7fad-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e7fad-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="e7fad-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e7fad-110">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e7fad-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7fad-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="e7fad-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="e7fad-112">共有フォルダーのサポートに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="e7fad-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7fad-113">注釈</span><span class="sxs-lookup"><span data-stu-id="e7fad-113">Remarks</span></span>

<span data-ttu-id="e7fad-114">一般に、Microsoft Office Outlook は MAPI プロバイダーは、フォルダーを共有する必要がある場合は、このインターフェイスを実装するプロバイダーを格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7fad-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="e7fad-115">例外は、Exchange Server のストア プロバイダーでこのインターフェイスを実装しなくてもフォルダーを共有することができます。</span><span class="sxs-lookup"><span data-stu-id="e7fad-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="e7fad-116">クライアントは、 **IFolderSupport** **[IMAPIFolder](imapifolderimapicontainer.md)** を照会できます。</span><span class="sxs-lookup"><span data-stu-id="e7fad-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="e7fad-117">成功した場合、 **IFolderSupport::GetSupportMask**を呼び出すし、 **FS_SUPPORTS_SHARING**ビットが設定されるを確認します。</span><span class="sxs-lookup"><span data-stu-id="e7fad-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

