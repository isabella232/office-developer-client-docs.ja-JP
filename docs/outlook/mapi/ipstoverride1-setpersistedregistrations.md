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
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 9895c558af94eebebe2dacdb6f9bf674e3de6263
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801187"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="752fc-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="752fc-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="752fc-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="752fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="752fc-105">それ以降、HrTrustedPSTOverrideHandlerCallback の呼び出しを回避する自動ロック解除では、個人用フォルダー (.pst) ファイルを登録します。</span><span class="sxs-lookup"><span data-stu-id="752fc-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="752fc-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="752fc-106">Parameters</span></span>

<span data-ttu-id="752fc-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="752fc-107">_pmval_</span></span>
  
> <span data-ttu-id="752fc-108">[in][SPropValue](spropvalue.md)構造のダイナミック リンク ライブラリ (DLL) が登録するパスへのポインターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="752fc-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="752fc-109">構造体には、次の特徴があります。</span><span class="sxs-lookup"><span data-stu-id="752fc-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="752fc-110">[PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL) の ulPropTag です。</span><span class="sxs-lookup"><span data-stu-id="752fc-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="752fc-111">Unicode 文字の null で終わる文字列の配列に設定されている MVszW 値プロパティです。</span><span class="sxs-lookup"><span data-stu-id="752fc-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="752fc-112">詳細については、 [SWStringArray](swstringarray.md)のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="752fc-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="752fc-113">SPropValue は、pst ファイルの内部の範囲の MAPI プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="752fc-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="752fc-114">このプロパティは、通常の MAPI アプリケーションにアクセス可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="752fc-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="752fc-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="752fc-115">Return value</span></span>

<span data-ttu-id="752fc-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="752fc-116">S_OK</span></span> 
  
> <span data-ttu-id="752fc-117">関数の呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="752fc-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="752fc-118">注釈</span><span class="sxs-lookup"><span data-stu-id="752fc-118">Remarks</span></span>

<span data-ttu-id="752fc-119">永続的な登録には、pst ファイルを開く Windows デスクトップ サーチでは、Outlook などのアプリケーションのパフォーマンスに悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="752fc-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="752fc-120">使用するか、永続的な登録の使用法を拡張するときにパフォーマンスに与える影響を検討してください。</span><span class="sxs-lookup"><span data-stu-id="752fc-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="752fc-121">このメソッドは、Unicode のみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="752fc-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="752fc-122">さらに、先制と、失敗、配列内のパスのいずれかの .dll のファイル名の拡張子はありません。</span><span class="sxs-lookup"><span data-stu-id="752fc-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="752fc-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="752fc-123">See also</span></span>

- [<span data-ttu-id="752fc-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="752fc-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="752fc-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="752fc-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

