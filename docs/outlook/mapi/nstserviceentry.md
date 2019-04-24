---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280055"
---
# <a name="nstserviceentry"></a><span data-ttu-id="02ba7-103">NSTServiceEntry</span><span class="sxs-lookup"><span data-stu-id="02ba7-103">NSTServiceEntry</span></span>

  
  
<span data-ttu-id="02ba7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02ba7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02ba7-105">MAPI ストアプロバイダーのメッセージサービスエントリポイント関数。 PST ベースのローカルストアを NST ストアとしてラップします。</span><span class="sxs-lookup"><span data-stu-id="02ba7-105">Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="02ba7-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="02ba7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02ba7-107">実装元:</span><span class="sxs-lookup"><span data-stu-id="02ba7-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="02ba7-108">MAPI プロバイダー</span><span class="sxs-lookup"><span data-stu-id="02ba7-108">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="02ba7-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="02ba7-109">Called by:</span></span>  <br/> |<span data-ttu-id="02ba7-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="02ba7-110">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="02ba7-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="02ba7-111">Parameters</span></span>

 <span data-ttu-id="02ba7-112">**nstserviceentry**は、 **[msgserviceentry](msgserviceentry.md)** 関数プロトタイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="02ba7-112">**NSTServiceEntry** uses the **[MSGSERVICEENTRY](msgserviceentry.md)** function prototype.</span></span> <span data-ttu-id="02ba7-113">パラメーターの詳細については、「 **[msgserviceentry](msgserviceentry.md)**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ba7-113">For information on its parameters, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="return-values"></a><span data-ttu-id="02ba7-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="02ba7-114">Return values</span></span>

<span data-ttu-id="02ba7-115">戻り値の詳細については、「 **[msgserviceentry](msgserviceentry.md)**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02ba7-115">For information on return values, see **[MSGSERVICEENTRY](msgserviceentry.md)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="02ba7-116">解説</span><span class="sxs-lookup"><span data-stu-id="02ba7-116">Remarks</span></span>

<span data-ttu-id="02ba7-117">**[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** を使用して msmapi32 でこの関数のアドレスを検索する場合は、プロシージャ名として "nstserviceentry" を指定します。</span><span class="sxs-lookup"><span data-stu-id="02ba7-117">When using **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** to look for the address of this function in msmapi32.dll, specify "NSTServiceEntry" as the procedure name.</span></span> 
  
<span data-ttu-id="02ba7-118">レプリケーション API を使用するには、最初に**[nstserviceentry](nstserviceentry.md)** を呼び出して、MAPI ストアプロバイダーが PST ベースのローカルストアを開いてラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="02ba7-118">To use the Replication API, a MAPI store provider must first open and wrap a PST-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="02ba7-119">プロバイダーは、API の主なインターフェイスである**[iostx](iostxiunknown.md)** と**[ipstx](ipstxiunknown.md)** を使用して、レプリケーションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="02ba7-119">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> 
  
<span data-ttu-id="02ba7-120">次の解説は、NST ストアに適用されます。</span><span class="sxs-lookup"><span data-stu-id="02ba7-120">The following remarks apply to an NST store:</span></span>
  
- <span data-ttu-id="02ba7-121">**nstserviceentry**を使用する MAPI プロバイダーを実装する場合は、[グローバルプロファイル] セクションに情報を格納しないでください。</span><span class="sxs-lookup"><span data-stu-id="02ba7-121">Do not store any information in the global profile section when implementing a MAPI provider that uses **NSTServiceEntry**.</span></span> <span data-ttu-id="02ba7-122">[グローバルプロファイル] セクションは、多くのプロバイダーによって共有され、このプロファイルに格納されているデータは上書きできます。</span><span class="sxs-lookup"><span data-stu-id="02ba7-122">The global profile section is shared by many providers and data stored in this profile can be overwritten.</span></span> 
    
- <span data-ttu-id="02ba7-123">変更された既存のタイムスタンプを持つアイテムのみ、スタンプが保存されたときに更新されます。</span><span class="sxs-lookup"><span data-stu-id="02ba7-123">Only items with existing modification time stamps get their stamps updated when they are saved.</span></span> 
    
- <span data-ttu-id="02ba7-124">アイテムが保存されるときに競合チェックは自動的に実行されません。</span><span class="sxs-lookup"><span data-stu-id="02ba7-124">Conflict-checking does not occur automatically when items are saved.</span></span>
    
-  <span data-ttu-id="02ba7-125">アイテムの保存時に重複データ検出が発生しません。</span><span class="sxs-lookup"><span data-stu-id="02ba7-125">Duplicate detection does not occur when items are saved.</span></span> 
    
-  <span data-ttu-id="02ba7-126">サーバーのキャッシュされたバージョンを表すファイルがに追加されます。NST.</span><span class="sxs-lookup"><span data-stu-id="02ba7-126">The file representing the cached version of the server is appended with .NST.</span></span> 
    
- <span data-ttu-id="02ba7-127">グローバルプロファイルセクションへのポインターを取得するために、メッセージサービスは、以下に定義されているように、 **pbNSTGlobalProfileSectionGuid**を使用して、support オブジェクトの**[imapisupport:: openprofile](imapisupport-openprofilesection.md)** セクションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02ba7-127">To obtain a pointer to the global profile section, a message service calls **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** in the support object using **pbNSTGlobalProfileSectionGuid** as defined below:</span></span> 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- <span data-ttu-id="02ba7-128">この場合、message service の support オブジェクトは、 **imapisupport:: openprofile** section が**[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** プロパティによって識別されるプロファイルセクションを既定のプロファイルセクションにあることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02ba7-128">In this case, the support object of the message service should ensure that **IMAPISupport::OpenProfileSection** returns the profile section that is identified by the **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** property in the default profile section.</span></span> <span data-ttu-id="02ba7-129">このプロファイルセクションを取得するには、support オブジェクトで [既定のプロファイル] セクションを開き、 **PR_SERVICE_UID**を取得して、その結果を**imapisupport:: openprofile**セクションに渡すことで、適切なグローバルプロファイルセクションを取得できます。</span><span class="sxs-lookup"><span data-stu-id="02ba7-129">To get this profile section, the support object can open the default profile section, retrieve **PR_SERVICE_UID**, and pass the result to **IMAPISupport::OpenProfileSection** to retrieve the correct global profile section.</span></span> <span data-ttu-id="02ba7-130">このサポートオブジェクトは、メッセージサービスへのこのグローバルプロファイルセクションへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="02ba7-130">The support object in turn returns a pointer to this global profile section to the message service.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="02ba7-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="02ba7-131">See also</span></span>



[<span data-ttu-id="02ba7-132">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="02ba7-132">About the Replication API</span></span>](about-the-replication-api.md)

