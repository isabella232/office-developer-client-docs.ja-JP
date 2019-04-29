---
title: ifoldersupport IUnknown
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
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="24e72-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24e72-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="24e72-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24e72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24e72-105">フォルダーの共有のサポートに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="24e72-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24e72-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="24e72-106">Provided by:</span></span>  <br/> |<span data-ttu-id="24e72-107">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="24e72-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="24e72-108">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="24e72-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="24e72-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="24e72-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="24e72-110">v の順序</span><span class="sxs-lookup"><span data-stu-id="24e72-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24e72-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="24e72-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="24e72-112">フォルダーの共有のサポートに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="24e72-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24e72-113">注釈</span><span class="sxs-lookup"><span data-stu-id="24e72-113">Remarks</span></span>

<span data-ttu-id="24e72-114">通常、プロバイダーがフォルダーを共有する場合、Microsoft Office Outlook では、このインターフェイスを実装するために MAPI ストアプロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="24e72-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="24e72-115">例外は、このインターフェイスを実装せずにフォルダーを共有できる Exchange サーバーストアプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="24e72-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="24e72-116">クライアントは、 **ifoldersupport**の**[imapifolder](imapifolderimapicontainer.md)** に対してクエリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="24e72-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="24e72-117">成功した場合は、 **ifoldersupport:: getsupportmask**を呼び出し、 **FS_SUPPORTS_SHARING**ビットが設定されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="24e72-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

