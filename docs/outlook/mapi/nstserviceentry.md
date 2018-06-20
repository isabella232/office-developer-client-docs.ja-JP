---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801666"
---
# <a name="nstserviceentry"></a><span data-ttu-id="9eae7-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="9eae7-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="9eae7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9eae7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9eae7-105">MAPI のメッセージ サービスのエントリ ポイントの関数では、NST ストアとして PST ベースのローカル ストアをラップするプロバイダーを格納します。</span><span class="sxs-lookup"><span data-stu-id="9eae7-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9eae7-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9eae7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9eae7-107">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="9eae7-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="9eae7-108">MAPI プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9eae7-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="9eae7-109">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9eae7-109">Called by:</span></span>  <br/> |<span data-ttu-id="9eae7-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="9eae7-110">MAPI</span></span>  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a><span data-ttu-id="9eae7-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="9eae7-111">Parameters</span></span>

 <span data-ttu-id="9eae7-112">**NSTServiceEntry**は、 **[MSGSERVICEENTRY](msgserviceentry.md)** 関数のプロトタイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="9eae7-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="9eae7-113">そのパラメーターについては、 **[MSGSERVICEENTRY](msgserviceentry.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9eae7-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="9eae7-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="9eae7-114">Return values</span></span>

<span data-ttu-id="9eae7-115">戻り値については、 **[MSGSERVICEENTRY](msgserviceentry.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9eae7-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9eae7-116">備考</span><span class="sxs-lookup"><span data-stu-id="9eae7-116">Remarks</span></span>

<span data-ttu-id="9eae7-117">Msmapi32.dll のこの関数のアドレスを検索するには、 **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** を使用して、プロシージャ名として"NSTServiceEntry"を指定します。</span><span class="sxs-lookup"><span data-stu-id="9eae7-117">When using **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="9eae7-118">レプリケーション API を使用するには、MAPI ストア プロバイダーする必要があります最初を開き**[NSTServiceEntry](nstserviceentry.md)** を呼び出すことによって PST ベースのローカル ストアをラップします。</span><span class="sxs-lookup"><span data-stu-id="9eae7-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="9eae7-119">プロバイダーは、レプリケーションを実行するための API、 **[IOSTX](iostxiunknown.md)** **[IPSTX](ipstxiunknown.md)**、主要なインタ フェースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9eae7-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="9eae7-120">NST ストアには、次の「解説」が適用されます。</span><span class="sxs-lookup"><span data-stu-id="9eae7-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="9eae7-121">**NSTServiceEntry**を使用している MAPI プロバイダーを実装する場合は、グローバル プロファイル セクション内の情報を保存しないでください。</span><span class="sxs-lookup"><span data-stu-id="9eae7-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="9eae7-122">グローバル プロファイル セクションでは、多くのプロバイダーによって共有され、このプロファイルに格納されたデータが上書きされることができます。</span><span class="sxs-lookup"><span data-stu-id="9eae7-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="9eae7-123">既存の変更のタイムスタンプを持つアイテムだけが保存されるときに更新のタイムスタンプを取得します。</span><span class="sxs-lookup"><span data-stu-id="9eae7-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="9eae7-124">競合チェックは発生しません自動的にアイテムが保存されます。</span><span class="sxs-lookup"><span data-stu-id="9eae7-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="9eae7-125">重複データ検出は、アイテムが保存されたときに発生しません。</span><span class="sxs-lookup"><span data-stu-id="9eae7-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="9eae7-126">サーバーのキャッシュされたバージョンを表すファイルが追加されます。NST です。</span><span class="sxs-lookup"><span data-stu-id="9eae7-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="9eae7-127">グローバル プロファイル セクションへのポインターを取得するには、メッセージ サービスは、下記のように**pbNSTGlobalProfileSectionGuid**を使用してサポート オブジェクトの**[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9eae7-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="9eae7-128">この例では、メッセージ サービスのサポート オブジェクトは、 **IMAPISupport::OpenProfileSection**が既定のプロファイル セクション内の**[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** プロパティによって識別されるプロファイルのセクションを返すようにしてください。</span><span class="sxs-lookup"><span data-stu-id="9eae7-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="9eae7-129">サポート オブジェクトが既定のプロファイル セクションを開くことができますこのプロファイルのセクションを取得するには、 **PR_SERVICE_UID**を取得し、結果を適切なグローバル プロファイル セクションを取得するのには**IMAPISupport::OpenProfileSection**に渡します。</span><span class="sxs-lookup"><span data-stu-id="9eae7-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="9eae7-130">サポート オブジェクトは、メッセージ サービスには、このグローバル プロファイル セクションへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9eae7-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9eae7-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="9eae7-131">See also</span></span>



[<span data-ttu-id="9eae7-132">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="9eae7-132">About the Replication API</span></span>](about-the-replication-api.md)

