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
ms.openlocfilehash: 4fc3b7427fc13a024aab38c7b7df1d940a4730ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801186"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="4f1e3-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="4f1e3-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="4f1e3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f1e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f1e3-105">個人用フォルダー (.pst) ファイルのロックを解除する手順を開始します。</span><span class="sxs-lookup"><span data-stu-id="4f1e3-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="4f1e3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4f1e3-106">Parameters</span></span>

 <span data-ttu-id="4f1e3-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="4f1e3-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="4f1e3-108">[in]サード ・ パーティ製のダイナミック リンク ライブラリ (DLL) のパスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4f1e3-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="4f1e3-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="4f1e3-109">_pvClientData_</span></span>
  
> <span data-ttu-id="4f1e3-110">[in]PST プロバイダーが DLL の HrTrustedPSTOverrideHandlerCallback 関数への後続の呼び出しに渡されます、クライアントのデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4f1e3-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="4f1e3-111">DLL によっては、このクライアント データを pst ファイルのロックが解除する必要があるかどうかを確認するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f1e3-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f1e3-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4f1e3-112">Return value</span></span>

<span data-ttu-id="4f1e3-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f1e3-113">S_OK</span></span>
  
> <span data-ttu-id="4f1e3-114">関数の呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="4f1e3-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f1e3-115">備考</span><span class="sxs-lookup"><span data-stu-id="4f1e3-115">Remarks</span></span>

<span data-ttu-id="4f1e3-116">WzDllPath パラメーターで指定された DLL は、デジタル証明書を使用して署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f1e3-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="4f1e3-117">DLL では、次のシグネチャを持つ関数をエクスポートする必要がありますもします。</span><span class="sxs-lookup"><span data-stu-id="4f1e3-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="4f1e3-118">Pst ファイルの IMsgStore オブジェクトへのポインター、IPSTOVERRIDE1 インターフェイスを実装する IUnknown オブジェクトへのポインター、および pvClientData を最初に入力したデータへのポインターでは、この関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4f1e3-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="4f1e3-119">詳細については、 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするのには、PST オーバーライドするハンドラーを実装する方法](http://support.microsoft.com/kb/956070)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f1e3-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4f1e3-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f1e3-120">See also</span></span>



[<span data-ttu-id="4f1e3-121">IPSTOVERRIDE1: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f1e3-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="4f1e3-122">IPSTOVERRIDEREQ: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f1e3-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

