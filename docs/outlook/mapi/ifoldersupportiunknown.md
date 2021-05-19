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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415776"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="6e829-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e829-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="6e829-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e829-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e829-105">フォルダーの共有のサポートに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6e829-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e829-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="6e829-106">Provided by:</span></span>  <br/> |<span data-ttu-id="6e829-107">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6e829-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="6e829-108">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="6e829-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6e829-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="6e829-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6e829-110">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="6e829-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e829-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="6e829-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="6e829-112">フォルダーの共有のサポートに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="6e829-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e829-113">注釈</span><span class="sxs-lookup"><span data-stu-id="6e829-113">Remarks</span></span>

<span data-ttu-id="6e829-114">通常、Microsoft Office Outlookを共有する場合は、MAPI ストア プロバイダーがこのインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e829-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="6e829-115">例外は、このExchange Server実装せずにフォルダーを共有できるストア プロバイダーの例外です。</span><span class="sxs-lookup"><span data-stu-id="6e829-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="6e829-116">クライアントは **[、IFolderSupport の IMAPIFolder](imapifolderimapicontainer.md)** **を照会できます**。</span><span class="sxs-lookup"><span data-stu-id="6e829-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="6e829-117">これが成功した場合は **、IFolderSupport::GetSupportMask** を呼び出し、FS_SUPPORTS_SHARING **を確認** します。</span><span class="sxs-lookup"><span data-stu-id="6e829-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

