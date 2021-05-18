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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315520"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="3230d-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="3230d-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="3230d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3230d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3230d-105">インターネット メッセージ アクセス プロトコル (IMAP) ストア オブジェクトを提供します。このオブジェクトを使用すると、同期を呼び出してアイテムをダウンロードすることなく、個人用フォルダー ファイル (PST) 内のアイテムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3230d-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3230d-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3230d-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3230d-107">継承元:</span><span class="sxs-lookup"><span data-stu-id="3230d-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="3230d-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="3230d-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="3230d-109">提供者:</span><span class="sxs-lookup"><span data-stu-id="3230d-109">Provided By:</span></span>  <br/> |<span data-ttu-id="3230d-110">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3230d-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="3230d-111">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="3230d-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3230d-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="3230d-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3230d-113">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="3230d-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="3230d-114">*プレースホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="3230d-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3230d-115">*サポートされていないか、文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="3230d-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="3230d-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="3230d-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="3230d-117">ラップされていない IMAP ストアへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="3230d-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="3230d-118">*プレースホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="3230d-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3230d-119">*サポートされていないか、文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="3230d-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3230d-120">注釈</span><span class="sxs-lookup"><span data-stu-id="3230d-120">Remarks</span></span>

<span data-ttu-id="3230d-121">IProxyStoreObject インターフェイスを取得するには、ソース メッセージ ストアで **IUnknown::QueryInterface を呼び出** します。 [](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3230d-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="3230d-122">次に **、IProxyStoreObject::UnwrapNoRef** を呼び出して、ラップされていないストア オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="3230d-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="3230d-123">**QueryInterface がエラー** メッセージを返 **MAPI_E_INTERFACE_NOT_SUPPORTED、** ストアはラップされません。</span><span class="sxs-lookup"><span data-stu-id="3230d-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="3230d-124">**UnwrapNoRef** はアンラップされたストア オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないので **、UnwrapNoRef** を正常に呼び出した後、参照カウントを維持するために [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3230d-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

