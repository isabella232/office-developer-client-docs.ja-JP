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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7c6c763e918947c423c5dae283b0d4ab2f880616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801151"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="0dd83-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="0dd83-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="0dd83-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0dd83-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0dd83-105">同期を呼び出すと、アイテムをダウンロードせず、元の個人用フォルダー ファイル (PST) へのアクセスを提供する、インターネット メッセージ アクセス プロトコル (IMAP) ラップ解除済みストア オブジェクトにポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="0dd83-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="0dd83-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0dd83-106">Parameters</span></span>

 <span data-ttu-id="0dd83-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="0dd83-107">_ppvObject_</span></span>
  
> <span data-ttu-id="0dd83-108">[out]ポインター、 [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)ストア オブジェクトをラップすることはありません。</span><span class="sxs-lookup"><span data-stu-id="0dd83-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="0dd83-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="0dd83-109">Return values</span></span>

<span data-ttu-id="0dd83-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0dd83-110">S_OK</span></span>
  
- <span data-ttu-id="0dd83-111">呼び出しが成功したし、 _ppvObject_で返されたラップが解除されたインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0dd83-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0dd83-112">備考</span><span class="sxs-lookup"><span data-stu-id="0dd83-112">Remarks</span></span>

<span data-ttu-id="0dd83-113">せず、最初に、IMAP ストアのラップを解除、ストア内のメッセージにアクセスすることができます、強制的に同期メッセージ全体をダウンロードしようとします。</span><span class="sxs-lookup"><span data-stu-id="0dd83-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="0dd83-114">ラップが解除されたストアを使用すると、ダウンロードをトリガーすることがなく現在の状態のメッセージへのアクセスができます。</span><span class="sxs-lookup"><span data-stu-id="0dd83-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="0dd83-115">**UnwrapNoRef**では、 **UnwrapNoRef**の呼び出しに成功した後はこの新しいオブジェクトへのポインター、ラップが解除されたストアでの参照カウントは増分されません、ために、参照カウントを維持するために[IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0dd83-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](http://msdn.microsoft.com/ja-jp/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0dd83-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="0dd83-116">See also</span></span>



[<span data-ttu-id="0dd83-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="0dd83-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

