---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: 311d055e0a319ec26cdc4eba5ac3b50dc9e63d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565180"
---
# <a name="iolkerrorunknown"></a><span data-ttu-id="c9aa9-102">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="c9aa9-102">IOlkErrorUnknown</span></span>

<span data-ttu-id="c9aa9-103">最後のエラーに関する追加情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c9aa9-103">Provides extra information about the last error.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c9aa9-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="c9aa9-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9aa9-105">継承します。</span><span class="sxs-lookup"><span data-stu-id="c9aa9-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="c9aa9-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9aa9-106">IUnknown</span></span>](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="c9aa9-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="c9aa9-107">Provided by:</span></span>  <br/> |<span data-ttu-id="c9aa9-108">クライアント</span><span class="sxs-lookup"><span data-stu-id="c9aa9-108">Client</span></span>  <br/> |
|<span data-ttu-id="c9aa9-109">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="c9aa9-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c9aa9-110">IID_IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="c9aa9-110">IID_IOlkErrorUnknown</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c9aa9-111">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="c9aa9-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c9aa9-112">発生しました</span><span class="sxs-lookup"><span data-stu-id="c9aa9-112">GetLastError</span></span>](iolkerrorunknown-getlasterror.md) <br/> |<span data-ttu-id="c9aa9-113">指定されたエラー メッセージ文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="c9aa9-113">Gets a message string for the specified error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9aa9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c9aa9-114">Remarks</span></span>

<span data-ttu-id="c9aa9-115">このインターフェイスは、 [IOlkAccountManager](iolkaccountmanager.md)、 [IOlkAccountNotify](iolkaccountnotify.md)、および[IOlkAccount](iolkaccount.md)でのエラーに関する追加情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c9aa9-115">This interface provides extra information about an error in [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md), and [IOlkAccount](iolkaccount.md).</span></span> <span data-ttu-id="c9aa9-116">また、 **IOlkAccountManager**、 **IOlkAccountNotify**、および**IOlkAccount**の基本インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="c9aa9-116">It is also the base interface for **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9aa9-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9aa9-117">See also</span></span>

- [<span data-ttu-id="c9aa9-118">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="c9aa9-118">About the Account Management API</span></span>](about-the-account-management-api.md)

