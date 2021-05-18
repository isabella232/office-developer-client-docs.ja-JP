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
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="44e23-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="44e23-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="44e23-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44e23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44e23-105">同期を呼び出してアイテムをダウンロードすることなく、基になる個人用フォルダー ファイル (PST) へのアクセスを提供する、ラップされていないインターネット メッセージ アクセス プロトコル (IMAP) ストア オブジェクトへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="44e23-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="44e23-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="44e23-106">Parameters</span></span>

 <span data-ttu-id="44e23-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="44e23-107">_ppvObject_</span></span>
  
> <span data-ttu-id="44e23-108">[out]ラップされていない [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) ストア オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="44e23-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="44e23-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="44e23-109">Return values</span></span>

<span data-ttu-id="44e23-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="44e23-110">S_OK</span></span>
  
- <span data-ttu-id="44e23-111">呼び出しが成功し、ラップされていないインターフェイスへのポインターが  _ppvObject で返されました_。</span><span class="sxs-lookup"><span data-stu-id="44e23-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44e23-112">注釈</span><span class="sxs-lookup"><span data-stu-id="44e23-112">Remarks</span></span>

<span data-ttu-id="44e23-113">最初に IMAP ストアをアンラップしない場合、ストア内のメッセージにアクセスすると、メッセージ全体のダウンロードを試みる同期を強制的に実行できます。</span><span class="sxs-lookup"><span data-stu-id="44e23-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="44e23-114">ラップされていないストアを使用すると、ダウンロードをトリガーすることなく、現在の状態にあるメッセージにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="44e23-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="44e23-115">**UnwrapNoRef** はアンラップされたストア オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないので **、UnwrapNoRef** を正常に呼び出した後、参照カウントを維持するために [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="44e23-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44e23-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="44e23-116">See also</span></span>



[<span data-ttu-id="44e23-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="44e23-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

