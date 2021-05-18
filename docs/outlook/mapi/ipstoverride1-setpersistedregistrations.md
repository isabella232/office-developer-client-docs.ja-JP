---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408349"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="97fa0-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="97fa0-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="97fa0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97fa0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97fa0-105">自動ロック解除用に個人用フォルダー (.pst) ファイルを登録し、HrTrustedPSTOverrideHandlerCallback へのそれ以上の呼び出しを回避します。</span><span class="sxs-lookup"><span data-stu-id="97fa0-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="97fa0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97fa0-106">Parameters</span></span>

<span data-ttu-id="97fa0-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="97fa0-107">_pmval_</span></span>
  
> <span data-ttu-id="97fa0-108">[in]登録するダイナミック リンク ライブラリ (DLL) のパスへのポインターを含む [SPropValue](spropvalue.md) 構造体。</span><span class="sxs-lookup"><span data-stu-id="97fa0-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="97fa0-109">構造には、次の特性があります。</span><span class="sxs-lookup"><span data-stu-id="97fa0-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="97fa0-110">ulPropTag [のPROP_TAG](prop_tag.md)(PT_MV_UNICODE、PROP_ID_NULL)。</span><span class="sxs-lookup"><span data-stu-id="97fa0-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="97fa0-111">NULL 終端 Unicode 文字文字列の配列に設定される MVszW 値プロパティ。</span><span class="sxs-lookup"><span data-stu-id="97fa0-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="97fa0-112">詳細については [、「SWStringArray」を参照](swstringarray.md) してください。</span><span class="sxs-lookup"><span data-stu-id="97fa0-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="97fa0-113">SPropValue は、PST の内部範囲の MAPI プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="97fa0-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="97fa0-114">このプロパティは、通常の MAPI アプリケーションにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="97fa0-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="97fa0-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="97fa0-115">Return value</span></span>

<span data-ttu-id="97fa0-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="97fa0-116">S_OK</span></span> 
  
> <span data-ttu-id="97fa0-117">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="97fa0-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97fa0-118">注釈</span><span class="sxs-lookup"><span data-stu-id="97fa0-118">Remarks</span></span>

<span data-ttu-id="97fa0-119">永続登録は、PST を開くデスクトップ検索やデスクトップ検索Outlook Windowsパフォーマンスに悪影響を及ぼす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="97fa0-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="97fa0-120">永続登録の使用法を使用または拡張する場合のパフォーマンス効果を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="97fa0-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="97fa0-121">このメソッドは Unicode でのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="97fa0-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="97fa0-122">さらに、配列内のパスにファイル名の拡張子が含.dll。</span><span class="sxs-lookup"><span data-stu-id="97fa0-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97fa0-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="97fa0-123">See also</span></span>

- [<span data-ttu-id="97fa0-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97fa0-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="97fa0-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97fa0-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

