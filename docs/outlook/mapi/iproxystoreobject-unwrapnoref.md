---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320154"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="d4a75-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="d4a75-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="d4a75-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4a75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4a75-105">同期を呼び出してアイテムをダウンロードすることなく、基になる個人用フォルダーファイル (PST) へのアクセスを提供する、ラップされていないインターネットメッセージアクセスプロトコル (IMAP) ストアオブジェクトへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="d4a75-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="d4a75-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d4a75-106">Parameters</span></span>

 <span data-ttu-id="d4a75-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="d4a75-107">_ppvObject_</span></span>
  
> <span data-ttu-id="d4a75-108">読み上げラップされていない[IMsgStore: imapiprop](imsgstoreimapiprop.md) store オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d4a75-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d4a75-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="d4a75-109">Return values</span></span>

<span data-ttu-id="d4a75-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4a75-110">S_OK</span></span>
  
- <span data-ttu-id="d4a75-111">呼び出しが正常に実行され、 _ppvObject_でラップされていないインターフェイスへのポインターが返されました。</span><span class="sxs-lookup"><span data-stu-id="d4a75-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4a75-112">解説</span><span class="sxs-lookup"><span data-stu-id="d4a75-112">Remarks</span></span>

<span data-ttu-id="d4a75-113">最初に IMAP ストアをラップ解除せずに、ストア内のメッセージにアクセスすると、メッセージ全体をダウンロードしようとする同期が強制的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d4a75-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="d4a75-114">ラップされていないストアを使用すると、ダウンロードをトリガーすることなく、現在の状態のメッセージにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d4a75-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="d4a75-115">**UnwrapNoRef**は、ラップされていない store オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないため、 **UnwrapNoRef**の呼び出しに成功した後で、 [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出して参照カウントを維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4a75-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4a75-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4a75-116">See also</span></span>



[<span data-ttu-id="d4a75-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="d4a75-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

