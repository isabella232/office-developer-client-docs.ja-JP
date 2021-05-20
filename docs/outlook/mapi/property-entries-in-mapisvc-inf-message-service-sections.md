---
title: MapiSvc.inf メッセージ サービス セクションのプロパティ エントリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427998"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="cf5f8-103">MapiSvc.inf メッセージ サービス セクションのプロパティ エントリ</span><span class="sxs-lookup"><span data-stu-id="cf5f8-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="cf5f8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf5f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf5f8-105">プロパティを設定するエントリでは、次の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="cf5f8-106">**プロパティ タグ** **=** プロパティ値</span><span class="sxs-lookup"><span data-stu-id="cf5f8-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="cf5f8-107">構成データが MAPI によって事前定義されたプロパティの 1 つを表す場合、またはデータが MAPI プロパティを表していない場合は標準以外のタグを表す場合、プロパティ タグには標準の MAPI プロパティ タグを指定できます。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="cf5f8-108">標準以外のタグは、プロパティ識別子の値とプロパティの種類を組み合わせて作成されます。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="cf5f8-109">結果は 8 桁の 16 進数です。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="cf5f8-110">プロパティの値は、プロパティ タグに対して意味のある値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="cf5f8-111">メッセージ サービス セクションには、構成するメッセージ サービスに応じて、さまざまなエントリを含めできます。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="cf5f8-112">通常、次の MAPI プロパティは、一覧表示された形式のメッセージ サービス セクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="cf5f8-113">**PR_DISPLAY_NAME**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="cf5f8-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="cf5f8-114">**PR_SERVICE_DLL_NAME**  =  _DLL ファイルの名前_</span><span class="sxs-lookup"><span data-stu-id="cf5f8-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="cf5f8-115">**PR_SERVICE_ENTRY_NAME**  =  _エントリ ポイント関数の名前_</span><span class="sxs-lookup"><span data-stu-id="cf5f8-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="cf5f8-116">**PR_SERVICE_SUPPORT_FILES**  =  _ファイルの一覧_</span><span class="sxs-lookup"><span data-stu-id="cf5f8-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="cf5f8-117">**PR_SERVICE_DELETE_FILES**  =  _ファイルの一覧_</span><span class="sxs-lookup"><span data-stu-id="cf5f8-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="cf5f8-118">**PR_RESOURCE_FLAGS**  =  _ビットマスク_</span><span class="sxs-lookup"><span data-stu-id="cf5f8-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="cf5f8-119">PR_DISPLAY_NAME  ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 文字列は、ユーザー インターフェイスに表示されるメッセージ サービスの名前、ユーザーがメッセージ サービスに関連付ける名前です。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="cf5f8-120">表示名は mapisvc.inf の省略可能なエントリです。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="cf5f8-121">表示名が 2 つの部分で構成される場合があります。メッセージ サービスによって割り当てられたパーツと、ユーザーによって割り当てられたパーツ。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="cf5f8-122">ユーザーがパーツの 1 つを割り当てる責任がある場合、これは通常、クライアント アプリケーションの制御下でメッセージ サービスによって提供されるプロパティ シートと呼ばれる特別なダイアログ ボックスで処理されます。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="cf5f8-123">メッセージ サービス ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))**エントリPR_SERVICE_DLL_NAME情報** は、メッセージ サービスを含む DLL の名前です。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="cf5f8-124">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) エントリに対して提供される情報は、MAPI がメッセージ サービスを構成するために呼び出す DLL 内のエントリ ポイント関数の名前です。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="cf5f8-125">メッセージ サービス ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))**エントリにPR_SERVICE_SUPPORT_FILES** ファイルは、メッセージ サービスと一緒にインストールする必要があるファイルです。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="cf5f8-126">同様に、メッセージ サービスが **削除PR_SERVICE_DELETE_FILES、** メッセージ サービス ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) エントリ内のファイルを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="cf5f8-127">この **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) エントリは、メッセージ サービスに対して定義されたオプションのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="cf5f8-128">たとえば、メッセージ サービスSERVICE_SINGLE_COPY特定のプロファイルに 1 回しか表示されない場合に、このビットが設定されます。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="cf5f8-129">メッセージ SERVICE_NO_PRIMARY_IDENTITY ID 情報を提供しない場合は、このビットが設定されます。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="cf5f8-130">標準以外のプロパティ エントリの 2 つの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="cf5f8-131">最初のエントリは、既定のアドレス帳でプロパティ値として使用されるファイルへのパスを指定します。2 番目のエントリは、数値プロパティ値を指定します。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="cf5f8-132">どちらのエントリも、AB メッセージ サービスに固有の意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="cf5f8-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


