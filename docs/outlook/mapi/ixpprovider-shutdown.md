---
title: IXPProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f5d253d0306e55699fbe5b9c9decf8c3242867fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801264"
---
# <a name="ixpprovidershutdown"></a><span data-ttu-id="246e4-103">IXPProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="246e4-103">IXPProvider::Shutdown</span></span>

  
  
<span data-ttu-id="246e4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="246e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="246e4-105">適切な順序でトランスポート プロバイダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="246e4-105">Closes down a transport provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="246e4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="246e4-106">Parameters</span></span>

 <span data-ttu-id="246e4-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="246e4-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="246e4-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="246e4-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="246e4-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="246e4-109">Return value</span></span>

<span data-ttu-id="246e4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="246e4-110">S_OK</span></span> 
  
> <span data-ttu-id="246e4-111">トランスポート プロバイダーのシャット ダウンの呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="246e4-111">The call succeeded in shutting down the transport provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="246e4-112">注釈</span><span class="sxs-lookup"><span data-stu-id="246e4-112">Remarks</span></span>

<span data-ttu-id="246e4-113">MAPI スプーラーでは、トランスポート プロバイダーのオブジェクトを解放する前に**IXPProvider::Shutdown**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="246e4-113">The MAPI spooler calls the **IXPProvider::Shutdown** method just prior to releasing a transport provider object.</span></span> <span data-ttu-id="246e4-114">**シャット ダウン**を呼び出す前に、MAPI は、プロバイダーのすべてのログオン オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="246e4-114">Before calling **Shutdown**, MAPI releases all logon objects for a provider.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="246e4-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="246e4-115">See also</span></span>



[<span data-ttu-id="246e4-116">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="246e4-116">XPProviderInit</span></span>](xpproviderinit.md)
  
[<span data-ttu-id="246e4-117">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="246e4-117">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)

