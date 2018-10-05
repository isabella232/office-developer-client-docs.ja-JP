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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395309"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="7d1ad-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="7d1ad-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="7d1ad-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d1ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d1ad-105">ラップするがされたため、同期を呼び出すと、アイテムをダウンロードしなくても、個人用フォルダー ファイル (PST) 内のアイテムへのアクセスを許可するインターネット メッセージ アクセス プロトコル (IMAP) ストア オブジェクトを提供します。</span><span class="sxs-lookup"><span data-stu-id="7d1ad-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7d1ad-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="7d1ad-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d1ad-107">継承されます。</span><span class="sxs-lookup"><span data-stu-id="7d1ad-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="7d1ad-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d1ad-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="7d1ad-109">によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="7d1ad-109">Provided By:</span></span>  <br/> |<span data-ttu-id="7d1ad-110">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="7d1ad-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="7d1ad-111">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="7d1ad-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7d1ad-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="7d1ad-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7d1ad-113">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="7d1ad-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="7d1ad-114">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="7d1ad-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="7d1ad-115">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="7d1ad-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="7d1ad-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="7d1ad-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="7d1ad-117">ラップ解除済みの IMAP ストアへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="7d1ad-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="7d1ad-118">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="7d1ad-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="7d1ad-119">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="7d1ad-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d1ad-120">備考</span><span class="sxs-lookup"><span data-stu-id="7d1ad-120">Remarks</span></span>

<span data-ttu-id="7d1ad-121">**IProxyStoreObject**インターフェイスを取得するのには元のメッセージ ストアには、 [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7d1ad-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="7d1ad-122">ラップ解除済みストア オブジェクトを取得する**IProxyStoreObject::UnwrapNoRef**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7d1ad-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="7d1ad-123">**QueryInterface**には、エラー **MAPI_E_INTERFACE_NOT_SUPPORTED**が返された場合、ストアがされてラップされません。</span><span class="sxs-lookup"><span data-stu-id="7d1ad-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="7d1ad-124">**UnwrapNoRef**では、 **UnwrapNoRef**の呼び出しに成功した後はこの新しいオブジェクトへのポインター、ラップが解除されたストアでの参照カウントは増分されません、ために、参照カウントを維持するために[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d1ad-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

