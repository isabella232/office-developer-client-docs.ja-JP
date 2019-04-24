---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315520"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="e5c69-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="e5c69-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="e5c69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5c69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5c69-105">ラップが解除され、同期を呼び出してアイテムをダウンロードすることなく個人用フォルダーファイル (PST) 内のアイテムにアクセスできるようにする、インターネットメッセージアクセスプロトコル (IMAP) ストアオブジェクトを提供します。</span><span class="sxs-lookup"><span data-stu-id="e5c69-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e5c69-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e5c69-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5c69-107">継承元:</span><span class="sxs-lookup"><span data-stu-id="e5c69-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="e5c69-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5c69-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="e5c69-109">提供元:</span><span class="sxs-lookup"><span data-stu-id="e5c69-109">Provided By:</span></span>  <br/> |<span data-ttu-id="e5c69-110">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="e5c69-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="e5c69-111">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="e5c69-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e5c69-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="e5c69-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e5c69-113">v の順序</span><span class="sxs-lookup"><span data-stu-id="e5c69-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="e5c69-114">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="e5c69-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e5c69-115">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="e5c69-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="e5c69-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="e5c69-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="e5c69-117">ラップされていない IMAP ストアへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="e5c69-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="e5c69-118">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="e5c69-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e5c69-119">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="e5c69-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5c69-120">解説</span><span class="sxs-lookup"><span data-stu-id="e5c69-120">Remarks</span></span>

<span data-ttu-id="e5c69-121">**iproxystoreobject**インターフェイスを取得するには、ソースメッセージストアで[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e5c69-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="e5c69-122">その後、 **iproxystoreobject:: UnwrapNoRef**を呼び出して、ラップ解除された store オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="e5c69-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="e5c69-123">**QueryInterface**がエラー **MAPI_E_INTERFACE_NOT_SUPPORTED**を返した場合、ストアはラップされていません。</span><span class="sxs-lookup"><span data-stu-id="e5c69-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="e5c69-124">**UnwrapNoRef**は、ラップされていない store オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないため、 **UnwrapNoRef**の呼び出しに成功した後で、 [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出して参照カウントを維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5c69-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

