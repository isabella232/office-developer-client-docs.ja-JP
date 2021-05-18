---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: '最終更新日: 2013 年 2 月 24 日'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279536"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="e2a8f-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="e2a8f-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="e2a8f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2a8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2a8f-105">個人用フォルダー (.pst) ファイルのロック解除手順を開始します。</span><span class="sxs-lookup"><span data-stu-id="e2a8f-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="e2a8f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2a8f-106">Parameters</span></span>

 <span data-ttu-id="e2a8f-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="e2a8f-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="e2a8f-108">[in]サードパーティのダイナミック リンク ライブラリ (DLL) のパスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2a8f-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="e2a8f-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="e2a8f-109">_pvClientData_</span></span>
  
> <span data-ttu-id="e2a8f-110">[in]クライアント データへのポインター。これは、PST プロバイダーによって DLL の HrTrustedPSTOverrideHandlerCallback 関数への後続の呼び出しに渡されます。</span><span class="sxs-lookup"><span data-stu-id="e2a8f-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="e2a8f-111">このクライアント データは、PST をロック解除する必要があるかどうかを確認するために DLL で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e2a8f-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2a8f-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="e2a8f-112">Return value</span></span>

<span data-ttu-id="e2a8f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2a8f-113">S_OK</span></span>
  
> <span data-ttu-id="e2a8f-114">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="e2a8f-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2a8f-115">注釈</span><span class="sxs-lookup"><span data-stu-id="e2a8f-115">Remarks</span></span>

<span data-ttu-id="e2a8f-116">wzDllPath パラメーターで指定された DLL は、デジタル証明書を使用して署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2a8f-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="e2a8f-117">DLL は、次のシグネチャを持つ関数もエクスポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2a8f-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="e2a8f-118">この関数は、PST の IMsgStore オブジェクトへのポインター、IPSTOVERRIDE1 インターフェイスを実装する IUnknown オブジェクトへのポインター、および pvClientData を介して最初に提供されたデータへのポインターを使用して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e2a8f-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="e2a8f-119">詳細については、「PST オーバーライド[ハンドラーを実装して、2007 年の PSTDisableGrow](https://support.microsoft.com/kb/956070)ポリシーをバイパスするOutlook参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2a8f-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2a8f-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2a8f-120">See also</span></span>



[<span data-ttu-id="e2a8f-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2a8f-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="e2a8f-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2a8f-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

